# HR-Analytics
 
## Define
Attrition is one of the most common issues at any organization. The amount of  time, money and effort to train new employees can lead to great loss for the company. The loss cost includes on-boarding, advertising, hiring, training and lost productivity. Additionally, attrition causes doubt or distrust among current employees with the management. 
According to the [Gallup](https://www.gallup.com/workplace/247391/fixable-problem-costs-businesses-trillion.aspx), U.S business lose a trillion dollars every year due to employee turnover. It also argues that problem is fixable with right strategy and retention plan. 

This project provides in-depth analysis of factors that lead to employee turnover, create model and provide retention strategy using [**Kaggle** IBM HR dataset.](https://www.kaggle.com/pavansubhasht/ibm-hr-analytics-attrition-dataset). Please follow this link, [Understanding and Predicting IBM Employee Attrition](https://github.com/min-tee/HR-Analytics/blob/main/HR_Analytics.ipynb) for details.


## Discover
Tools Used : Google Colab

Packages : pandas, numpy, matplotlib, seaborn, sklearn

Data :  35 features with 1470 observations.

**EDA**

**Feature Distributions**
![feature_dist](https://github.com/min-tee/HR-Analytics/blob/fd84a0d7477d265fc85f9c4b95c176e18503fd38/Charts/distributions.png)
![age](https://github.com/min-tee/HR-Analytics/blob/ccbacc3903ae6cae02e12953e55a69145927855b/Charts/attrition_age.png)
Attrition is high among employees in late 20's and early 30's.

**Attrition Counts**

![attrition](https://github.com/min-tee/HR-Analytics/blob/4d3c27d93d511602c18c095ceeff96d870295214/Charts/imbalanced_data.png)

Data is highly imbalanced. 

**Correlation**

![correlation](https://github.com/min-tee/HR-Analytics/blob/c63b2cc858c5315aaa88ccbba1c27f30d6e6a2d6/Charts/correlation%20matrix.png)
Instances of multicollinearity. 






## Develop
Models : Logistic Regression, Random Forest, KNN, SVM

Feature Engineering : One-hot Encoding

Model Performance Techniques: Feature Selection, Feature Scaling, Treat imbalanced dataset(SMOTE, Up sampling & Down sampling), Hyperparameter Tuning

Metrics : F1-Score, ROC Graph

First, developed baseline models without model improvement techniques. 

**Baseline AUC & F1-score**

![scores](https://github.com/min-tee/HR-Analytics/blob/d12b193f2922f683f09792450bf59c3a34f9ff2e/Charts/baseline_scores.PNG)


**Baseline ROC Graph**

![roc](https://github.com/min-tee/HR-Analytics/blob/d12b193f2922f683f09792450bf59c3a34f9ff2e/Charts/baseline_roc.png)

**Improved AUC & F1-score**

![improved](https://github.com/min-tee/HR-Analytics/blob/fc01a41a84e58960c9dfb5cf0ed7a45e45de219c/Charts/improved_metrics.png)


**Improved ROC Graph**

![improved_roc](https://github.com/min-tee/HR-Analytics/blob/fc01a41a84e58960c9dfb5cf0ed7a45e45de219c/Charts/improved_roc.png)

**Random Forest Feature Importance**

![rf_feat](https://github.com/min-tee/HR-Analytics/blob/fc01a41a84e58960c9dfb5cf0ed7a45e45de219c/Charts/rf_feat_impt.png)




## Deploy

**Retention Strategy**

Based on feature importance chart, we can say that that overtime, job level, stock option level, time with current manager, marital status and income also play a vital role in employee attrition. On the contrary, department, job role, education tend not to contribute for turnover. The company can focus on the factors contributing higher contributing attrition. However, there are other factors such as selection bias, type of employment(interns, contractors, part time or full time) that may need to be considered that are not necessarily captured by the model. Additionally, it is recommended that models are tuned at a certain frequency to include recent data and drop features of lower importance. Chi-Square test may be used to determine the dependence between attrition and other features.

