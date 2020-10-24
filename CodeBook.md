Codebook
========

Variables
---------

dtTidy

Variable                                   | Comments
-------------------------------------------|-----------
Subject                                    |  subject identifier of volunteer (1-30)
ActivityName                               |  name ofactivity subject performed (LAYING,SITTING,STANDING,WALKING,WALKING_DOWNSTAIRS,WALKING_UPSTAIRS)
timeBodyAccelerometerMeanX                 |  mean of tBodyAcc-mean()-X
timeBodyAccelerometerMeanY                 |  mean of tBodyAcc-mean()-Y
timeBodyAccelerometerMeanZ                 |  mean of tBodyAcc-mean()-Z
timeBodyAccelerometerStdX                  |  mean of tBodyAcc-std()-X
timeBodyAccelerometerStdY                  |  mean of tBodyAcc-std()-Y
timeBodyAccelerometerStdZ                  |  mean of tBodyAcc-std()-Z
timeGravityAccelerometerMeanX              |  mean of tGravityAcc-mean()-X
timeGravityAccelerometerMeanY              |  mean of tGravityAcc-mean()-Y
timeGravityAccelerometerMeanZ              |  mean of tGravityAcc-mean()-Z
timeGravityAccelerometerStdX               |  mean of tGravityAcc-std()-X
timeGravityAccelerometerStdY               |  mean of tGravityAcc-std()-Y
timeGravityAccelerometerStdZ               |  mean of tGravityAcc-std()-Z
timeBodyAccelerometerJerkMeanX             |  mean of tBodyAccJerk-mean()-X
timeBodyAccelerometerJerkMeanY             |  mean of tBodyAccJerk-mean()-Y
timeBodyAccelerometerJerkMeanZ             |  mean of tBodyAccJerk-mean()-Z
timeBodyAccelerometerJerkStdX              |  mean of tBodyAccJerk-std()-X
timeBodyAccelerometerJerkStdY              |  mean of tBodyAccJerk-std()-Y
timeBodyAccelerometerJerkStdZ              |  mean of tBodyAccJerk-std()-Z
timeBodyGyroscopeMeanX                     |  mean of tBodyGyro-mean()-X
timeBodyGyroscopeMeanY                     |  mean of tBodyGyro-mean()-Y
timeBodyGyroscopeMeanZ                     |  mean of tBodyGyro-mean()-Z
timeBodyGyroscopeStdX                      |  mean of tBodyGyro-std()-X
timeBodyGyroscopeStdY                      |  mean of tBodyGyro-std()-Y
timeBodyGyroscopeStdZ                      |  mean of tBodyGyro-std()-Z
timeBodyGyroscopeJerkMeanX                 |  mean of tBodyGyroJerk-mean()-X
timeBodyGyroscopeJerkMeanY                 |  mean of tBodyGyroJerk-mean()-Y
timeBodyGyroscopeJerkMeanZ                 |  mean of tBodyGyroJerk-mean()-Z
timeBodyGyroscopeJerkStdX                  |  mean of tBodyGyroJerk-std()-X
timeBodyGyroscopeJerkStdY                  |  mean of tBodyGyroJerk-std()-Y
timeBodyGyroscopeJerkStdZ                  |  mean of tBodyGyroJerk-std()-Z
timeBodyAccelerometerMagMean               |  mean of tBodyAccMag-mean()
timeBodyAccelerometerMagStd                |  mean of tBodyAccMag-std()
timeGravityAccelerometerMagMean            |  mean of tGravityAccMag-mean()
timeGravityAccelerometerMagStd             |  mean of tGravityAccMag-std()
timeBodyAccelerometerJerkMagMean           |  mean of tBodyAccJerkMag-mean()
timeBodyAccelerometerJerkMagStd            |  mean of tBodyAccJerkMag-std()
timeBodyGyroscopeMagMean                   |  mean of tBodyGyroMag-mean()
timeBodyGyroscopeMagStd                    |  mean of tBodyGyroMag-std()
timeBodyGyroscopeJerkMagMean               |  mean of tBodyGyroJerkMag-mean()
timeBodyGyroscopeJerkMagStd                |  mean of tBodyGyroJerkMag-std()
frequencyBodyAccelerometerMeanX            |  mean of fBodyAcc-mean()-X
frequencyBodyAccelerometerMeanY            |  mean of fBodyAcc-mean()-Y
frequencyBodyAccelerometerMeanZ            |  mean of fBodyAcc-mean()-Z
frequencyBodyAccelerometerStdX             |  mean of fBodyAcc-std()-X
frequencyBodyAccelerometerStdY             |  mean of fBodyAcc-std()-Y
frequencyBodyAccelerometerStdZ             |  mean of fBodyAcc-std()-Z
frequencyBodyAccelerometerJerkMeanX        |  mean of fBodyAccJerk-mean()-X
frequencyBodyAccelerometerJerkMeanY        |  mean of fBodyAccJerk-mean()-Y
frequencyBodyAccelerometerJerkMeanZ        |  mean of fBodyAccJerk-mean()-Z
frequencyBodyAccelerometerJerkStdX         |  mean of fBodyAccJerk-std()-X
frequencyBodyAccelerometerJerkStdY         |  mean of fBodyAccJerk-std()-Y
frequencyBodyAccelerometerJerkStdZ         |  mean of fBodyAccJerk-std()-Z
frequencyBodyGyroscopeMeanX                |  mean of fBodyGyro-mean()-X
frequencyBodyGyroscopeMeanY                |  mean of fBodyGyro-mean()-Y
frequencyBodyGyroscopeMeanZ                |  mean of fBodyGyro-mean()-Z
frequencyBodyGyroscopeStdX                 |  mean of fBodyGyro-std()-X
frequencyBodyGyroscopeStdY                 |  mean of fBodyGyro-std()-Y
frequencyBodyGyroscopeStdZ                 |  mean of fBodyGyro-std()-Z
frequencyBodyAccelerometerMagMean          |  mean of fBodyAccMag-mean()
frequencyBodyAccelerometerMagStd           |  mean of fBodyAccMag-std()
frequencyBodyBodyAccelerometerJerkMagMean  |  mean of fBodyBodyAccJerkMag-mean()
frequencyBodyBodyAccelerometerJerkMagStd   |  mean of fBodyBodyAccJerkMag-std()
frequencyBodyBodyGyroscopeMagMean          |  mean of fBodyBodyGyroMag-mean()
frequencyBodyBodyGyroscopeMagStd           |  mean of fBodyBodyGyroMag-std()
frequencyBodyBodyGyroscopeJerkMagMean      |  mean of fBodyBodyGyroJerkMag-mean()
frequencyBodyBodyGyroscopeJerkMagStd       |  mean of fBodyBodyGyroJerkMag-std()


