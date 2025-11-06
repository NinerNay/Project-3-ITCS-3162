# Introduction
The goal of this project is to predict house prices based on various physical and locational characteristics of residential properties. This is a part of a Kaggle competition, "House Prices: Advanced Regression Techniques". The competition provides a dataset describing nearly 1,500 homes in Ames, Iowa, each with 79 explanatory variables such as lot size, year built, overall material quality, etc.

By applying multiple regression-based modeling techniques, this project seeks to identify the underlying patterns and relationships that influence housing prices. The analysis demonstrates how statistical modeling and machine learning can be leveraged to extract insights from real-world data, ultimately supporting data-driven decision-making in the housing market.

For this study, the train.csv and test.csv datasets provided by Kaggle were used to train the models and generate predictions on unseen data.

# Regression
Regression is a supervised learning technique used to predict continuous numerical values based on one or more independent variables (features). These features influence the prediction, while the dependent variable (target) is the value we are trying to predict. Regression analysis helps us understand how changes in input variables influence the output variable.

In this project, the focus is on Linear Regression, one of the most fundamental and widely used statistical models in both machine learning and data science.

# Linear Regression
Linear regression learns from labeled datasets and models the relationship between input features and the target variable by fitting a straight line that best represents the data. The main objective of linear regression is to find the line that minimizes the difference (error) between the predicted values and the actual data points.

This relationship is represented by the equation:

* y = mx +b

Where:

* y = predicted value (dependent variable)
* x = input feature (independent variable)
* m = slope of the lines (how much y changes when x changes)
* b = the intercept (value of y when x = 0)

In practice, linear regression identifies the optimal values of m and b that minimize the Mean Squared Error (MSE) between predicted and actual outcomes. This process enables the model to generalize patterns from the training data and make accurate predictions on new, unseen data.

# Data Understanding
Before beginning the experiments, I first explored the dataset to gain a better understanding of its structure and contents. Using the .info() function on both the training and testing datasets, I examined the different data types and checked for any missing values. This revealed that the dataset contains a mix of categorical and numerical features.

To understand the distribution of house prices, I created a histogram of the SalePrice variable. The visualization showed that housing prices were right-skewed, meaning that most houses were moderately priced, with a few much higher-priced properties pulling the distribution to the right. To address this skewness and make the data more suitable for modeling, I applied a log transformation to the SalePrice variable, which helped normalize the values.

Next, I created a correlation heatmap to examine how different features relate to the sale price. The analysis showed that certain features, such as GarageArea, GrLivArea (above-ground living area), and OverallQual (overall material and finish quality), have a strong positive correlation with house prices. In general, homes with larger garage spaces or higher overall quality tend to have higher sale values.
