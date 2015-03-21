###CODEBOOK

The "result.txt" file contains data showing the mean values of a range of measurements recorded on 30 subjects while they were performing six different physical activities. 

The measurements were made from signals from the accelerometers and gyrometers on Samsung smartphones. Details of the research methodology can be found here: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

##CLEANING THE DATA

The original data collected by the researchers included more than 500 measurement variables. 

The new dataset was derived from the original data with three main changes.  

First, variable names and values were cleaned up in line with tidy data principles. Variable names were converted to lower case and extraneous characters such as hyphens and brackets were removed. In the case of the categorical variable “activity” the values of the variable were converted into descriptive names (e.g, ”Walking”, “Sitting”) rather than the numeric coding in the original dataset.

##EXTRACTING THE DATA 

Second, only measurement variables which contained mean values and standard deviations of the raw measurements were included. The procedure for identifying these variables was to select any of the original variables which had the strings “mean” or “std” in their names. This reduced the number of measurement variables to 79. 


##TRANSFORMING THE DATA

Third, for each of these variables the mean of the measurements recorded for each subject performing each activity was calculated and included in the new dataset.

##STRUCTURE OF THE NEW DATASET

This results in a dataset comprising 180 rows (30 subjects times six activities) and 81 columns. 

The first column contains the variable “subjects” which records the individual subject ID. 

The second column contains the variable “activity” which records the activity being performed ((walking, standing, sitting, laying, walking downstairs and walking upstairs).

The remaining columns contain the 79 measurement variables extracted from the original dataset’s 500-plus variables. The values of these measurement variables are the mean of each measurement recorded for each subject while performing each activity.


##MEASUREMENT VARIABLE NAMES

The naming convention for the 79 measurement variables is as follows:
*“t” denotes time signal
*“f” denotes frequency domain signal
*“body” denotes body acceleration
*“gravity” denotes gravity acceleration
*“acc” denotes accelerometer measurement
*“gyro” denotes gyroscope measurement
*“jerk” denotes the jerk signal based on body linear acceleration and angular velocity
*“mag” denotes the magnitude of three-dimensional signals
*“x”, “y” and “z” denote three-axial signals in the X, Y and Z directions.
*“mean” denotes the mean value of the measurements recorded
*“meanfreq” denotes the mean frequency calculated using a weighted average of the frequency components of the signals from the smartphones 
*“std” denotes the standard deviation of the measurements recorded.

For example:
* *tbodyaccmeanx* represents the mean value of time signals for body acceleration in the X direction measured using the accelerometer
* *fbodygyromeanz* represents the mean value of frequency signals for body acceleration in the Z direction measred using the gyrometer
* *tgravityaccstdy* represents the standard deviation of time signals for gravity acceleration measured using the accelerometer
* *fbodyaccmagmean* represents the mean of the magnitude of frequency signals for body acceleration measured using the accelerometer.

##VALUES ARE NORMALISED

Note the values recorded in the original data were normalised to fall between -1 and 1.


