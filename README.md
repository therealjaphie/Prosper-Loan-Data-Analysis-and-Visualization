# Prosper Loan Data Exploration
## by Josephine Ochai


## Dataset

The dataset consists of approximately 114,000 records of Prosper loans with 81 attributes 
for each loan including -but not limited to- the loan status, loan original amount, borrower APR 
& interest rate, credit score, employment status of the individuals as well as their income range. 
The dataset can be downloaded [here] (https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv) 
with data dictionary [here] (https://docs.google.com/spreadsheets/d/1gDyi_L4UvIrLTEC6Wri5nbaMmkGmLQBk-Yx3z0XDEtI/edit#gid=0) 
to understand the dataset's variables. For the purpose of my analysis, I wanted to investigate 
what attributes in the data affect loan status; I suspected the following attributes wiould 
have the most impact, so I limited the attributes in the dataset to just these variables and excluded 
all others: Term, BorrowerRate, BorrowerAPR, EmploymentStatus, IsBorrowerHomeowner, CreditScoreRangeLower, 
CreditScoreRangeUpper, IncomeRange, LoanOriginalAmount, MonthlyLoanPayment and Recommendations.


## Summary of Findings

In the exploration, I found that the Loan Status variable had a distribution that showed 
most borrowers had a positive loan status (current or completed) than they were negative i.e 
charged off, defaulted or gone past their due payment date. I also found 
that most people that took loans had an average income range between  25,000− 75,000 and 
were mostly employed. There was a strong relationship between loan status, credit score and 
borrower rates that indicated the borrowers with the highest credit scores and lowest interest 
& annual percentage rates were those who had a history of completing loan payments or who still
had a current loan status. These people were mostly employed and owned homes. 
Conversely, borrowers who had defaulted or had their debts charged off or were past due agreed 
payment timelines had low credit scores and high interest rates. Furthermore, more borrowers with 
a 'current' loan status were given higher loan amounts and were mostly homeowners. 
Surprisingly, it was observed that the borrowers that had completed loan payments were issued 
one of the lowest loan amounts and more homeowners had a 'defaulted' loan status than those
who did not own a home. 

Outside of the main variable of interest, I ascertained a strong positive relationship
between BorrowerRate & BorrowerAPR and; an increase in borrower's interest rate led to a 
corresponding increase in the BorrowerAPR.
Also, credit score was mostly negatively correlated with the borrower's interest rate which was
within reason that Prosper might want to reward/entice those individuals with reputable financial 
status evident from their high credit scores with low interest rates to encourage loan requests with 
a reduced financial risk on their end. There were some exceptions to this rule and upon further 
analysis, it was observed that Prosper majorly issued low interest rate loans to borrowers with low credit 
scores who had loan status of either 'completed', 'defaulted' or 'chaarged off'.
Another interesting observation among the features was the fact that unemployed people earning $0
surprisingly had very high credit scores, though, their corresponding borrower APR and interest rates 
were amongst the highest. These individuals might be explained as those who probably did not work regular 
jobs and did not have a steady source of income but had built high credit scores overtime. However, 
Prosper was likely to grant them loans with higher interest rates in order to protect themselves
in cases of loan defaults.
Lastly, there was a reasonable increase in the credit scores of homeowners across all categorical levels 
of loan status more than those who did not have homes indicating that owning properties generally tends 
to improve one's credit score to a significant level.


## Key Insights for Presentation

For the presentation, I majorly focus on the influence of credit score and borrower interest rates 
on the loan status and on each other. I also illustrate how being a homeowner can affect one's 
credit score. I start by introducing the loan status, credit score and borrower rate variables, then
I present a scatterplot that shows the correlation between credit score and borrower rate. Next, I
zoom in on plots that show the exceptional cases where credit score is not negatively correlated with
the interest rate. I do this by filtering the master dataframe to create other dataframes where only
the category of interest of loan status is present and then I plot separate scatterplots of credit 
score vs borrower rate for each category.
Afterwards, I depict the relationship existing both credit score & borrower rate and loan 
status using violin plots.  Lastly, I use point plots to show the variability in the credit scores 
of homeowners vs non-homeowners across all levels of loan status. 