
<p>This file describes the variables, the data, and any transformations or work that I have performed to clean up the data.  </p>

<ul class="task-list">
<li>The site where the data was obtained:<br><a href="http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones">http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones</a><br>
The data for the project:<br><a href="https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip">https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip</a><br>
</li>
<li>The run_analysis.R script performs the following steps to clean the data:<br><ol class="task-list">
<li>Read X_train.txt, y_train.txt and subject_train.txt from the "./UCI HAR Dataset/train" folder and store them in <em>trainData</em>, <em>trainLabel</em> and <em>trainSubject</em> variables respectively.<br>
</li>
<li>Read X_test.txt, y_test.txt and subject_test.txt from the "./UCI HAR Dataset/test" folder and store them in <em>testData</em>, <em>testLabel</em> and <em>testsubject</em> variables respectively.<br>
</li>
<li>Concatenate <em>testData</em> to <em>trainData</em> to generate a 10299x561 data frame, <em>joinData</em>; concatenate <em>testLabel</em> to <em>trainLabel</em> to generate a 10299x1 data frame, <em>joinLabel</em>; concatenate <em>testSubject</em> to <em>trainSubject</em> to generate a 10299x1 data frame, <em>joinSubject</em>.<br>
</li>
<li>Read the features.txt file from the "/UCI HAR Dataset" folder and store the data in a variable called <em>features</em>. We only extract the measurements on the mean and standard deviation. This results in a 66 indices list. We get a subset of <em>joinData</em> with the 66 corresponding columns.<br>
</li>
<li>Clean the column names of the subset. We remove the "()" and "-" symbols in the names, as well as make the first letter of "mean" and "std" a capital letter "M" and "S" respectively.<br>
</li>
<li>Read the activity_labels.txt file from the "./UCI HAR Dataset"" folder and store the data in a variable called <em>activity</em>.<br>
</li>
<li>Clean the activity names in the second column of <em>activity</em>. We first make all names to lower cases. If the name has an underscore between letters, we remove the underscore and capitalize the letter immediately after the underscore.<br>
</li>
<li>Transform the values of <em>joinLabel</em> according to the <em>activity</em> data frame.<br>
</li>
<li>Combine the <em>joinSubject</em>, <em>joinLabel</em> and <em>joinData</em> by column to get a new cleaned 10299x68 data frame, <em>cleanedData</em>. Properly name the first two columns, "subject" and "activity". The "subject" column contains integers that range from 1 to 30 inclusive; the "activity" column contains 6 kinds of activity names; the last 66 columns contain measurements that range from -1 to 1 exclusive.<br>
</li>
<li>Write the <em>cleanedData</em> out to "merged_data.txt" file in current working directory.<br>
</li>
<li>Finally, generate a second independent tidy data set with the average of each measurement for each activity and each subject. We have 30 unique subjects and 6 unique activities, which result in a 180 combinations of the two. Then, for each combination, we calculate the mean of each measurement with the corresponding combination. So, after initializing the <em>result</em> data frame and performing the two for-loops, we get a 180x68 data frame.</li>
<li>Write the <em>result</em> out to "data_with_means.txt" file in current working directory. </li>
</ol>
</li>
</ul>
