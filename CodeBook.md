# Getting-and-Cleaning-Data-Course-Project

This file contains describing of the data in the dataset "data_mean" and of the methods which were used for transforming data from the raw datasets to the target dataset.

The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (prefix 't' to denote time) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ) using another low pass Butterworth filter with a corner frequency of 0.3 Hz. 
Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag). 
Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. (Note the 'f' to indicate frequency domain signals). 

The dataset "data_mean" contains the next variables:
 - Subject, describes ID of a person who participated in the research. Type of data - numeric. Same to variable subject in the raw datasets.
 - Activity, describes type of activity of a person. Type of data - character. Possible values - WALKING, WALKING_UPSTAIRS, WALKING_DOWN STAIRS, SITTING, STANDING, LAYING. Same to activity labels in the raw datasets.
 - Block of data (see below). Type of data - numeric. Measurements unit - in standard gravity units 'g'.

Block of data contains the average for each activity and each subject of the mean(Mean value) and the std(Standard deviation) for the next variables:
'-XYZ' is used to denote 3-axial signals in the X, Y and Z directions. 
 - tBodyAcc-XYZ
 - tGravityAcc-XYZ
 - tBodyAccJerk-XYZ
 - tBodyGyro-XYZ
 - tBodyGyroJerk-XYZ
 - tBodyAccMag
 - tGravityAccMag
 - tBodyAccJerkMag
 - tBodyGyroMag
 - tBodyGyroJerkMag
 - fBodyAcc-XYZ
 - fBodyAccJerk-XYZ
 - fBodyGyro-XYZ
 - fBodyAccMag
 - fBodyAccJerkMag
 - fBodyGyroMag
 - fBodyGyroJerkMag

For transforming data from the raw datasets to the tidy dataset were completed the next operations:
 - was consolidated the datasets with ID of the person, ID and type of activities, measurements 
 - was filtered data for including to the target dataset "data_mean"
 - was grouped dataset by a subject and by  an activity
 - was calculated the average of each variable (the raw data from the raw datasets) for each activity and each subject


