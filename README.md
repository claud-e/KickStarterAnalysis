# Kickstarting with Excel

## Overview of Project

Louise is trying to fund her play _Fever_ through the Kickstarter platform, and has asked us to analyze the data from 4113 projects that have been published to Kickstarter to try and find trends, insights and best practices to make her campaign successful.

### Purpose

To make a campaign that will successfully reach its 10,000.00 USD goal by looking specifically at launch dates and plea ammounts, as well as their relationships with the outcomes for each project. 

## Analysis and Challenges

The analysis starts by combing through the data and verifiyng its integrity and quality. In this case it is assumed that the data had no problems on this front.

A few calculations and extra columns were added, namely _Average donation_ and _Percentage funded_, more importantly and relevant for this analysis the columns _Date created conversion_, _Date ended conversion_ and _Subcategory_ were added.

### Analysis of Outcomes Based on Launch Date

For this analysis a pivot table was created using the _Date created conversion_ column for rows, and the _Outcomes_ column for columns, _Years_ and _Parent category_ for filters. The associated line chart is as follows:    ![Theater Outcomes Based on Launch](https://github.com/claud-e/KickStarterAnalysis/blob/main/resources/Theater_Outcomes_vs_Launch.png) 

May and june show a notable spike of successful campaigns, which could be an indication of a good moment to launch a campaign. On the same note, it is important to note that failed and cancelled campaigns do not increase in a significant way, which might indicate a correlation between the month and the success independent from a simple overall increase in campaigns.

Winter in general seems to be a bad time to launch a campaign since the number of successful campaigns decrease significantly, although in this case the overall number of campaigns decrease as well and it seems like a statistically significant dip is happening. Unfortunately at the time of writing I'm unaware of an appropriate test to prove this question.

### Analysis of Outcomes Based on Goals

This analysis is performed by creating a table using the function CountIfs() to pull _plays_ based on their outcomes and the ranges of their goals. Once the information is organized, the calculated percentages are graphed as follows: ![Outcomes Based on Goal](https://github.com/claud-e/KickStarterAnalysis/blob/main/resources/Outcomes_vs_Goals.png) 

The resulting analysis shows that the lower the goal, the more likely it is for a campaign to be successful. This negative correlation continues until the range of 35K to 45K, where the number of successful campaigns spike again before plummeting again. 

### Challenges and Difficulties Encountered

One challenge is the need for specificity and attention to detail that comes with programming in general. I found several instances of formulas not working because of a missplaced comma or a missing parenthesis.

Another challenge is the use and navigation of tools I am unfamiliar with, in this case markdown and github have occupied a good portion of the time I allocated to this project.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

1. May and june seem to be the best months to launch a campaign.
2. Failed campaigns seem to be independent from their launch dates.

- What can you conclude about the Outcomes based on Goals?

1. Lower goals might be easier to fund, but there are other variables affecting the decisions of backers since there is a lot of room for high-cost projects to be funded as well.

- What are some limitations of this dataset?

1. Most of the campaigns have happened in the US, it would be interesting to see similar analysis performed on other countries.
2. The necessity to transform several of the columns to make them usable seems like an avoidable step.
3. More specific data regarding the location of backers and campaigns would be useful to determine the best places to make campaigns.

- What are some other possible tables and/or graphs that we could create?

1. We could look at the correlation between _staff pick_ and _outcome_  or _Spotlight_ and _Outcome_ using a stacked column chart or a line chart since it is possible this will boost a project. If that is the case, looking at what factors make the staff pick a project would benefit us.
