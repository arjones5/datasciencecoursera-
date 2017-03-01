# Intro

The script 'run_analysis.R' executes the following 4 steps

* All similar data is merged using the 'rbind()' function. This addresses the entities with the redundant data
* The columns with the mean and SD measures are taken from the dataset. After extracting these columns, they are given the correct names, taken from 'features.txt'.
* Activity values are reassigned with values 1:6, activity values are taken from 'activity_labels.txt' and they are replaced in the dataset.
* Output file is called 'tidyAvergagesData.txt', and uploaded to this repository.

# Variables

* 'x_train', 'y_train', 'x_test', 'y_test', 'subject_train' and 'subject_test' is the data from the downloaded files.
* 'x_data', 'y_data' and 'subject_data' merge the previous datasets to further analysis.
* 'features' contains the correct names for the 'x_data' dataset, which are applied to the column names stored in 'mean_and_std_features', a numeric vector used to extract the desired data.
* A similar approach is taken with activity names through the 'activities' variable.
* 'all_data' merges 'x_data', 'y_data' and 'subject_data' in a big dataset.
* 'tidyAveragesData.txt' contains the relevant averages which will be later stored in a '.txt' file. 'ddply()' from the plyr package is used to apply 'colMeans()' and ease the development.
