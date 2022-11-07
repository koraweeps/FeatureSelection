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
* Do not use machine learning algorithms
* Model agnostic
* Tend to be less computationaly expensive
* Usually give lower prediction performance compared to other methods
* Suitable for quick screen and removed of irrelevant features

**Main Step Procedure in Filter method**
* Rank features according to certain criteria: Each feature is ranked independently of the feature space (univariate)
* Select the highest ranking features
* Note: may select redundant variables because they do not consider the relationship between features

**Ranking Criteria of filter method: Univariate**
* Chi-square | Fisher Score
* Univariate parametric tests (ANOVA)
* Mutual Information
* Variance including constant features and quasi-constant features

**Multivariate Filter Selection Methods**
* Handle redundant Feature
* Duplicate Feature
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
