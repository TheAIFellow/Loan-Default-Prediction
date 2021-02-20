# Loan-Default-Prediction

Loan default occurs when a borrower fails to pay back a debt according to the initial arrangement. In the case of most consumer loans, this means that successive payments have been missed over the course of weeks or months. Fortunately, lenders and loan servicers usually allow a grace period before penalizing the borrower after missing one payment. The period between missing a loan payment and having the loan default is known as delinquency. The delinquency period gives the debtor time to avoid default by contacting their loan servicer or making up missed payments.
Defaulting on a loan will cause a substantial and lasting drop in the debtor's credit score, as well as extremely high interest rates on any future loan. For loans secured with collateral, defaulting will likely result in the pledged asset being seized by the bank. The most popular types of consumer loans that are backed by collateral are mortgages, auto loans and secured personal loans. For unsecured debts like credit cards and student loans, the consequences of default vary in severity according to the type of loan. In the most extreme cases, debt collection agencies can garnish wages to pay back the outstanding debt.
The loan is one of the most important products of the banking. All the banks are trying to figure out effective business strategies to persuade customers to apply their loans. However, **there are some customers behave negatively after their application are approved**.

Feature Details:
:id:-A unique LC assigned ID for the loan listing.

1:member_id:-A unique LC assigned Id for the borrower member.

2:loan_amnt:-The listed amount of the loan applied for by the borrower. If at some point in time, the credit department reduces the loan amount, then it will be reflected in this value.

3:funded_amnt:-The total amount committed to that loan at that point in time.

4:funded_amnt_inv:-The total amount committed by investors for that loan at that point in time.

5:term:-The number of payments on the loan. Values are in months and can be either 36 or 60.

6:int_rate:-Interest Rate on the loan

7:installment:-The monthly payment owed by the borrower if the loan originates.

8:grade:-LC assigned loan grade

9:sub_grade:-LC assigned loan subgrade

10:emp_title:-The job title supplied by the Borrower when applying for the loan.*

11:emp_length:-Employment length in years. Possible values are between 0 and 10 where 0 means less than one year and 10 means ten or more years. 

12:home_ownership:-The home ownership status provided by the borrower during registration. Our values are: RENT, OWN, MORTGAGE, OTHER.

13:annual_inc:-The self-reported annual income provided by the borrower during registration.

14:verification_status:-Indicates if income was verified by LC, not verified, or if the income source was verified

15:issue_d:-The month which the loan was funded

16:loan_status:-Current status of the loan

17:pymnt_plan:-Indicates if a payment plan has been put in place for the loan

18:url:-URL for the LC page with listing data.

19:desc:-Loan description provided by the borrower

20:purpose:-A category provided by the borrower for the loan request. 

21:title:-The loan title provided by the borrower

22:zip_code:-The first 3 numbers of the zip code provided by the borrower in the loan application.
23:addr_state:-The state provided by the borrower in the loan application
24:dti:-A ratio calculated using the borrower’s total monthly debt 
payments on the total debt obligations, excluding mortgage and the requested LC loan, divided by the borrower’s self-reported monthly income.

25:delinq_2yrs:-The number of 30+ days past-due incidences of delinquency in the borrower's credit file for the past 2 years

26:earliest_cr_line:-The month the borrower's earliest reported credit line was opened

27:fico_range_low:-The lower boundary range the borrower’s FICO at loan origination belongs to.

28:fico_range_high:-The upper boundary range the borrower’s FICO at loan origination belongs to.

29:inq_last_6mths:-The number of inquiries in past 6 months (excluding auto and mortgage inquiries)

30:mths_since_last_delinq:-The number of months since the borrower's last delinquency.

31:open_acc:-The number of open credit lines in the borrower's credit file.

32:pub_rec:-Number of derogatory public records

33:revol_bal:-Total credit revolving balance

34:revol_util:-Revolving line utilization rate, or the amount of credit the borrower is using relative to all available revolving credit.

