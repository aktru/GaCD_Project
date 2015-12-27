# Getting-and-Cleaning-Data-Course-Project
Purpose of this Project - creating tidy datasets of measurements with using raw datasets.


Raw dataset contains the sensor signals (accelerometer and gyroscope) for different people and different type of their activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWN STAIRS, SITTING, STANDING, LAYING).
More information about methods of reserching and the structure of data you can get from file "README.txt" (see folder "./getdata_projectfiles_UCI HAR Dataset/UCI HAR Dataset/").
Source raw data is https://d396qusza40orc.cloudfront.net/getdata_projectfiles_UCI HAR Dataset.zip  

Raw data sources contains different data from:

 - ./getdata_projectfiles_UCI HAR Dataset/UCI HAR Dataset/ - readme, description of features and activity labels

 - ./getdata_projectfiles_UCI HAR Dataset/UCI HAR Dataset/train/ - raw data for train

 - ./getdata_projectfiles_UCI HAR Dataset/UCI HAR Dataset/test/ - raw data for test


Tidy dataset is "data_mean". 
This dataset contains only the average data of each variable (the measurements on the mean and standard deviation for each measurement) for each activity and each subject.
The file "data_mean.txt" contains copy of this dataset for research.

I use the script "run_analysis.R" for transforming the raw datasets to the tidy dataset.

This script includes several basic steps:
 - Checking and loading of R packages data.table and dplyr
 - Uploading the column names for datasets, raw data for train and for test datasets
 - Selecting columns which contains the measurements on the mean and standard deviation for each measurement
 - Creating the consolidated dataset "data_summary" for train and test data with specifying activity label and ID of subject for each measurement. I define new variable "Dataset" for identifying each measurement in the consolidated dataset.
 - Creating the consolidated dataset "data_mean" by using function summarise for calculation of average of each variable for each activity and each subject.

You can upload the tidy dataset by using function of write.table with the argument "row.name=FALSE".

It's can be important for running of the script:
 - raw data are located in the working folder and structure of folders is unchanged after unzipping of the archive
 - the script was developed in the environment of R Studio for Windows
