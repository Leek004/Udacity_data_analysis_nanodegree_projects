# Exploration of the Loan prosper dataset
## by Abdulmaleek Mubaraq


## Dataset


> The dataset used for this exploration was one of the compiled datasets provided by udacity for the 3rd project of the data analysis nanodegree. It contains data about 113939 loan listings on 81 columns, between 2005 and 2014. the goal of this exploration was to answer the following questions:

1. Which set of features has the most highest listings in the dataset
2. Which of these features has the highest average loan amount
3. Which features has the most charge off rate

## Summary of Findings


#### Findings from the exploration are as follows
> About 50% of the loans are current running loans, about 33% are completed and 10% were charged off. Less than 10% are past due or cancelled. Most of the loan listings are for debt consolidation; between lower credit score range amounts of 600 and 800 and an income range of 25000 and 75000; and a monthly revolving payment amount less than 1000. The listings are split almost evenly between home owners and non home owners who are mostly not in a group and have a verifiable income.<br>
Income range '25k-50k' which has the highest number of loan listings and highest average loan amount, and also has the highest chargeoff rate.<br><br>
Listing categories with the highest number of loan listings didnt have the higest charge off rate but those with relatively smaller listings including 'green loan', 'household expenses' and 'medical/dental'. The number off charged off loans in the dataset is only about 10% of the data and 23% for non current loans(charged off and completed)<br><br>
High amount loans (25k+) are scarce in the dataset and are found only at points where features like income range, credit score open revolving payment and employment status duration are at their highest values

## Key Insights for Presentation

> Employment status duration increases both income range and lower credit score which increases number of high loan amount
ths will be shown with a barplot demonstrating how average employment status duration increases with income range, Then a facet grid of how higher employmet status duration(400 and above) has more distribution at points where income range and credit score is high and then  a facet grid demonstrating how number of high amount loans increased at high income range and high lower credit score point.
>  High number of open credit lines and open revolving accounts reduces the number of loan listings. This might be because high number of credit lines and revolving accounts are associated with listings with high income and revolving monthly payment amount. This two features leads to higher loan amounts which is scarce in the datatset
> Listing categories 'green loan', 'household expenses' and 'medical/dental'; and  income range 25,000-49,999  had the highest chargeoff rate



