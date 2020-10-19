# coursera-data-science-getting-and-cleaning-data
Peer-graded Assignment: Getting and Cleaning Data Course Project in [Coursera - Data Science Specialization](https://www.coursera.org/specializations/jhu-data-science)/[Course 3  Getting and Cleaning Data](https://www.coursera.org/learn/data-cleaning?specialization=jhu-data-science).

## Introduction
This repository contains the R script, unzipped raw data, and the output tidy data for the course project.

The folder data has the below structure.

  data                                     
   ¦--getdata_projectfiles_UCI HAR Dataset 
   ¦   °--UCI HAR Dataset                  
   ¦       ¦--activity_labels.txt          
   ¦       ¦--features.txt                 
   ¦       ¦--features_info.txt            
   ¦       ¦--README.txt                   
   ¦       ¦--test                         
   ¦       ¦   ¦--Inertial Signals         
   ¦       ¦   ¦--subject_test.txt         
   ¦       ¦   ¦--X_test.txt               
   ¦       ¦   °--y_test.txt               
   ¦       °--train                        
   ¦           ¦--Inertial Signals         
   ¦           ¦--subject_train.txt        
   ¦           ¦--X_train.txt              
   ¦           °--y_train.txt              
   ¦--tidy_data1.txt                       
   °--tidy_data2.txt  

## Raw data
The original dataset can be downloaded at: 
[Human Activity Recognition Using Smartphones Data Set](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip)

In this repo, the raw data is stored in: path2raw = /data/getdata_projectfiles_UCI HAR Dataset/UCI HAR Dataset/. Features are normalised and stored in X_test.txt and X_train.txt. Activity labels are stored in y_test.txt and y_train.txt. Subject IDs are stored in subject_test.txt and subject_train.txt. Feature and activity labels are stored in features.txt and activity_labels.txt respectively.

See CodeBook.md for more information.

## Script for data merging and cleaning
Run run_analysis.R and you will get two tidy datasets (see the below description).

The steps include:

1. Merges the training and the test sets to create one data set.

2. Extracts only the measurements on the mean and standard deviation for each measurement.

3. Uses descriptive activity names to name the activities in the data set.

4. Appropriately labels the data set with descriptive variable names.

5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

## Tidy data
Two tidy datasets, one for steps 1-4 and the other for steps 1-5, are output as a tab-delimited file called tidy_data1.txt and tidy_data2.txt under data folder.

## CodeBook.md
A detailed description of the raw dataset and the two tidy datasets.
