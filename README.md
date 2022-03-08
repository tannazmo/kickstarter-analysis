# An Analysis of Kickstarter Campaigns

## Overview of Project
Louise, a playwright, would like to start a crowdfunding campaign to fund her play FEVER. 

So, we will be performing analysis on Kickstarter data to uncover trends by extracting useful data from the raw dataset for helping Louise making an informed decision on how to run her fundraising campaign to increase the likelihood of being successfully funded and setting her up for success by helping her see what other crowdfunding campaigns have done, that might have been a factor in their project having succeeded or failed.

## Analysis and Challenges
From the raw data set, we first looked at the Goal and Pledged dollar amount for all campaigns to see what percentage of the goal amount was raised for each campaign. we did that by dividing the pledged amount by the goal amount (PLEDGED/GOAL)% to show it better we also rounded the results to whole numbers.

 =ROUND(pledged/goal*100,0)

Also looked at the average donation for each campaign, to do so the whole pledged amount for each campaign was divided by the number of backers for that campaign.

=Pledged/Backers

One of the **challenges** we encountered was that since in our data set the Category and Subcategory were shown together. So, to be able to focus on the related industry and its subcategories, Category and Subcategory were separated into two columns by using the *Text to Columns* feature, then filtered out all unrelated campaigns to only look at what Theatre and Play subcategories were doing in their crowdfunding campaign. 

We also wanted to know for how long these campaigns were running to reach their goals. So, we looked at the 'Date Created' and 'Date Ended' for each campaign. Here the **challenge** we faced was that the dates were shown in a different format (Unix format), therefore they were incomprehensible, so we had to convert the dates. We overcame this challenge by using the formula:

=([Date shown in the field]/60/60/24)+DATE(1970,1,1)

Date (in seconds) divided by 60 to get the number of minutes, divided by 60 again to get the number of hours and then divided by 24 to get the number of days, we then added the beginning point for the UNIX date showing system which is 1970/1/1

### Data Visualization

Now that we have a data set that we can turn into tables and charts with meaningful and useful information, we used Pivot Tables and Charts.

For this we thought it would be useful for Louise to know if time of year, e.g., month could be factor in the outcome of the challenge. 
So, we created a table and chart showing the outcomes of the Theatres based on their launch date, more specifically, the month they launched.

![Theatre_Outcomes_vs_Launch](/resources/Theatre_Outcomes_vs_Launch.png "Theatre Outcomes Based on Launch Date")
 
Another analysis we thought is useful is looking at the goal amount to determine if what campaigns were more successful or had failed considering their goal amounts.
So, we created a table and chart showing the outcomes based on the goal's dollar amount. to better show this, since the goals could vary by a little or a lot, we used the ranges of goals, e.g., less than $1000, between $1000 and $5000, etc., to see what percentage of the campaigns have succeeded or failed or cancelled.  

![Outcomes_vs_Goals](/resources/Outcomes_vs_Goals.png "Outcomes Based on Goals")


## Results

### What are two conclusions you can draw about the Theater Outcomes by Launch Date?


By looking at the Theater Outcomes by Launch Date charts we have created, we could show that:

1) Numbers of successful campaigns launched in May is the highest and as it goes to June and July, the numbers go down, but not quite as low as the month of December which shows that May, June and July may be the preferred months to launch a successful campaign while May shows to be the best of all.

2) In December the number of successful campaigns is almost the same as failed campaigns (the line showing successful campaigns and the line showing failed campaigns are almost touching), so it could be one of the worst months to launch a campaign.

3) In October there was a jump in the number of failed campaigns.

### What can you conclude about the Outcomes based on Goals?
By looking at the Outcomes Based on Goals chart, we can say that:

1) For campaigns with goals under $30K, the number of successful campaigns decline as the goal increases. 

2) Campaigns with goals in the range of 5K-10K have a similar chance of succeeding, to campaigns with goals in the range of 10K-15K. And since Louise's goal was about 10K, she would not decrease or increase her chances of running a successful campaign by changing her goal by about 5K, so there is no point in lowering her goal, also it wouldn't hurt much if she decided to increase her goal a by that margin.

### What are some limitations of this dataset?
Some limitation of this data set we can think of, is that it does not give statistics by state, so while Louise can get the information based on countries, she cannot find out how the campaigns are funded in the State where she wants her play performed. 
Also, if there was another level of subcategories for the genre of the plays, she could probably get a more focused chart to her help visualise. 

### What are some other possible tables and/or graphs that we could create?

We could filter the dataset by the country and create a table and chart.
We could also look at how long the successful campaigns were based on their goal.


### Dataset used:
To create more views, you also have access to the main data Excel file by clicking [here](/Kickstarter_Challenge.xlsx "download the EXCEL file").
