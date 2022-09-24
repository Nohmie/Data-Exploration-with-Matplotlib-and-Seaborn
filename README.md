# Exploratory Data Visualization

## Dataset

This document explores a dataset containing 113,937 loans with 81 variables on each loan, including details on the loan such as loan amount, loan origination date, estimated returns, borrower rate (or interest rate), current loan status, loan rating; Details on the borrower such as borrowers' occupation, borrowers' income, employment status and many others.
The dataset can be found [here](https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv),
with feature documentation available [here](https://www.google.com/url?q=https://docs.google.com/spreadsheet/ccc?key%3D0AllIqIyvWZdadDd5NTlqZ1pBMHlsUjdrOTZHaVBuSlE%26usp%3Dsharing&sa=D&ust=1554486256024000)

A subset of the original dataframe was created which contains the features of interest as I am most interested in the following

* Factors that affect a loan’s outcome status
* What affects the borrower’s APR or interest rate
* If there are differences between loans depending on how large the original loan amount was
So I will be working with the Loan Status, Borrower APR/Borrower Rate and exploring every other variable likely to affect it


## Summary of Findings

Since the aim of the analysis was to find out the effect of the features of interest on the loan status, I filtered out the current loans and worked with loans that were tagged default and the completed loans. I noticed that both monthly income and debt to income ratio seemed to have a relationship with default as people with higher stated monthly incomes defaulted less often than those with lower incomes, regardless of the size of the loan and loans are more likely to default if the debt to income ratio is higher.

Looking at the several loan categories, the Green loans had the most defaults of about 56.5% while the RV loan accounted for about 11.11% default times which is the least, the default class seemed to have higher rates and after comparing the loan status to the rating, it was noticed that the higher the rating, the less likely there is to be defaults but from the distribution, the frequency of borrowing is highest in loans with a C rating.

After the relationship of borrower rate was checked with other features, It was noticed that the borrower Rate has a large range with each loan amount size but the Borrower Rate decreases with an increase in loan amount which is why there's a negative correlation, there is also a negative correlation between the borrowers' monthly income and the loan rate as the rate decreases with an increase in income.

When the average rates for each term were compared, we saw that as the term increases, the rate increases as well. The 36months term which has the most borrower count has a median rate of about 20%. It was also observed that in 2008-2009 there was a large dip in loan origination after which a slow rise was noticed till it peaked in 2013. After a bit of research, I discovered that it was due to the great recession in 2008-2009 which was as a result of the global financial crisis. A strong positive relationship exists between the term and loan amount i.e longer the term, the larger the loan. I noticed also that most Borrowers are mostly employed with full time employment with monthly income ranging from 50,000 to 100,000+ and are mostly home owners. Their loans are usually within the 36months term and there's a decrease in estimated returns with an increase in salary range which could be as a result of the negative correlation between the rates and monthly stated income as noticed earlier.

After exploration I came to the following conclusions:
* There's a constant high likelihood of defaults with loans in the 60 months term irrespective of the Rating. The likelihood though of a default decreases as the rating progresses and the high risk loans are at a constant 36months term
* The median rates for the completed loans are lower than rates for loans in the default class and it is also noticed that the higher the income range the lower the interest rates
* The interest rate is not dependent on the employment status but the loan outcome is highly dependent on the interest rate. The lower the interest rate, the more likely the loan is to be completed
* The loan outcome is not dependent on the loan amount
* There is a weak negative correlation between the loan amount and the interest rate.

The overall conclusion is that the Loan outcome is highly dependent on the interest rate and doesn't factor in the employment status, occupation or income and the more money people earn, the more money they are likely to borrow.

## Key Insights for Presentation

For the presentation, I will focus on the influence of the features of interest (borrowers rate) on the loan outcome and discover the relationship between the borrowers, the loans they took out and the effect it has on the interest rate. I have introduced the features of interest, how they relate to one another and eventually how they all come together to influence the overall outcome of the loans.