# GettingandCleaningData


Data Input
---------

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 


Analysis Script
---------

`run_analysis.R`: this script takes the input data, and creates the output file 

The script first downloads and unzips the dataset from the above url. The script then reads the test and train sets, merges them in No.1.  Then it extracts the mean and std features in No.2. In No.3, it uses descriptive activity names to name the activities in the data set. It then builds up a series of labeled columns to represent single variables from the feature in No.4.  It calculates the average of each variable and writes out this data set to `MeanData.txt`in No.5.


Output
---------

Tidy dataset: `MeanData.txt`


Code Book
---------

`CodeBook.md`: describes the variables, the data, and any transformations or work that you performed to clean up the data
