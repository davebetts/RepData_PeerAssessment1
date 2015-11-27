# PROJECT AND DATA DESCRIPTION:
The following project is a summation of body movement data recorded for 30 volunteer participants (subjects) between the ages of 19 - 48, using a Samsung Galaxy S smartphone.   Measurements of linear and angular movements were collected by the smartphones' accelerometers and gyroscopes.  Each measurement was recorded during a specified window of time.  Each measurement variable for all particpants were then normalized so that all movement values are between -1 and 1, which also eliminates the units of measurement.

**Client:** Course Project for Getting and Cleaning Data

## DATA CLASSIFICATION:
Activity types were assigned manually using video recordings of the partcipants' activities.  The 30 particpants were separated into two groups.  70% of the individuals were used to train the software to recognize activity types, and the remaining 30% were used to test the efficiency of the trained software.

## PROJECT AND DATA DESCRIPTION:
The following project is a summation of body movement data recorded for 30 volunteer participants (subjects) between the ages of 19 - 48, using a Samsung Galaxy S smartphone.   Measurements of linear and angular movements were collected by the smartphones' accelerometers and gyroscopes.  Each measurement was recorded during a specified window of time.  Each measurement variable for all particpants were then normalized so that all movement values are between -1 and 1, which also eliminates the units of measurement.

Additional information regarding the study can be found in the "README.txt" found within the original data files, as well as 
http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones 

The data used for this project are retrieved from:
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 

### Objectives: 
1. Combine a previously divided set of observations of the movements of 30 individuals that has been divided into multiple files 
  1. Training measurements  ('train/X_train.txt')
  2. Testing measurements ('test/X_test.txt')
  3. Measurement variables names ('features.txt')
  4. Observation labels
    1. Activity IDs ('train/y_train.txt', 'test/y_test.txt')
    2. Activity names ('activity_labels.txt')
    3. Participant ID ('train/subject_train.txt', 'test/subject_test.txt')
2. Summarize the combined data set
  1. Using the mean and standard deviation (std) of the measurements
  2. Summarize subset to produce a single mean value per measurement per activity for each activity for each participant.
  c. Relable measurements and activities with descriptive (human readable) names

The description provided by the client (Course Project for Getting and Cleaning Data) is as follows:

"You should create one R script called run_analysis.R that does the following." 
* Merges the training and the test sets to create one data set. (Objective 1)
* Extracts only the measurements on the mean and standard deviation for each measurement. (Objective 2.i)
* Uses descriptive activity names to name the activities in the data set (Objective 2.iii)
* Appropriately labels the data set with descriptive variable names. (Objective 2.iii)
* From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject. (Objective 2ii)

Because the term "measurements" was ambiguous, mean frequency measurements were included because they fit within the clients description of retaining means.  The columns have been sorted to facilitate the both the removal of the mean frequency columns and to group similar measurements to increase readability of the table alone.

For the goal of "descriptive variable names" complete words were used for the naming of the measuremetn variables.  Because the measurement names are a combination of multiple terms, capitals and underscores were used to provide visual breaks between terms.  Although all lower case characters and the absence of special characters are encouraged, readabibilty warrants their inclusion in this case.

Movement is measured by accelerometers, and gyroscopes.
Movement has X, Y, and Z directionality, as well as Jerk movements.
Magnitude, Timing and Frequency of these movements are measured.
Differences are accounted for between Body movement and measurments attributed to Gravity.

### run_analysis.R will perform the following tasks:
* Download, unzip and read the original data files.
* Combine the training and testing data sets
* Relable measurement variables
* Label observation rows by activity type and participant ID
* Subset the data files to include only the means and standard deviations (std) of the measurements.
* Summarize each measurement (calculating the mean) for each activity, for each participant (6 activities, 30 participants = 180 rows of measurements)
