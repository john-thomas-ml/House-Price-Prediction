House Price Prediction Using Machine Learning

Project Overview

This project leverages machine learning techniques to predict house prices based on various features, including square footage, number of bedrooms, and location. The primary objective is to develop a robust model that accurately estimates property values, facilitating informed decision-making for buyers, sellers, and investors.

Data Preprocessing

- Feature Engineering: The dataset was enhanced by creating new features such as price_per_sqft (price divided by square footage) and house_age (calculated as the current year minus the year built).

- Categorical Encoding: Categorical variables like zipcode and waterfront were transformed using one-hot encoding to convert them into numerical format suitable for modeling.

- Scaling: Standardization was applied to numerical features using StandardScaler to ensure all features contribute equally to the model, improving convergence and performance.

- Log Transformation: A log transformation was applied to the target variable (price) to address skewness and reduce the impact of outliers, leading to a more normal distribution and enhancing model accuracy.

Modeling

- Linear Regression: A linear regression model was trained on the preprocessed data to establish a baseline for performance.

- Cross-Validation: To assess the model's generalizability, 5-fold cross-validation was performed, providing a more reliable estimate of its performance.

Results

- Mean Absolute Error (MAE): $67,512.61

- Mean Squared Error (MSE): $15,375,971,725.82

- R-squared (R²): 0.898

- Root Mean Squared Error (RMSE): $123,999.89

These metrics indicate a strong predictive performance, with the model explaining approximately 89.8% of the variance in house prices.

Conclusion

The project demonstrates the effectiveness of machine learning in predicting house prices. By employing data preprocessing techniques such as feature engineering, categorical encoding, scaling, and log transformation, the model achieved high accuracy. The results underscore the importance of data preparation and model evaluation in developing reliable predictive tools for the real estate market.