# Introduction

The script `run_analysis.R`performs the 5 steps provided in the project instructions.

* Step 1: Similar data sets are merged using the `rbind()` function. 
* Step 2: Columns with mean and standard deviation measures are extracted. After extracting these columns, they are given the correct names, taken from `features.txt`.
* Step 3: As activity data is addressed with values 1 to 6, activity names and IDs are taken from `activity_labels.txt` and substituted in the dataset.
* Step 4: Columns with vague column names are corrected.
* Step 5: A new dataset is generated with all the average measures for each subject and activity type (30 subjects * 6 activities = 180 rows). The output file is called `averages_data.txt`, and uploaded to this repository.

# Variables

* `x_train`, `y_train`, `x_test`, `y_test`, `subject_train` and `subject_test` are data from the downloaded files.
* `x_data`, `y_data` and `subject_data` are merge datasets to facilitate analysis.
* `features` contains the correct names for the `x_data` dataset.
* `mean_and_std_features` - a numeric vector used to extract the desired data.
* `full_data` merges `x_data`, `y_data` and `subject_data` in a big dataset.
* `averages_data` contains the relevant averages.
* `ddply()` from the plyr package is used to apply `colMeans()` and ease the development.