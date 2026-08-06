### Comparing different regression types

| Model Name | Description | Code Syntax |
| --- | --- | --- |
| Simple linear regression | **Purpose:** To predict a dependent variable based on one independent variable.<br><br> **Pros:** Easy to implement, interpret, and efficient for small datasets.<br><br> **Cons:** Not suitable for complex relationships; prone to underfitting.<br><br> **Modeling equation:** $y = b_0 + b_1x$ | <ol><li> `from sklearn.linear_model import LinearRegression` </li><li>`model = LinearRegression()` </li><li> `model.fit(X, y)` </li></ol> |
| Polynomial regression | **Purpose:** To capture nonlinear relationships between variables. <br><br> **Pros:** Better at fitting nonlinear data compared to linear regression. <br><br> **Cons:** Prone to overfitting with high-degree polynomials. <br><br> **Modeling equation:** $y = b_0 + b_1x + b_2x^2 + \dots$ | <ol><li> `from sklearn.preprocessing import PolynomialFeatures` </li><li>`from sklearn.linear_model import LinearRegression` </li><li> `poly = PolynomialFeatures(degree=2)` </li><li> `X_poly = poly.fit_transform(X)` </li><li> `model = LinearRegression().fit(X_poly, y)` </li></ol> |
| Multiple linear regression | **Purpose:** To predict a dependent variable based on multiple independent variables. <br><br> **Pros:** Accounts for multiple factors influencing the outcome. <br><br> **Cons:** Assumes a linear relationship between predictors and target. <br><br> **Modeling equation:** $y = b_0 + b_1x_1 + b_2x_2 + \dots$ | <ol><li> `from sklearn.linear_model import LinearRegression` </li><li> `model = LinearRegression()` </li><li> `model.fit(X, y)` </li></ol> |
| Logistic regression | **Purpose:** To predict probabilities of categorical outcomes. <br><br> **Pros:** Efficient for binary classification problems. <br><br> **Cons:** Assumes a linear relationship between independent variables and log-odds. <br><br> **Modeling equation:** $log(p/(1-p)) = b_0 + b_1x_1 + b_2x_2 + \dots$ | <ol><li> `from sklearn.linear_model import LogisticRegression` </li><li> `model = LogisticRegression()` </li><li> `model.fit(X, y)` </li></ol> |

<br>

### Associated functions commonly used

| Function/Method Name | Brief Description | Code Syntax |
| --- | --- | --- |
| train_test_split | Splits the dataset into training and testing subsets to evaluate the model's performance. | <ol><li> `from sklearn.model_selection import train_test_split` </li><li> `X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)` </li></ol> |
| StandardScaler | Standardizes features by removing the mean and scaling to unit variance. | <ol><li> `from sklearn.preprocessing import StandardScaler` </li><li> `scaler = StandardScaler()` </li><li> `X_scaled = scaler.fit_transform(X)` </li></ol> |
| log_loss | Calculates the logarithmic loss, a performance metric for classification models. | <ol><li> `from sklearn.metrics import log_loss` </li><li> `loss = log_loss(y_true, y_pred_proba)` </li></ol> |
| mean_absolute_error (MAE) | Calculates the mean absolute error between actual and predicted values. | <ol><li> `from sklearn.metrics import mean_absolute_error` </li><li> `mae = mean_absolute_error(y_true, y_pred)` </li></ol> |
| mean_squared_error (MSE) | Computes the mean squared error between actual and predicted values. | <ol><li> `from sklearn.metrics import mean_squared_error` </li><li> `mse = mean_squared_error(y_true, y_pred)` </li></ol> |
| root_mean_squared_error (RMSE) | Calculates the root mean squared error (RMSE), a commonly used metric for regression tasks. | <ol><li> `from sklearn.metrics import mean_squared_error` </li><li> `import numpy as np` </li><li> `rmse = np.sqrt(mean_squared_error(y_true, y_pred))` </li></ol> |
| r2_score | Computes the R-squared value, indicating how well the model explains the variability of the target variable. | <ol><li> `from sklearn.metrics import r2_score` </li><li> `r2 = r2_score(y_true, y_pred)` </li></ol> |