# SGD-Regressor-for-Multivariate-Linear-Regression

## AIM:
To write a program to predict the price of the house and number of occupants in the house with SGD regressor.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries and define the feature and target datasets.
2. Apply feature scaling using StandardScaler
3. Create and train the SGDRegressor model using the scaled data.
4. Display the model coefficients, intercept, and predicted values.

## Program:
```
/*
Program to implement the multivariate linear regression model for predicting the price of the house and number of occupants in the house with SGD regressor.
Developed by: JAYASHREE J
RegisterNumber:  212225040145

#Using scikit-learn SGDRegressor
import numpy as np
from sklearn.linear_model import SGDRegressor
from sklearn.preprocessing import StandardScaler

# Features and target
X = np.array([
    [2, 80, 50],
    [3, 60, 40],
    [5, 90, 70],
    [7, 85, 80],
    [9, 95, 90]
])
y = np.array([50, 45, 70, 80, 95])

# Feature scaling
scaler = StandardScaler()
X_scaled = scaler.fit_transform(X)

# Create SGD Regressor
sgd_reg = SGDRegressor(max_iter=1000, learning_rate='invscaling', eta0=0.01, random_state=42)
sgd_reg.fit(X_scaled, y)

# Coefficients and intercept
print("Weights (coefficients):", sgd_reg.coef_)
print("Intercept:", sgd_reg.intercept_)

# Predictions
y_pred = sgd_reg.predict(X_scaled)
print("Predicted values:", y_pred)

*/
```

## Output:
<img width="1410" height="101" alt="image" src="https://github.com/user-attachments/assets/ef6a738c-c43a-4e64-a077-415c499f5996" />



## Result:
Thus the program to implement the multivariate linear regression model for predicting the price of the house and number of occupants in the house with SGD regressor is written and verified using python programming.
