# An Analysis of Kickstarter Campaigns
Performing analysis on Kickstarter data to uncover trends
# Kickstarting with Excel

## Overview of Project

### Purpose

The purpose of the project is to understand Kickstarter funding for theater plays in an 8 year span.

## Analysis and Challenges
Data was collected and then filtered to focus on funding for theater specifically, plays. Two charts were created:

### Analysis of Outcomes Based on Launch Date

1. Success, failure, and cancelation rate based on their launch date.

The launch date was recorded in excel as a timestamp and "=(((J2/60)/60)/24)+DATE(1970,1,1)" was used to convert it to the MM/DD/YY format. The "Year()" function was then used to capture the year only.

The "pivot table" was used to plot the number of successful, failed and canceled campaigns against the month funding was launched.

![Outcomes_vs_Goals.png](/Users/hueso/Desktop/Data Science/Analysis Projects/Crowd Funding Analysis/Resources/Outcomes_vs_Goals.png)

### Analysis of Outcomes Based on Goals

2.Success, failure and cancellation rate based on 12 different goal brackets.

The countifs() function was used to report the number of successful, failed, and canceled funding campaigns in different goal brackets.

![Theater_Outcomes_vs_Launch.png](/Users/hueso/Desktop/Data Science/Analysis Projects/Crowd Funding Analysis/Resources/Theater_Outcomes_vs_Launch.png)

### Challenges and Difficulties Encountered

The data collected also captured a "live" category under outcomes which was displayed in the chart and the table. It was unclear if this was to be included or omitted from the chart as there were no instructions to filter it out but the examples of how the chart should look like did not include the "live" data. After going through all the modules, I decided to click on the filter button above the "successful" table header which is not all that intuitive as it is directly above one column not all column labels.

When using the countifs() function, I did not realize there was also a countif() function and I simply clicked on the first result which happened to be the incorrect function. It was not a big issue since I was able to notice there were two similar formulas before moving on to the next cell, however, such a small difference in the formula could have led to a bigger issue.

The biggest challenge encountered was understanding how to use the countifs() formula for this particular analysis. At one point, the input in the formula seemed correct but the chart did not look accurate. To overcome this challenge, I stepped away for a few minutes, relaxed, reread the requirements, and deleted everything to start from scratch.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
Funding is most successful when funding starts during the second quarter of year.
Funding is most unsuccessful in December.

- What can you conclude about the Outcomes based on Goals?
Funding Campaigns with goals less than $1000 are most successful.

- What are some limitations of this dataset?
The data collected is informative yet limited only to funds. The data collected does not include how much effort was put into outreach. If social media was used to promote the campaigns, knowing how many platforms were used, would add more value. Additionally, incentives offered by creators to the backers is not disclosed. We cannot be certain that the timing of the campaign launch date is directly correlated to success because it's possible that creators were able to provide incentives to their backers. It is also possible that the genre of the plays were more fitting for the season of the launch date.

- What are some other possible tables and/or graphs that we could create?

Most successful/unsuccessful Goals vs most successful/unsuccessful launch date (month).
Successful, failed, canceled vs total time (deadline - launch date).
Successful campaigns vs Goal brackets (like Outcomes based on Goals, one campaign has a goal of $1.00 and they raised 6500%)



