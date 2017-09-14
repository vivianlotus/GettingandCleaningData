## Code Book for Course Project

### Overview

[Source](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip) of the original data:

	https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

[Full Description](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones) at the site where the data was obtained:

	http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones
	
### Process

The script `run_analysis.R` performs the following process to clean up the data
and create tiny data sets:

1. Merge the training and test sets to create one data set.

2. Reads `features.txt` and uses only the measurements on the mean and standard
   deviation for each measurement. 

3. Reads `activity_labels.txt` and applies readable activity names to
   name the activities in the data set.

4. Labels the data set with descriptive names. 

5. Creates a tidy data set with the average of each variable for each activity and each subject. The result is saved as `MeanData.txt`.

### Variables

- test.x - table contents of `test/X_test.txt`
- train.x - table contents of `train/X_train.txt`
- test.y - table contents of `test/Y_test.txt`
- train.y - table contents of `train/Y_train.txt`
- test.Subject - table contents of `test/subject_test.txt`
- train.Subject - table contents of `test/subject_train.txt`
- trainData - combined data set of train.x and train.y
- testData - combined data set of test.x and test.y
- fullData - combined data set of trainData and testData
- featureName - Names of data columns from `features.txt`
- featureIndex - index of mean and std in featureName
- activityName - table contents of `activity_labels.txt`
- finalData$activity- replace columns names with readable activity names
- names(finalData) - label the data set with descriptive names
- summarise_each(funs(mean)): get the mean of each variable for each activity and subject



### Output

#### MeanData.txt

`MeanData.txt` is a 180x68 data frame.
