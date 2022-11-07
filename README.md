# FEATURE SELECTION 

**What is feature selection?**
* Process of selecting a subset of relevant features (variable,predictors) to use in machine learning model building.

**Why should we select feature?**
* Simple models are easier to interpret
* Shorter trainings times: reduce computation cost, benefitial when fast decision need to be made
* Enhanced generalisaion by reducing overfitting
* Easy to implement by software developer , easier coding
* Reduce risk of data errors during model use
* Variable Redundancy (correlated features)
* Bad learning behavior in high dimensional spaces

**Main Features Selection Categories** 
1. Filter Methods
2. Wrapper Methods
3. Embedded Methods

# 1. Filter Methods
* Rely on the characteristics of data (feature characteristics)
* Features are selected on the basis of their scores in various statistical tests for their correlation with the outcome variable
* Do not use machine learning algorithms
* Model agnostic
* Tend to be less computationaly expensive
* Usually give lower prediction performance compared to other methods
* Suitable for quick screen and removed of irrelevant features
* Note: (-) Ignore the interaction with the classifier and each feature is considered independently thus ignoring feature dependencies

**Main Step Procedure in Filter method**
* Rank features according to certain criteria: Each feature is ranked independently of the feature space (univariate)
* Select the highest ranking features
* Note: may select redundant variables because they do not consider the relationship between features

**Ranking Criteria of filter method: Univariate**

![image](https://user-images.githubusercontent.com/117054438/200222116-81394bc8-917d-4d1b-bcf1-aa3232f91d1a.png)

* Pearson’s correlation coefficient (linear)
* Spearman’s rank coefficient (nonlinear)
* Univariate parametric tests (ANOVA) (linear) 
* Fisher Score
* Kendall’s rank coefficient (nonlinear)
* Chi-square 
* Mutual Information
* Variance including constant features and quasi-constant features
  - [Constant features removal - zero variance](https://github.com/solegalli/feature-selection-for-machine-learning/blob/main/03-Constant-Quasi-Constant-Duplicates/03.1-Constant-features.ipynb).
  - [Quantsi Constant features removel](https://github.com/solegalli/feature-selection-for-machine-learning/blob/main/03-Constant-Quasi-Constant-Duplicates/03.2-Quasi-constant-features.ipynb)

**Multivariate Filter Selection Methods**
* Handle redundant Feature
* Duplicate Feature
  - [Duplicate feature removal](https://github.com/solegalli/feature-selection-for-machine-learning/blob/main/03-Constant-Quasi-Constant-Duplicates/03.3-Duplicated-features.ipynb)
* Correlated Feature

**Summary of Filter methods**
* Simple yet power method to quickly remove irrelevant and redundant features: Constant, Duplicate, Correlate
* First step in feature selection procedure

# 1.1 Variance: Constant Feature



# 2. Wrapper Methods
* Use predictive machine learning model to score the feature subset
* Train a new model on each feature subset
* Tend to be very computationally expensive, sometime even can't be implemented
* Usually provide the best performing feature subset for given machine learning algorithms
* May not produce the best feature combination for different machine learning model

# 3. Embedded Methods
* Perform feature selection as part of model construction process
* Consider the interaction between features and model
* Less computationally expensive than wrapper methods, because they fit the machine learning model only once

# Other Popular Methods
* Boruta SHAP Feature Selection Method
  - [Boruta SHAP Implementation](https://www.kaggle.com/code/carlmcbrideellis/feature-selection-using-the-boruta-shap-package/notebook)
  - [Boruta SHAP](https://blog.kxy.ai/boruta-shap-is-as-bad-as-rfe/)
