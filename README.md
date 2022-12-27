## Predicting Default for the next Credit Payment

### Problem Statement
Given certain parameters predict the chances of a client defaulting on his/her next credit card payments.

### Data 
Data has been collected from <a href="https://archive.ics.uci.edu/ml/datasets/default+of+credit+card+clients"> here </a>.

### Evaluation
**Trained on the following models:**
 - k-nearest-neighbors
 - RandomForestClassifier
 - LogisticRegression

**After training the models, we also performed the following:**
 - Hypyterparameter tuning
 - Feature importance
 - Confusion matrix
 - Cross-validation
 - Precision
 - Recall
 - F1 score
 - Classification report
 - ROC curve
 - Area under the curve (AUC)

At or above 80% accuracy we consider our model as successful. 
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

### Used Libraries and Pre-Defined Metrics/Models
```
 import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# we want our plots to appear inside the notebook
%matplotlib inline 

# For Models from Scikit-Learn
from sklearn.linear_model import LogisticRegression
from sklearn.neighbors import KNeighborsClassifier
from sklearn.ensemble import RandomForestClassifier

# For Model Evaluations
from sklearn.model_selection import train_test_split, cross_val_score
from sklearn.model_selection import RandomizedSearchCV, GridSearchCV
from sklearn import metrics
from sklearn.metrics import confusion_matrix, classification_report
from sklearn.metrics import precision_score, recall_score, f1_score
from sklearn.metrics import plot_roc_curve
 ```
 ### Conclusion
 
 RandomForestClassifier emerged as the best model with 82% accuracy. With the following parameters: 
 ```
 {'n_estimators': 710,
 'min_samples_split': 16,
 'min_samples_leaf': 3,
 'max_depth': 20}
 ```
 
 
