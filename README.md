House Price Prediction Using Machine Learning

Project Overview

This project leverages machine learning techniques to predict house prices based on various property features (e.g., square footage, number of bedrooms, and location). The primary objective is to develop a robust model that accurately estimates property values, thereby facilitating informed decision-making for buyers, sellers, and investors.

Data Preprocessing

- Feature Engineering:
    New features were created to enhance the dataset:
        - price_per_sqft: Calculated as the raw price divided by square footage. (Note: After computing this, both the raw price and the original square footage were dropped to reduce redundancy and multicollinearity.)
        - house_age: Computed as the current year minus the year built.

- Categorical Encoding:
    Categorical variables such as zipcode and waterfront were transformed using one-hot encoding to convert them into numerical format.

- Scaling:
    Standardization (using StandardScaler) was applied to numerical features to ensure that all features contribute equally to the model, improving convergence and performance.

- Log Transformation:
    To address right-skewness and reduce the influence of extreme values, a log transformation was applied to the target variable (price). This not only helps in stabilizing variance and normalizing the distribution but also enhances the predictive performance of the model.

Modeling

- Linear Regression:
    A linear regression model was trained on the preprocessed data, with the log-transformed price as the target variable.

- Cross-Validation:
    5-fold cross-validation was used to assess the model's generalizability, providing a more robust estimate of its performance.

Results

The model's performance on the log-transformed target is summarized below:

- Mean Absolute Error (MAE): 0.0933
- Mean Squared Error (MSE): 0.0180
- R-squared (R²): 0.9368
- Root Mean Squared Error (RMSE): 0.1342
- Cross-validation MSE: 0.0155

These metrics indicate that the model explains approximately 93.7% of the variance in the log-transformed house prices—a significant improvement compared to previous iterations. While the error metrics are now on the log scale, they reflect improved residual behavior and a better-fitting model. (If needed, predictions can be exponentiated to revert back to the original dollar scale.)

Conclusion

This project demonstrates the effectiveness of combining robust data preprocessing techniques—including feature engineering, categorical encoding, scaling, and log transformation—with linear regression to predict house prices. The new model not only achieves higher explanatory power (R² ≈ 93.7%) but also benefits from improved error distribution and reduced multicollinearity by using a normalized metric (price per square foot) in place of the raw price and square footage. These results underscore the importance of thoughtful data transformation and feature selection in developing reliable predictive tools for the real estate market.