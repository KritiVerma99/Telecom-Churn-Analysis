# Telecom-Churn-Analysis
TEAM_MEMBERS:


Siddhant Gupta

Swasti Baghel

Shubh Rastogi

Kriti Verma


OVERVIEW:


The telecommunication industries within the sector of information and communication technology is made up of all telecommunications/telephone companies and internet service providers and plays the crucial role in the evolution of mobile communications and the information society. 
With the rapid development of telecommunication industry, the service providers are inclined more towards expansion of the subscriber base. To meet the need of surviving in the competitive environment, the retention of existing customers has become a huge challenge. 
In the survey done in the Telecom industry, it is stated that the cost of acquiring a new customer is far more that retaining the existing one. Therefore, by collecting knowledge from the telecom industries can help in predicting the association of the customers as whether or not they will leave the company.


PROBLEM_STATEMENT:


To build a Vanilla Classification Model on 'Churn dataset of a Telecom Company' to predict Telecom churns and to identify the factors influencing churn in the telecom company. 


DOMAIN: MACHINE LEARNING 


DISCUSSIONS: 


Meeting 01 - Jun 01,2021:

Ques: How are dealing null values for variables having more that 70% of data missing?

Ans:

Understanding : In the type of data set we are using i.e Churn data set, dropping variables because of having high null data points will not be a right thing to do because there could be a logical reason behind it . Since we are seeing telecom data set for Churn, null values for different variable for a particular customer could mean that the customer has stopped using the services of the telecom operator in a particular month and hence the data points for subsequent months is missing.

Action: We had 166/226 columns with null values present. We have replaced all null values for the given variables with '0' except for the data_of_last_rech column for each month, where the null values have been replaced by the mode of that particular months having 'Churn' as 1 rest 0.

Ques: How to identify customer as 'Churn' or 'Non-Churn'?

Ans:
Understanding: The data given is for 4 months i.e June, July, August and September. A customer of telecom company will be considered under 'Churn' if he/she is seen to be inactive in the last two months i.e August and September. We have observed that some customers shows a trend of being active in alternate months hence we have not considered anyone under 'Churn' for only one month of inactivity and taken the criteria of two consecutive months of inactivity to be sure that the person wouldn't come back.

Action: We constructed columns of 'active_month' to find customers who are active in different months based on the totals of their outgoing data, incoming data and data usage for each month. Using the columns of 'active_month', we then have calculated our Churn values as 1 or 0 based on the condition on inactiveness in last two months.




