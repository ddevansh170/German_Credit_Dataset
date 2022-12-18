Executive summary

Problem statement

In banks, loan default happens when the customer is unable to repay the loan within desired time with the interest. Loan Default prediction is the process of using data to identify which customers are likely to default the loan in the future. This is important for banks because banks suffer from massive capital losses when customers are unable to repay the loan amount. Loan Default Prediction can help banks focus on identifying customers who are likely to default the loan. The German Credit project is conducted to respond to the statement “Which existing or new customers are likely to default the loans ? ".

Exploratory Data Analysis and Insights

The dataset contains 1000 customers and 21 features, in which Default is the dependent variable. The Default value is binary with 1 is Default, representing the customer default the loan and 0 is Not Default, representing the customer didn’t default the loan. The Default accounts for 30%, while the Non Default makes up 70% in the dataset. 

There are very few outliers in age [23 outliers], amount  [72 outliers] and duration [70 outliers]. 
The customer profile of outliers in these variables was studied and almost the equal number of customers, default for each of these 3 variables, Hence these outliers were treated using the Quantile based flooring method.
In this approach, the outliers greater than the upper limit(Q3 +1.5*IQR) are masked with 100th percentile value. The outliers lesser lower limit (Q1 -1.5*IQR) are masked with 0th percentile value.

INSIGHTS

➢	 The best model for German Credit Default prediction is Logistics Regression with an accuracy score of 77.33 %.
➢	 Around 50 % of customers, having a checking status of less than 0 DM default the loan.
➢	 Customers with Credit History of A30 (no credits taken/ all credits paid back duly) and A31 (all credits at this bank paid back duly) have higher percentage of default than non default. So any customer with these credit histories should be closely monitored.
➢	 Majority of the customers take out loans for buying used cars, furniture/equipment or radio/television. Customers who have taken out a loan for buying a new car, education or business have more than 30 % probability to default.
➢	 Out of all the customers who have employment history of either less than 1 year or are unemployed. There is around a 35 % probability that they would default. 33 % of the customers who take loans have work ex of 1 to 4 years.
➢	 50 % of the people who take out loans are Single males. Males or females who are divorced/ separated have the highest likelihood to default loan.
➢	 People who don't know property or their property status is unknown have 43 % probability that they would default on the loan.
➢	 Around 70 % of the people who take out loans own a house and 40 % of the people who live for free default the loan.


Modeling

➢	Decision Tree, Random Forest, Logistics Regression, and Linear Regression are preferred tools for this problem. Model performance will be conducted using Accuracy, Sensitivity, Specificity, Precision and F1-score.
➢	For the purpose of this problem, the model is expected to identify as many customers who are likely to Churn as possible. Hence, Sensitivity which measures the ratio between how much are correctly identified as churn to how much are actually churn, is set to be the main measure.
Model Performance
●  	Decision Tree provides the best insight into the features used by the algorithm to split the tree. It has the highest sensitivity among all the algorithms  96.74 %, i.e. out of 100 actual default customers, 96 were predicted correctly as default. Also the accuracy for the train and test data are immersive with values of 65 % and 98.33 % respectively. This is the best model for predicting credit default.
●  	Random Forest performance is poorer than Decision tree. Having the highest specificity value for the train and test data. Also it has the highest precision among all models. But the sensitivity is extremely poor: 2.4 % for train data and 35.87 % for test data, this is the reason it wasn’t considered the best model.
●  	The Logistics Regression model yields the relatively good result across Accuracy, Sensitivity, and Specificity in both train and test data. Logistic regression has a good accuracy score of 67 % for train data and 65 % for test data. The statistical results produced by this model are relatively consistent with the descriptive analysis.
 
Decision Tree will be the chosen model for implementation as it yields the highest Sensitivity and great insights into feature significance.

Recommendations

Based on the outcomes produced by the Decision Tree model, the management team is recommended to consider a number of approaches to manage customers with high likelihood of default loan, which include:
➢ The credit history of the individual  and commercial credit history should be properly analyzed from past data before lending a loan.
➢	The banks should collect collateral to secure a loan like a house, so that the bank may seize that property if the customer fails to make proper payments on the loan.
➢	Myriad pieces of loan documentation that includes business and personal financial statements, income tax returns, a business plan and that essentially sums up and provides evidence for the credit history, Cash flow history and projections for the business, Collateral available to secure the loan and character.
➢	When reviewing the loan application, banks should consider how much experience the customer has. If he owned his business for years and has managed his company’s finances responsibly, then the loan could be granted. However, if he has recently opened his business or has struggled financially, this could be detrimental.
➢	Customers with an age group of 20 to 40, loan amount greater than 7000 Cr or should be very carefully monitored before giving loans, as according to the analysis these people default the most.
