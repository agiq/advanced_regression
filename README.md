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
- Conclusion 1 from the analysis
- Conclusion 2 from the analysis
- Conclusion 3 from the analysis
- Conclusion 4 from the analysis

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
- library - version 1.0
- library - version 2.0
- library - version 3.0

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements
Give credit here.
- This project was inspired by...
- References if any...
- This project was based on [this tutorial](https://www.example.com).


## Contact
Created by [@githubusername] - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
