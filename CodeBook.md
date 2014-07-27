# CodeBook
antekai  
Sunday, July 27, 2014  
The purpose of this project is to demonstrate ability to collect, work with, and clean a data set. The goal is to prepare tidy data that can be used for later analysis. Data collected from the accelerometers from the Samsung Galaxy S smartphone. A full description is available at the site where the data was obtained: [Human Activity Recognition Using Smartphones](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)
    

##Getting & Cleaning Data with R


###R script

Packages required: `data.table`,`reshape2`

[run_analysis.R](https://github.com/antekai/GCDproject/blob/master/run_analysis.R) in summary does the following:

1. Gets an reads: [DataSet](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip)
2. Merges the training and the test sets to create one data set.
3. Extracts only the measurements on the mean and standard deviation for each    measurement. 
4. Uses descriptive activity names to name the activities in the data set
5. Appropriately labels the data set with descriptive variable names. 
6. Creates a second, independent tidy data set with the average of each variable for each activity and each subject.
7. Saves tidy data set created as comma delimited file 

If you are interested more in Rscript check:
[Detailed preview of Rscript](http://htmlpreview.github.io/?https://github.com/antekai/GCDproject/blob/master/run_analysis.html)

You can view output tidy data set here: [tidyData](https://github.com/antekai/GCDproject/blob/master/tidyData.csv)

###Variable list and descriptions

Variable name | Description
-----------------|------------
subject | ID the subject who performed the activity for each window sample. Its range is from 1 to 30.
activity | Activity name
featDomain | Feature: Time domain signal or frequency domain signal (Time or Freq)
featInstrument | Feature: Measuring instrument (Accelerometer or Gyroscope)
featAcceleration | Feature: Acceleration signal (Body or Gravity)
featVariable | Feature: Variable (Mean or SD)
featJerk | Feature: Jerk signal
featMagnitude | Feature: Magnitude of the signals calculated using the Euclidean norm
featAxis | Feature: 3-axial signals in the X, Y and Z directions (X, Y, or Z)
featCount | Feature: Count of data points used to compute `average`
featAverage | Feature: Average of each variable for each activity and each subject


