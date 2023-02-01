# Business Goal
You are required to model the price of houses with the available independent variables. This model will then be used by the management to understand how exactly the prices vary with the variables. They can accordingly manipulate the strategy of the firm and concentrate on areas that will yield high returns. Further, the model will be a good way for management to understand the pricing dynamics of a new market. Ridge and Lasso Regeression

## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
Step 1: Import the data by reading in the csv file

Step 2: Understand the data using df.describe(), df.info(), df.isnull().sum(), handling of missing data, categeorical and numerical data, convert date, feature engineering, create diction mapping, determine binary variables

Step 3: Clean the data - first find the pecentage of missing data.  In this case, I didn't drop any rows or columns.  I managed to replace misisng values with NA, mean/mode/or median.

Step 4: Data visualization to understand the data even more so that we know if there are any outliers; see if there are any lineararity.  I use boxplot and lmplot.
For outliers, I use IQR. Anything lies below or above upbound and lowerbound respectively will be removed. I also look at any correlation so I can determine which variables to drop.

Step 5: Scale the data and create dummy variables - machines only understand numbers.  Scaling will help speed up model training and convergence

Step 6: Train test split with RFE - coupled with Ridge and Lasso regularization to avoid overfitting


<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions

- Ridge: the coefficient changes but not significantly enough to change the order of Features. Higher alpha causes the coefficient to lower for positive value and the opposite for negative. Ridge uses Lamba as penalty. Ridge puts constraint on the coefficient (w) in the formula above. Large w will get penalized. 
- Ridge puts constraint on the coefficient (w) in the formula above. Large w will get penalized. cLasso penalizes the sum of their absolute values.  This also known as L1 regularization; where as Ridge is L2.  Higher alpha can lead to zero coefficient; hence auto feature selection.
- In this use case, I’d go with Ridge.  Out of the bat and without performing hyper parameter turning, Ridge 0.511 R-squared and 0.472 Adj. R-squared.  Also, the VIF value for Ridge is a lot smaller.  I have not removed any variables and retrain the model.  The result is subjected to change.
- On the other hand, Lasso gives 0.480 R-squared and 0.470 Adj. R-squared.
- To generalize the model, we have to discuss the diagram above.  The middle dotted line is the optimal where the model is not so complex and both bias and variance meet at an equilibrium middle section.   Highly complex model will have low bias and high variance.  The opposite is true where not so complex model will have low variance and high bias.  On the left side (high bias and low variance), the model is considered as underfitting.  Contrary, low bias high variance is overfitting. That means the model is doing very good with training data, but do poorly with real data.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
I had to import the following libraries for this project

- import numpy as np
- import pandas as pd
- import matplotlib.pyplot as plt
- import seaborn as sns
- import datetime as dt
- from datetime import date
- from sklearn.preprocessing import PowerTransformer
- from sklearn.feature_selection import RFE
- from sklearn.linear_model import Ridge, Lasso
- from sklearn.model_selection import GridSearchCV
- import statsmodels.api as sm
- from statsmodels.stats.outliers_influence import variance_inflation_factor





<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->


## Contact
Created by [@agiq] - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
