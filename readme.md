# (Prosper Loan Data Exploration)
## by (Mohamed Elmofty)


## Dataset

The dataset includes 113,937 rows (loan), 81 variables. Most of the columns are numeric, also there are some date/time columns. BorrowerAPR, BorrowerRate and DebtToIncomeRatio denote percentages and are represneted by decimals. There are also some ordered categorical variables like CreditGrade ProsperRating(Alpha). The ProsperRating is also represented with a numeric equivalent (0 - 7). ProsperScore that determines a risk score(1 - 10) for the loan.

The CreditGrade scale: NC, HR, E, D, C, B, A, AA The ProsperRating (Alpha) scale : N/A, HR, E, D, C, B, A, AA Both have simillar ratings


## Summary of Findings

First impressions were that the various different credit risk scores associated with each loan and income/debt related features would be the most suitable in this analysis. My initial intuition was correct and the majority of the features chosen were correlated with the interest rate columns, with ProsperRating (Alpha) or it's numeric variant ProsperRating (numeric) being highly correlated.

The others weren't as correlated, and I looked deeper into why the proprietary ProsperScore wasn't as correlated and turned out that when looking at multivariate relationships that the values for the ProsperScore column were distributed acorss all levels of the ProsperRating(s). What this means is that a loan with a low/wrose ProsperRating could have a good/high ProsperScore and vice-versa. This implies that other criteria not explored in the analysis are used to determine the ProsperScore and it would be a good place for future anaylsis to begin.

Another variable that I though would be related was the DebtToIncomeRatio but it turned out to have a very low correlation to the interest rate columns. The distribution also contained extreme outliers and when exploring it's distribution the x-axis had to be adjusted to see a normally distributed histogram between values of 0 and 1.25 with a left skew.

In exploring how the interest rate of a loan is affected by the loans Term (length of loan) I discovered that under every ProsperRating shorter term loans had a lower interest rate. Unsurprisingly those with a higher/better ProsperRating had a lower interest rate.


## Key Insights for Presentation

To get a lower interest rate, build a good credit score (the higher the better).
Plan on making the loan term as short as possible.