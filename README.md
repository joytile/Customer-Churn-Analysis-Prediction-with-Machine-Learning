# PowerCo Customer Churn Analysis Prediction with Machine Learning
![GitHub](https://img.shields.io/badge/Language-Python-blue)
![GitHub](https://img.shields.io/badge/Model-Voting_Classifier-purple)
![GitHub](https://img.shields.io/badge/Library-Scikit_Learn-Green)

## Project Overview

PowerCo is a major gas and electricity company concerned about losing customers. We have been been provided with the client data and price data and we will try to determine what the major drivers of churn are.

Our leading hypothesis is: 'Does price sensitivity affect churn?'

## Dataset 📂
The dataset is contained in the 'client_data.csv' and 'price_data.csv'

## Methodology 
### 1. Exploratory Data Analysis 🔭
- **Descriptive Statistics**: Examining the characteristics of the data
- **Variable Analysis**: Visualizing each feature to understand it better
  
![Chart](https://github.com/joytile/Customer-Churn-Analysis-and-Prediction-with-Machine-Learning/blob/main/churn_status.png)
### 2. Data Preprocessing and Feature Engineering 🛠️
- **Outlier Handling**: Logarithmic transformation on positively skewed features
- **Variable encoding**: Encoding boolean and other categorical variables to allow the model understand them
- **Creating new features**: Engineered new features to contribute to predictive power of the model
- **Dropping features**: Removing features that don't contribute much to the model
### 3. Model Development
- **Hyperparameter Tuning**: Tuning the model with optuna to maximize F1-score
- **Class Balancing**: Balancing the severely imbalanced target variable, churn.
- **Ensemble Model**: Combined LightGBM and Random forest Classifiers using Voting Classifier
### 4. Model Evaluation
- **Metrics**: Accuracy, Precision, Recall, F1-Score, Confusion Matrix


# Key insights💡
- Net margin on power subscription and consumption over 12 months the top drivers for churn in this model.
- Forecasted electricity consumption and overall net margins are also influential drivers.
- Time seems to be an influential factor, especially the number of months they have been active, their tenure and the number of months since they updated their contract
- Our price sensitivity features are scattered around but are not the main driver for customer churning

The last observation is important because this relates back to our original hypothesis:

    > Is churn driven by the customers' price sensitivity?

Based on the output of the feature importances, it is not a main driver, but a weak contributor. 

![Chart](https://github.com/joytile/Customer-Churn-Analysis-and-Prediction-with-Machine-Learning/blob/main/feature_importances.png)
# Rceommendations 👌
- Discount strategy of 20% offered to hugh value customers with high churn probability
