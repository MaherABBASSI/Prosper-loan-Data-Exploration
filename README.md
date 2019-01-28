# Prosper Loan Data Exploration

## Dataset

Prosper is the first peer-to-peer American lending marketplace, with more than 2 million members and over two billion dollars in funded loans. The data set available to the public (last updated on March 11th, 2014) contains 113,937 loans with 81 variables on each loan, including loan amount, borrower rate (or interest rate), current loan status, borrower income, and many others.
The dataset is available [here](https://www.google.com/url?q=https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv&sa=D&ust=1545823012093000),
with feature documentation available [here](https://www.google.com/url?q=https://docs.google.com/spreadsheet/ccc?key%3D0AllIqIyvWZdadDd5NTlqZ1pBMHlsUjdrOTZHaVBuSlE%26usp%3Dsharing&sa=D&ust=1545823012094000).


## Summary of Findings

In the exploratory data analysis, we first started by looking at the main 
features (income range, the loan original amount, debt to income ratio, 
prosper score)that we expected to most influential regarding Borrower APR and
loan outcome. 

Then we performed a bivariate exploration by looking closer to 
the pairwise correlations present between features in the data.And we found 
that there is a moderate negative correlation between borrower APR and Prosper
score and between borrower APR and LoanOriginalAmount.
By plotting a pairgrid of numerical features according to categorical features
we discovered that The Income range is positively correlated to Prosper score
and Loan Original Amount, the debt to income ration is negatively correlated to
the income range.
For the loan status, defaulted and past due status showed higher borrower APR.
finally, homeowners have higher employment duration, higher loans and Credit 
Score but lower borrower APR.
At the end of bivariate, we focused on the relationships between the categorical
features which showed that Borrower with Income range between 25 k and 75k are 
the biggest borrowers in all categories especially for loan consolidation.

For the Multivariate exploration and given the high number of features we 
decided to focus only on how categorical features like 'IncomeRange',
'EmploymentStatus', 'IsBorrowerHomeowner', 'LoanStatus' and 'ListingCategory'
interact with 'BorrowerAPR', 'ProsperScore' and 'DebtToIncomeRatio',
'LoanOriginalAmount'. We highlited some interesting findings such as the fact
that Higher BorrowerAPR with lower ProsperScore results in higher probability
of Past due Loans. However, lower BorrowerAPR with higher ProsperScore results
in lower probability of Past due Loans...



## Key Insights for Presentation

For the presentation, we tried to answer the question:
- What factors affect a loan’s outcome status?
- What affects the borrower’s APR or interest rate?

We decided to focus on the influence of the main features, namely, the income 
range, the loan original amount, debt to income ratio, prosper score, that we 
expected to have the strongest effect on the the borrower APR and the loan 
outcome status.

We've introduced them one by one by plotting their distribution and the box plot
to show if there are outliers that could affect our findings. Then, we emphasized
the paired interactions between Borrower APR and consecutively Prosper Score,
Loan Original Amount and Loan Status.
For the loan's outcome, we've plotted the Loan Status distribution highlighting 
the Income Range and the HomeOwners categries.

To go deeper in the exploration, we used the pointplot to cast the interaction 
between the borrower, the Income Range and the Loan Status at the same time. 
Likewise for the Loan Original Amount by Loan Status and Home owner.
