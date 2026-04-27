# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Load the dataset into a DataFrame and explore its contents to understand the data structure.
2.Separate the dataset into independent (X) and dependent (Y) variables, and split them into training and testing sets.
3.Create a linear regression model and fit it using the training data.
4.Predict the results for the testing set and plot the training and testing sets with fitted lines.
5.Calculate error metrics (MSE, MAE, RMSE) to evaluate the model’s performance.

## Program:
```
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: Rishwanth S V
RegisterNumber: 212225040338
*/

import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression

X = np.array([1, 2, 3, 4, 5, 6, 7]).reshape(-1, 1)
Y = np.array([35, 40, 50, 60, 65, 70, 78])
model = LinearRegression()
model.fit(X, Y)
hours = float(input("Enter number of hours studied: "))

predicted_marks = model.predict([[hours]])
print("Predicted Marks Scored:", round(predicted_marks[0], 2))

plt.scatter(X, Y, color='blue', label='Actual Marks')
plt.plot(X, model.predict(X), color='red', label='Regression Line')
plt.xlabel("Hours Studied")
plt.ylabel("Marks Scored")
plt.title("Simple Linear Regression – Marks Prediction")
plt.legend()
plt.show()
```

## Output
<img width="840" height="618" alt="image" src="https://github.com/user-attachments/assets/d454899c-475a-4ec9-81ea-95d1af662f58" />


## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
