# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:

### Step 1: Import libraries and read the dataset

* Import the required libraries (`pandas` and `sklearn.linear_model`).
* Read the CSV file using `pd.read_csv()` to load the data into a DataFrame.

### Step 2: Select input and output variables

* Choose **independent variables (X)** — here, `Weight` and `Volume`.
* Choose the **dependent variable (Y)** — here, `CO2`.

### Step 3: Create and train the Linear Regression model

* Create a `LinearRegression()` object.
* Fit the model using `regr.fit(X, Y)` to find the best-fit line (plane).

### Step 4: Display model parameters

* Print the **coefficients** (`regr.coef_`) and **intercept** (`regr.intercept_`).
* These values form the regression equation.

### Step 5: Make predictions using the trained model

* Use `regr.predict([[3300,1300]])` to predict CO₂ for the given weight and volume.
* Print the predicted result.

## Program:
```
Developed by: LAAVANYA.R
RegisterNumber: 212224230135

import pandas as pd
from sklearn import linear_model
df = pd.read_csv(r"C:\Users\admin\Downloads\car (1).csv")
x = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(x, y)
print("Coefficients:", regr.coef_)
print("Intercept:", regr.intercept_)
predictedCO2 = regr.predict([[3300, 1300]])
print("Predicted CO2 for the corresponding weight and volume:", predictedCO2)

```
## Output:

<img width="1246" height="398" alt="image" src="https://github.com/user-attachments/assets/6bfd8ef1-b5cc-4e96-8109-4d3f2022e6dc" />


## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
