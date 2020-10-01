# Predicting Snapchat Political Advertisement Impressions
## Background
On July 21, 2020, Rachel Kraus published an [article](https://mashable.com/article/snapchat-political-ads-q2-2020-earnings/) on Mashable called _Snapchat hungry for political ads as Twitter, Facebook shy away_. In this article, Kraus elaborates on how Snapchat established their very own specific guidelines to have political advertisements after some of the company's rivals banned or stopped politcal ads, such as TikTok in October of 2019, Twitter within days after TikTok, Google restricting ad targeting demographics for political ads, and Facebook having some controversial methods of displaying political ads that inclues some false or misleading information. Unlike Facebook, "Snap does fact check political ads" and Jeremi Gorman, Snapchat's chief business officer, mentions that they have "very specific guidelines". As the presidential election is coming our way in a few months, can we predict the impressions that these ads created during a full year? Which factors can contribute to help predict the impressions of that year? We will delve more into the data provided by [Snapchat](https://www.snap.com/en-US/political-ads/) to further analyze the significant variables (spend, days of advertisement, and most common organization) to create a regression to ultimately predict the number of impressions that political ads formed during the years of 2020, 2019, and 2018.
## Business Question
_Can we predict the number of impressions for an advertisement for any year with the variables of dollars spent, days of advertisement, and the most common organization?_
## Data Question - Open Data
We'll use open data from one source:
- Snapchat: This research group constructs [publically open data "to find out details about all political and advocacy advertising running on our platform".](https://www.snap.com/en-US/political-ads/) We will be creating multiple linear regressions:
    
    i. 2020: Original open data on political advertisements in the year 2020.
    
    ii. 2019: Original open data on political advertisements in the year 2019.
    
    iii. 2018: Original open data on political advertisements in the year 2018.
## Data Question - Analysis
We will use Microsoft Excel to answer these questions:

- __How does the regression for the number of impressions from political ads in the year 2020 look like?__ Creating a multiple linear regression to predict the number of impressions with variables of spend, days, and the most common organization.

- __How does the regression for the number of impressions from political ads in the year 2019 look like?__ Creating a multiple linear regression to predict the number of impressions with variables of spend, days, and the most common organization.

- __How does the regression for the number of impressions from political ads in the year 2018 look like?__ Creating a multiple linear regression to predict the number of impressions with variables of spend, days, and the most common organization.

## Data Answer

### How does the regression for the number of impressions from political ads in the year 2020 look like?
__2020 Regression 1__
![alt text](https://github.com/schoi74/Snapchat-Politcal-Ads-Impressions/blob/master/2020%20regression%201.png)

Here we can see that the R^2 value is pretty high with 0.7002041, Significance F value of 0, and p-values low enough for each variable except for _ACRONYM?_. As ACRONYM was the most common organization that had the political ads, I performed the regression data analysis for ACRONYM. However, the p-value for this variable too high of 0.4018296, meaning it is not significant in the regression. Therefore, I performed the regression with the next most common organization, Assembly. 

__2020 Regression 2__
![alt text](https://github.com/schoi74/Snapchat-Politcal-Ads-Impressions/blob/master/2020%20regression%202.png)

Here, the R^2 value increases a little bit to 0.70343838 from 0.7002041, Significance F value stays the same as 0, and the p-values for all the variables and the intercept are way below 0.001. As that of the variable "Spend" is 0 on the table, we can assume it is less than 0.001 and determine as significant to the regression model. 

Thus, the final multiple linear regression equation is:

__Impressions = -299145.42 + 427.141777*(Spend) + 2608.88975*(Days_of_Ads) + 1384066.01*(Assembly?)__

### How does the regression for the number of impressions from political ads in the year 2019 look like?
__2019 Regression 1__
![alt text](https://github.com/schoi74/Snapchat-Politcal-Ads-Impressions/blob/master/2019%20regression%201.png)

Here, we first notice that all the p-values are high, meaning the variables are insignificant. The R^2 value is 0.71017584, which is higher than that of the regression model for the year 2020 and the Significance F value is also 0, meaning these variables contribute to the final regression model. However, as these p-values are too high and insignificant, I wanted to rerun the analysis by setting the second most common organization name, _the Aber Group_ as the variable, just like how I did for the year 2020 to see if I can get a better correlation and significance of these variables.

__2019 Regression 2__
![alt text](https://github.com/schoi74/Snapchat-Politcal-Ads-Impressions/blob/master/2019%20regression%202.png)

After rerunning the data analysis, you can notice that the R^2 value decreases a little bit to 0.71007518 from 0.71017584, but the Significance F value stays at 0. However, the p-values for the variables, _Days_of_Ads_ and _UnRestrict_Minnesota_ increases by a significant amount, making these variables less significant.

Thus, the final multiple linear regression equation is:

__Impressions = 138485.082 + 340.626168*(Spend) + 661.869532*(Days_of_Ads) - 200594.96*(UnRestrict_Minnesota?)__

Even though this regression model is not the best equation to use to predict the number of impressions of political ads for the year 2019, we can safely assume that it will predict the number of impressions with a bigger margin of error.

### How does the regression for the number of impressions from political ads in the year 2018 look like?
__2018 Regression__
![alt text](https://github.com/schoi74/Snapchat-Politcal-Ads-Impressions/blob/master/2018%20regression.png)

Here, we first notice how the R^2 value for this regression model is lower than the previous two with the value of 0.63742605. However, when analyzing the p-values of the individual variables, the values are all lower than 0.001 except for that of the intercept. As the three variables (Spend, Days_of_Ads, and Bully_Pulpit_Interactive?) are all extremely small numerical values that mean significance of them in the regression model, we can safely assume that these variables are significant enough. Even though the p-value of the intercept is 0.03877166 and can increase the margin of error of the regression equation, it is close enough to 0.001 to determine it as significant as it is only the intercept. We can also notice that the Significance F value for the year 2018 is not 0, but 8.2326E-144. However, as it is such a miniscule number, we can safely assume it is 0 and that the variables contribute to the final regression equation adequately. 

Thus, the final multiple linear regression equation is:

__Impressions = -72466.73 + 348.426633*(Spend) + 4438.44254*(Days_of_Ads) - 290379.41*(Bully_Pulpit_Interactive?)__

## Summary
## Stey-by-Step Excel Analysis
