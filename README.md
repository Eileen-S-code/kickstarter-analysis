# Kickstarting with Excel

## Overview of Project
- Louise created a kickstarter campaign for her play Fever, which came close to her goal in a short amount of time. 
### Purpose
- She wants to see how other plays did on kickstarter based on their launch date and funding goals.


## Analysis and Challenges
### Analysis of Outcomes Based on Launch Date
- In order to analyze theater goals by launch date a pivot table was created. 
- The filters were years and parent category. 
- The rows were based on the date created and filtered for month only.
- The count of outcomes for successful, failed and canceled projects were displayed in the columns.
- Then a line graph was created to display the results.
### Analysis of Outcomes Based on Goals
- To perform the analysis on outcomes based on goals the =Countifs() function was used.
- For example when determining the number of successful plays with a goal of 5000 to 9999 the following code was used 
- =COUNTIFS(Kickstarter!$F:$F, "successful",Kickstarter!$R:$R, "plays",Kickstarter!$D:$D, ">=5000",Kickstarter!$D:$D, "<=9999")
- The value of the goals and the outcome for the play were updated accordingly per criteria.
- To find the percentage successful, failed, and canceled per each funding category the SUM() of the all the played was found.
- Then each category (successful, failed, and canceled) were divide by the total number of projects and multiplied by 100.
- Finally for visual analysis a line graph of each was created. 

### Challenges
- At first I thought filtering the data sheet for plays would change the COUNTIFS function output. When it did not I realized that I needed to add another criteria in the function to filter for plays. 

## Results
- Based on launch date one can conclude that most successful plays are started in May and the least successful are launched in December.
- Campaigns with high monetary goals are more likely to fail, unless they are in the range of 35000 to 44999.
- While the dataset is useful the monetary parameters were not converted to a standard amount across countries therefore comparing goals, pledges, and average donations across countries is not useful., Some additional graphs that could be useful is one that graphs successes based on country once a common currency is calculated. Another table and graph combination that could be useful would be to compare successful and failed plays based on the number of backers and the average donation.
