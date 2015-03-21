##run_analysis.R
This is an R script submitted for the course project in the Getting and Cleaning Data course.

###What it does
The run_analysis.R script:
* Reads into R data collected from 30 subjects using the accelerometer and gyroscope from Samsung smartphones;
* Cleans up that data according to tidy data principles; 
* Transforms the dataset by extracting a subset of variables of interest; 
* Further transforms the dataset by calculating the mean values of each of the variables for each subject in each of six conditions;
* Saves this new dataset as a text file.

### Getting the data
The original data should be obtained from here: https://class.coursera.org/getdata-012/human_grading/view/courses/973499/assessments/3/submissions
The following 7 text files should be unzipped and saved in your R working directory: "X_train.txt", "X_test.txt", "y_train.txt", "y_test.txt", "subject_train.txt", "subject_test.txt", "features.txt".

###Install dplyr package
The script requires the R package dplyr to be installed. This should be done in R before running the script by using the command *install.packages(“dplyr”)*.

###Reading the output
After the script has been run, the output is a text file called “result.txt” saved in your R working directory. 
This data can be read back into R using the command *read.table (result.txt, header=TRUE)*.

