## Predicting Defaulting Rate of Users for next Credit Card Payment

### Problem Statement
Given certain parameters predict the chances of a client defaulting on his/her next credit card payments.

### Data 
Data has been collected from <a href="https://archive.ics.uci.edu/ml/datasets/default+of+credit+card+clients"> here </a>.

### Evaluation
**Trained on the following models:**
 - k-nearest-neighbors
 - RandomForestClassifier
 - LogisticRegression

At 80% accuracy we consider our model as successful. 
For evaluation check: credit-card-default-payment-prediction.ipynb 

### Data Features
This research employed a binary variable, default payment (Yes = 1, No = 0), as the response variable. This study reviewed the literature and used the following 23 variables as explanatory variables:<ol>
<li>Amount of the given credit (NT dollar): it includes both the individual consumer credit and his/her family (supplementary) credit.<br> <span id="features"></span>
<li>Gender (1 = male; 2 = female).<br>
<li>Education (1 = graduate school; 2 = university; 3 = high school; 4 = others).<br>
<li>Marital status (1 = married; 2 = single; 3 = others).<br>
<li>Age (year).<br>
<li>History of past payment (History of Past Payment): We tracked the past monthly payment records (from April to September, 2005) as follows: X6 = the repayment status in September, 2005; X7 = the repayment status in August, 2005; . . .;X11 = the repayment status in April, 2005. The measurement scale for the repayment status is: -1 = pay duly; 1 = payment delay for one month; 2 = payment delay for two months; . . .; 8 = payment delay for eight months; 9 = payment delay for nine months and above.<br>
<li>Amount of bill statement (NT dollar)(BILL_AMT) X12 = amount of bill statement in September, 2005; X13 = amount of bill statement in August, 2005; . . .; X17 = amount of bill statement in April, 2005.<br>
<li>Amount of previous payment (NT dollar)(Pay_Amt 1). X18 = amount paid in September, 2005; X19 = amount paid in August, 2005; . . .;X23 = amount paid in April, 2005.
