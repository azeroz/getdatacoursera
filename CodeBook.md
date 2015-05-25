Getting and Cleaning Data (Coursera). Course Project Codebook
==============================================================

## Original Data

There original data comes from the smartphone accelerometer and gyroscope 3-axial raw signals, 
which have been processed using various signal processing techniques to measurement vector consisting
of 561 features. For detailed description of the original dataset, please see `features_info.txt` in
the zipped dataset file.

- [source](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip) 
- [description](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)


### Attribute Information
For each record in the dataset it is provided: 

- Triaxial acceleration from the accelerometer (total acceleration) and the
    estimated body acceleration. 
  - Triaxial Angular velocity from the gyroscope. 
  - A 561-feature vector with time and frequency domain variables. 
  - Its activity label. 
  - An identifier of the subject who carried out the experiment.

### Section 1. Merge the training and the test sets to create one data set.
Read data into tables located in:

  - X_test.txt 
  - X_train.txt
  - y_test.txt
  - y_train.txt
  - subject_test.txt
  - features.txt
  - subject_train.txt

Assign column names and join to form one dataset 

### Section 2. Extract only the measurements on the mean and standard deviation for each measurement.
Extract from merged dataset to columns names that contain "mean" or "std"

### Section 3. Use descriptive activity names to name the activities in the data set 
Combine MeanDF and StdDF column-wise and add Person Id and Activity columns

### Section 4. Appropriately label the data set with descriptive activity names. 
Give activity proper names instead of number, recode into factor

### Section 5. Create a second, independent tidy data set with the average of each variable for each activity and each subject 
Group by PersonId and Activity, summarize each column by mean and output.
