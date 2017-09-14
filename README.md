# GettingandCleaningData


Input
-----

Data set: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 


Analysis Script
---------------

`run_analysis.R`: this script takes the input data, and creates the output file 

The script first downloads and unzips the dataset from the above url. The script then reads the test and training sets, merges them (1).  It filters down the mean and std features, and selects only these (2) It merges in the activity names for the activities (3) It then builds up a series of labeled columns to represent single variables from the feature. (4)  It calculates the average of each variable and writes out this data set to `tidy.txt` (5)


Output
------

* Tidy dataset: `tidy.txt`


Code Book
---------

`CodeBook.md`: describes the variables, the data, and any transformations or work that you performed to clean up the data
