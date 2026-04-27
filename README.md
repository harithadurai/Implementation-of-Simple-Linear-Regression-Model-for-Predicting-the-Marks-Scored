# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.  Import required libraries and prepare the dataset (X and Y values).
2.  Create and train the simple linear regression model using the dataset.
3.  Accept input (hours studied) and predict the marks using the trained model.
4.  Display the predicted result and visualize the data using a graph.
   

## Program:
```
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: D.HARITHA
RegisterNumber:  212225040118
*/
```
```
import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression
X = np.array([1, 2, 3, 4, 5]).reshape(-1, 1)
Y = np.array([35, 50, 65, 70, 85])

model = LinearRegression()

model.fit(X, Y)

m = model.coef_[0]
b = model.intercept_

print("Slope (m):", m)
print("Intercept (b):", b)

x_input = float(input("Enter hours studied: "))
predicted_marks = model.predict([[x_input]])
print("Predicted Marks:", predicted_marks[0])

Y_pred = model.predict(X)

plt.scatter(X, Y, label="Actual Data")
plt.plot(X, Y_pred, label="Regression Line")
plt.xlabel("Hours Studied")
plt.ylabel("Marks Scored")
plt.title("Simple Linear Regression (Using sklearn)")
plt.legend()
plt.show()
```

## Output:
![simple linear regression model for predicting the marks scored](sam.png)
<img width="772" height="637" alt="image" src="https://github.com/user-attachments/assets/e8c217bd-d093-4a5d-83be-4a55d21b9005" />



## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