35:total_acc:-The total number of credit lines currently in the borrower's credit file

36:initial_list_status:-The initial listing status of the loan. Possible values are – W, F

37:out_prncp:-Remaining outstanding principal for total amount funded

38:out_prncp_inv:-Remaining outstanding principal for portion of total amount funded by investors

39:total_pymnt:-Payments received to date for total amount funded

40:total_pymnt_inv:-Payments received to date for portion of total amount funded by investors

41:total_rec_prncp:-Principal received to date

42:total_rec_int:-Interest received to date

43:total_rec_late_fee:-Late fees received to date

44:recoveries:-post charge off gross recovery

45:collection_recovery_fee:-post charge off collection fee

46:last_pymnt_d:-Last month payment was received

47:last_pymnt_amnt:-Last total payment amount received

48:last_credit_pull_d:-The most recent month LC pulled credit for this loan

49:last_fico_range_high:-The upper boundary range the borrower’s last FICO pulled belongs to.

50:last_fico_range_low:-The lower boundary range the borrower’s last FICO pulled belongs to.

51:collections_12_mths_ex_med:-Number of collections in 12 months excluding medical collections

52:policy_code:-publicly available policy_code=1

new products not publicly available policy_code=2

53:application_type:-Indicates whether the loan is an individual 
application or a joint application with two co-borrowers

54:acc_now_delinq:-The number of accounts on which the borrower is now delinquent.

55:chargeoff_within_12_mths:-Number of charge-offs within 12 months

56:delinq_amnt:-The past-due amount owed for the accounts on which the 
borrower is now delinquent.

57:pub_rec_bankruptcies:-Number of public record bankruptcies

58:tax_liens:-Number of tax liens


Steps :
 1. Defining problem statement 
 2. EDA and feature engineering
 3. Feature Selection 
 4. Preparing dataset for modeling
 5. Applying Model 
 6. Model Validation and Selection

# **Conclusion**
1. The last_fico_range, grade, inq_last_6month  features were found to be the most relevant for predicting loan default in. The current model tries to predict default biased data from credit analysts grade and assigned interest rate. The XGBC and RF models provide substantial improvements on traditional credit screening. A recall score significantly and robustly above 90%, with AUC-ROC scores ≃74%. The features provided to the model in our study generalize to any lending activity and institution, beyond P2P lending. The present work could, therefore, be augmented in order to predict loan default risk without the need for human credit screening.
2. Due to the time limit, it is not possible to conduct a thorough study and have a deep understanding of the dataset. There are still many features in the dataset that are unused and a lot of the information has not been fully digested with knowledge in the banking industry.
3. Only the Random Forest., XGBoost, model is used, but there are many good ones out there even neural networks. The models can also be improved further by finer tunings on hyperparameters or using ensemble methods such as bagging, boosting,.
4. In the bank loan behaviour prediction, for example, banks want to control the loss to a acceptable level, so they may use a relatively low threshold. This means more customers will be grouped as “potential bad customers” and their profiles will be checked carefully later by the credit risk management team. In this way, banks can detect the default behaviours in the earlier stage and conduct the corresponding actions to reduce the possible loss.

# **Recomendation**

Dataset from a Lending club is an interesting dataset. It is offen very difficult to get the insights of interest rate from Bank. This analysis provides interesting information about the interest rate which we get from Lending club for each person.
The interest rate which we receive depends on the various factors like FICO score, Homeownership, Purpose of loan, loan amount requested, Annual income, Employee length, Issue month, Previous bankrupcies and Debt to income ratio.
If a person is wanting to get a good interest rate then he need to focus on above factors before applying for a lending club loan.
From the research question, we understood that we need to perform various test and add visalizations to understand the patern of Lending club borrowers data and find the interest rate. It is not a very straight forward method which gets from FICO scores. Also lot of financial terms while dealing with loans.
