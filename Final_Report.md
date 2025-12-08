# Can we successfully predict a person's happiness level?

## Introduction

Our project proposal is worthwhile because in the growing age of social media, there are increased concerns regarding impacts on mental health. There are many factors and habits that play a role in a person's happiness. Previous studies have included a connection with physical health, lack of security of fulfillment of basic needs, and social isolation. Mental health is crucial to society and struggles with it need to be addressed, but proposed solutions or methods for combating mental health struggles need to be rooted in the variables that actually impact individuals the most. Therefore, it is important to attempt to distinguish which factors contain more of a potentially significant role in order to best be able to apply findings to aid people's mental health struggles.

## Methods

### Dataset Description

We found our dataset on Kaggle. The sample size is 500 entries, all being unique samples. There are 10 columns, including age, gender, sleep quality, screen time, days without social media, happiness index, and more. Our dataset is 50% male, 46% female, and 4% other. The participants range from 16 to 49 years old, with a mean age of 32.98 and a standard deviation of 9.96.

### Data Preparation

To prepare our dataset for modeling, we had no missing values so we did not have to do anything in that regard. We did need to encode the categorical variables, and we dropped the user ID column.

### Models and Preprocessing

We used four models: A Penalized Linear Model, Support Vector Machine, Ensemble Model, and a Neural Network. All models required the same preprocessing steps which are label encoding categorical variables and standardizing features using StandardScaler.

**Elastic Net Regression (Penalized Linear Model):** Elastic Net combines L1 and L2 regularization for feature selection, with hyperparameters tuned over alpha values [0.001, 0.01, 0.1, 0.5, 1, 5, 10] and l1_ratio [0.1, 0.3, 0.5, 0.7, 0.9].

**Support Vector Machine (SVM):** SVMs capture non-linear relationships through kernel transformations with kernels including linear, rbf, and poly.

**Ensemble Model:** The Ensemble Model used Random Forest for improved robustness.

**Neural Network:** The Neural Network used fully connected layers with ReLU activation and dropout regularization, trained with SGD optimization.

### Cross-Validation Strategy

All models except for Neural Network used 5-fold cross-validation to estimate generalization performance by partitioning training data into 5 equal subsets, with each fold serving as validation while the remaining folds were used for training. The Neural Network model uses 3-fold validation.

### Performance Metrics

Model performance was evaluated using Mean Squared Error (MSE), Root Mean Squared Error (RMSE), Mean Absolute Error (MAE), and R² Score to assess prediction accuracy and model reliability.
