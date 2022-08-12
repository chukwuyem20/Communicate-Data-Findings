# Communicating Data Findings

## by Peace Ugbekile

## Dataset

> The original dataset is the Loan Data From Prosper with a structure of 113,937 rows and 81 columns. The columns contained variables regarding each loan, some of which were loan term, loan amount, borrower rate, loan status and borrowers' income alongside other information. Prior to the commencement of exploratory data analysis, I performed the following tasks on the dataset to obatin my final dataset on which EDA was conducted:

> 1. Data gathering: I chose a dataset from the list of provided datasets

> 2. Data assessing: Investigating the dataset for my choice variables as well as issues requiring cleaning.

> 3. Data cleaning: Creating a new dataframe containing only interested variables, removing null values from "ProsperScore" column, removing null values from "debt-to-income ratio" column, splitting the "ListingCreationDate" into different columns (Year, Month, Day and Time),  removing outlier from "employment status" column.

## Summary of Findings

> I explored two basic issues: understanding the factors affecting borrowers' ability to complete their loan repayment by looking at their loan status as well as the main factors affecting their loans' Annual Percentage Rate (APR). I further investigated the impact of loan tenure (loan term) on the relationship between various variables of interest.

> The apriori expectation was that the amount of loan availed to borrowers would impact their ability to complete their repayment. However, this would also depend on their income level, interest rate as well as APR. Furthermore, their APR would be affected by their credit worthiness (captured as their prosper score), monthly income as well as loan amount.

> Before these relationships were examined, the individual variables were examined and the following observations were noted:

> The most loans were availed in 2013 and in the month of January. However, the last quarter of the year (October - December) also had high number of loan disbursement compared to the second and third quarter. This could imply that the borrowers were preparing for the first quarter of the year with respect to the utilization of the loan, hence the increase in loan disbursement between the last quarter and begining of the first quarter (January and February). Other quarters were most likely production and utilization period, rather than a period for debt accummulation. 

> Loans that were currently running and not yet classified as either completed, defaulted or bad, had the highest count. This was followed by the comploeted loans. The distribution of the APR is almost a normal distribution, however, there are several peaks, i.e., the graph is a multimodal with the highest peak found between 0.35 and 0.37. Very few loans have APR greater than 0.4.

> The interest rate distribution had a similar distribution pattern with the APR plot. However, the highest peak for this multimodal graph is between 0.31 and 0.33. Furthermore, beyond the rate of 0.35, the number of loans was extremely few. The plot of monthly income is extremely rightly skewed with the highest number of loan recipients earning close to the mean monthly income of approximately 5,964 dollars. Those earning above 15,000 dollars are infinitesimal. This refelceted in the income range of the borrowers where the higher income range had the least number of persons and the highest count was in the range of 50k to 75k dollars.

>  Most of the borrowers had a debt-to-income ratio between 0.19 and 0.21. This appears to be a good value given that the As a general guideline around debt-to-income ratio is that most lenders prefer a value that is lower than 0.36 as this index reflects the ease with which a borrower can pay down a loan. Another interesting index is the Prosper Score which defines the credit worthiness of the borrower. The plot is almost normally distributed but multimodal with the highest number of borrowers falling between a prosper score of 8 and 9.

> The relationship between the loan status and loan amount satisfied the apriori expectation as the plot revealed that the mean loan amount for the completed loans is less than all other status except current (which represents ongoing loans not yet classed as defaults or past due and whose status could change with time) and past due (61 - 90 days), which could be explained by other factors not investigated in this analysis. This could mean that the borrowers are more likely to complete their repayment if the loan amount is small. However, investigating how their monthly income was associated with their repayment helped with deeper insights as the mean income for completed current and payment in progress loans was higher than all other forms of bad or defaulting loans. This further strengthens the hypothesis that income affects ability to pay down on loans.

> In terms of the interest rate (borrowers' rate), it was observed that the mean interest rate for "completed" loans, "current" loans and "final payment in progress" loans was lower than for defaulting and other bad loans (past due). This meets the apriori expectation that likelihood for prompt repayment increases with decrease in borrower's rate.

> Following the correlation analysis that was carried out and displayed using a heat map, it was observed that APR was strongly correlated with interest rate (corr = 0.993) and this relationship was a postitve correlation which means that as APR increases, the interest rate given to a borrower also increases. This could be a function of several factors like the amount of loan or even the credit worthiness of the borrower. Furthermore, APR was also strongly correlated with prosper score, but this was a negative correlation which implies that as prosper score increases, the APR decreases (corr = -0.675).

> The correlation coefficient of borrower APR and loan original amount is -0.418 which shows a negative correlation. This suggests that the more the loan amount, the lower the APR. Also, the loan original amount showed a positive correlation with monthly income (corr = 0.300) which indicates that borrowers who earn more would be availed more funds in loan.

> Loan tenure (term) was introduced as a mediator to moderate the relationship between some of these variables. However, it was observed that across all loan tenures (12, 36 and 60 months) the relationship between APR and Original Loan Amount remained unchanged, i.e., a negative relationship was still observed.

> Interestingly, APR decreases with increased loan term for defaulters and past due loans. Similar APR movement pattern was observed for current, completed and final payment in progress loans, i.e., an increase then a decrease in APR. However, the proportion differs.

> Regarding the effect of loan term on the association between APR and Prosper Score, three patterns were observed. An increase in APR was seen between the score of 1 and 3 and immediately followed by a decrease as the loan term increased. While the score of 4, 6 and 7 showed a decreasing APR with an increase in loan term. Finally, between the prosper score of 9 - 11, an increase in APR was observed with increasing loan term.

## Key Insights for Presentation

> Number of loan availment is highest in January and loan disbursement increased at an increasing rate between 2009 - 2013 and then declined in 2014. This could have been because of the increase in defaults or bad loans.

> The currently running loans and completed loan are more than defaults for the period under observation.

> Borrowers' Annual Percentage Rate is multimodal with the highest peak found between 0.35 and 0.37 and infinitesimal number of loans with APR greater than 0.4.

> Monthly income is extremely right skewed with majority of the borrowers earning within the mean income amount of about 5,964 dollars and extremely few persons earning above 15,000 dollars. Income range strengthens this position as borrowers with higher income range had the least number of persons and the highest count was in the range of 50k to 75k dollars.

> The mean loan amount for the completed loans is less than all other status except current (which represents ongoing loans not yet classed as defaults or past due and whose status could change with time) and past due (61 - 90 days). This implies that the borrowers are more likely to complete their repayment if the loan amount is small. 

> The mean income for completed, current and payment in progress loans was higher than all other forms of bad or defaulting loans. This further strengthens the hypothesis that income affects ability to pay down on loans.

> Borrower APR is negatively correlated with loan original amount suggesting that the more the loan amount, the lower the APR and the loan original amount is positively correlated with monthly income indicating that borrowers who earn more would be availed more funds in loan.

> The borrower APR decreases with the increasingly better prosper score. Borrowers with the best Prosper scores have the lowest APR. It means that the Prosper rating has a strong effect on borrower APR.

> The mean interest rate for "completed" loans, "current" loans and "final payment in progress" loans was lower than for defaulting and other bad loans (past due). 
