# WearableDataAnalysis
## (This is for the Getting and Cleaning Data Course Final Project)


This program loads all data measured and generates a brief summary. In detail the following is happening:

1.  Use read.table to read the data into R.
2.  x_data contains the x train and x text which were combined in this order using rbind.
3.  y_data and sub_data were created by reprsating Step 2 y train and y test, as well as sub train and sub test respectively. 
4   all_data was created using cbind in the following order: sub_data, y_data, x_data
5.  The features text file was loaded using read.table and assigned to avg_sd. The detail is in the Codebook
6.  ext was created by subsetting means and stds out of avg_sd 
7.  ext was used to subset all_data which removed all columns that were not avg and std resulting in ext_avg_sd.
8.  Column names and activities were assigned to ext_avg_sd.
9.  The melt function was used to convert from wide to long format, using subject and activities as the id.
10. The dcast function was used to convert from long to wide format and calculating the mean of each activity for each subject.
11. Melted the data again to tidy format.
12. A text file named Warable tidy data was created.
