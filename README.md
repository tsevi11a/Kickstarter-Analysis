# An Analysis of Kickstarter Campaign

## Overview of Project

This project examines several Kickstarter campaigns to discover trends and identify any factors that may lead to a more successful campaign. 

### Purpose

We will use these insights to garner a better understanding of theatre campaigns and make recommendations for up-and-coming playwrights. More specifically, we will review how different theatre campaigns fared in relation to their launch dates and funding goals. 

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
* As part of our analysis, we looked at the relationship between launch date and campaign outcomes. 
* To do this, we created a pivot table using the Kickstarter data and filtered the parent category to show us the outcomes for “Theatre” campaigns. 
* Using the “Date Created” data, we were able to determine the number of successful, failed and cancelled campaigns for each month of the year. 
* To help visualize the relationship, we used a line chart to display the results (see below):
![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/86018601/124366744-e3dde880-dc1f-11eb-8c03-0eb9b0612be1.png)

### Analysis of Outcomes Based on Goals
* Next, we narrowed in to the “Plays” sub-category and reviewed the different outcomes based on the size of the campaign goals. 
* We first created dollar-amount ranges and then used the COUNTIFS() function to determine the number of successful, failed, and cancelled campaigns within each range.
* We then calculated the percentage of different outcomes for each range by first using the SUM() function to determine the total number of campaigns within each range. 
* The following line chart was created to illustrate the results:
![Outcome_vs_Goals](https://user-images.githubusercontent.com/86018601/124369246-b3a24400-dc37-11eb-876b-e6184851dbbd.png)

### Challenges and Difficulties Encountered
The most challenging part of the analysis was working with the COUNTIF() function, having had to manually adjust the criteria for each range and outcome. Once the first set of formulas for each range under the “Successful” outcome was created, it was copied over to the columns for the other outcomes. Instead of manually amending each formula, the “Find and Replace” tool was used to amend the formula respectively (for example, “successful” to “failed”).
<img width="966" alt="SS_COUNTIFS" src="https://user-images.githubusercontent.com/86018601/124371888-1f92a580-dc54-11eb-8272-f220d69710d4.png">

## Results

- What are two conclusions you can draw about the Outcomes based on Launch     Date?
  - The chart above illustrates the number of successful, failed and cancelled campaigns in relation to the month that they were launched. From this, we can see that the highest volume of campaigns were during the summer months. The highest number successful campaigns was in May and began to decline in June and continued to decline to the end of the year (with the exception of a small spike in October). In contrast, the number of failed campaigns were roughly the same throughout. Based on this, the recommendation would be to launch the campaign during the month of May.

- What can you conclude about the Outcomes based on Goals?
  - The most successful campaigns are those with a goal of $1,000 or less where 76% were successful. This was followed closely by campaigns between $1,000 to $4,999 where 73% were successful. Overall, the as the goal increases, it becomes less likely of being met. One thing to note is that campaigns between $35,000 to $50,000 also have a relatively high percentage of success (67%), however there are a very limited number of campaigns in this range. Based on this, the recommendation would be to be to use Kickstarter for campaigns that are $5,000 or less.

- What are some limitations of this dataset?
  - The data does not provide context to other factors that may have impacted the results, such as the country where the campaign was launched or seasonality. There are also many outliers in the data which can skew the results. 

- What are some other possible tables and/or graphs that we could create?
  - It would be beneficial to also use a box plot to review the distribution of campaign goals to identify any outliers that may be displacing some of our findings. 


