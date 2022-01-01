# Kickstarting with Excel

## Overview of Project

### Purpose
Louise, who is a playwrite, would like to start a crowdfunding campaign for her play Fever. Her current budget estimate is over $10,000. 
Louise is looking for information on what makes a crowfunding campaign in the play category successful (successful defined as crowdfunding campaigns that met or exceeded their fundraising goal), so that she can mirror the elements that seemed to contribute to the success. 
This requires the examination of a large dataset with information about many crowdfunding campaigns of varying degrees of success.


## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
The first piece of analysis looked at launch dates, particularly the months successful **theater** campaings were launched. This was done by creating a pivot table as formated in the following image: 
![Theater Outcomes by Launch Date Pivot Table](https://github.com/baileyvo/kickstarter-analysis/blob/main/Resources/Analysis_Launch_Dates.PNG)

The pivot table was then used to generate a pivot chart, to visualize the results of the analysis:
![Theater Outcomes Based on Launch Date Chart](https://github.com/baileyvo/kickstarter-analysis/blob/main/Resources/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals
The second piece of analysis looked at goals, and the number of successful, failed, and canceled **play** crowdfunding campaigns. This was done by using the Excel formula "COUNTIFS" to count the number of plays in each of the aforementioned categories in groups of $5000. 
For example, to find the number of **successful** crowdfunding campaigns with a funding goal of **$1000 to $4999**, the following formula was used in Excel: **=COUNTIFS(Kickstarter!$F:$F,"successful",Kickstarter!$D:$D,">=1000",Kickstarter!$D:$D,"<5000",Kickstarter!$R:$R,"plays")**

From there, the sum of successful, failed, and canceled campaigns was calculated using the SUM formula, and then the percentage of successful, failed, and canceled campaigns were calculated. These percentages were used to generate the following line chart:
![Outcomes Based on Goal](https://github.com/baileyvo/kickstarter-analysis/blob/main/Resources/Outcomes_vs_Goals.png)

### Challenges and Difficulties Encountered
One difficultly came in the Analysis of Outcomes Based on Goals, in that a fair amount of manual work was required writing the formulas. I overcame this by coping my formulas using CTRL+C, changing the values, but using the $ sign to lock in reference ranges. 


## Results

- Two conclusions can be drawn about the Theater Outcomes by Launch Date:
	-May has the most campaign launches, and thus has the most successful and most failed launchs. However, proportionally more launches are successful than other months. May would be the best month to lauch her campaign.
	-December had the fewest number of successful campaign launches, and had an almost equal amount of failed. 

- With a current budget estimate of over $10,000, Louise needs a goal of at least $10,000. Campaigns with a goal of **$35,000 to $39,999** or **$40,000 to $44,999** saw the largest percentage of successful campaigns, at 67% successful for both. Campaigns in her range, **$10,000 to $14,999** were 54% successful and 46% failed, so if goals are determining success, she may want to choose a higher goal. 

- There were a few limitations with this dataset:
1. There was no data about actual costs associated with the campaigns, therefore it is difficult to make a recommendation about what goal to set to meet actual costs.
2. The currencies varied from item to item, therefore comparisons may not have been accurate. 

- Other analysis could have been completed by creating other tables and graphs, such as:
1. Doing the same analysis as above, but only using campaigns in Louise's country. 
2. Looking at number of backers and average donation amount to see if any trends could be uncovered.
3. Seeing if trends changed from year to year.
4. Calculating the length in days of campaigns, and graphing successful vs. failed. vs. canceled campaigns by length. 