Transformations
---------------

1. Dataset was initially split into subject, activity, and features. Each of these were further split into test and train sets. Merging was performed to get everything in one dataset.

2. Dataset activity variable was merged with the activity lookup table to yield descriptive activity name.

3. Features were filtered to only those matching mean() or std(). Dataset was merged with derived feature code lookup table to get featureName.

4. Datset was melted with subject, activity, and feature as id variables.

5. An average was added per group of subject, activity, and feature

6. Since this is a TIDY data set, new descriptive columns were created to represent specific variables from the single feature variable (Domain,Instrument,Acceleration,StatVariable,Jerk,Magnitude and Axis) using grepl. The original feature is now redundant and removed.

7. The dataset is then written to `tidy.txt` file

Data
----

Copied from readme.txt in original dataset.

> ==================================================================
> Human Activity Recognition Using Smartphones Dataset
> Version 1.0
> ==================================================================
> Jorge L. Reyes-Ortiz, Davide Anguita, Alessandro Ghio, Luca Oneto.
> Smartlab - Non Linear Complex Systems Laboratory
> DITEN - Università degli Studi di Genova.
> Via Opera Pia 11A, I-16145, Genoa, Italy.
> activityrecognition@smartlab.ws
> www.smartlab.ws
> ==================================================================
> 
> The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 
> 
> The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. See 'features_info.txt' for more details. 
> 
> For each record it is provided:
> ======================================
> 
> - Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
> - Triaxial Angular velocity from the gyroscope. 
> - A 561-feature vector with time and frequency domain variables. 
> - Its activity label. 
> - An identifier of the subject who carried out the experiment.
> 
> The dataset includes the following files:
> =========================================
> 
> - 'README.txt'
> 
> - 'features_info.txt': Shows information about the variables used on the feature vector.
> 
> - 'features.txt': List of all features.
> 
> - 'activity_labels.txt': Links the class labels with their activity name.
> 
> - 'train/X_train.txt': Training set.
> 
> - 'train/y_train.txt': Training labels.
> 
> - 'test/X_test.txt': Test set.
> 
> - 'test/y_test.txt': Test labels.
> 
> The following files are available for the train and test data. Their descriptions are equivalent. 
> 
> - 'train/subject_train.txt': Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30. 
> 
> - 'train/Inertial Signals/total_acc_x_train.txt': The acceleration signal from the smartphone accelerometer X axis in standard gravity units 'g'. Every row shows a 128 element vector. The same description applies for the 'total_acc_x_train.txt' and 'total_acc_z_train.txt' files for the Y and Z axis. 
> 
> - 'train/Inertial Signals/body_acc_x_train.txt': The body acceleration signal obtained by subtracting the gravity from the total acceleration. 
> 
> - 'train/Inertial Signals/body_gyro_x_train.txt': The angular velocity vector measured by the gyroscope for each window sample. The units are radians/second. 
> 
> Notes: 
> ======
> - Features are normalized and bounded within [-1,1].
> - Each feature vector is a row on the text file.
> 
> For more information about this dataset contact: activityrecognition@smartlab.ws
> 
> License:
> ========
> Use of this dataset in publications must be acknowledged by referencing the following publication [1] 
> 
> [1] Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support Vector Machine. International Workshop of Ambient Assisted Living (IWAAL 2012). Vitoria-Gasteiz, Spain. Dec 2012
> 
> This dataset is distributed AS-IS and no responsibility implied or explicit can be addressed to the authors or their institutions for its use or misuse. Any commercial use is prohibited.
> 
> Jorge L. Reyes-Ortiz, Alessandro Ghio, Luca Oneto, Davide Anguita. November 2012.
> 
