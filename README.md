# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:

Import the required libraries and read the dataset carsemission.csv using pandas.


Select Weight and Volume as input variables (X) and CO2 as output variable (y).


Create and train the Linear Regression model using LinearRegression() and fit() method.


Give new input values (Weight = 3300, Volume = 1300) and predict the CO2 emission using predict() method, then display the result.



## Program:

```
import pandas as pd
from sklearn import linear_model
df = pd.read_csv("carsemission.csv")
X = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:', regr.intercept_)
input_data = pd.DataFrame({'Weight': [3300], 'Volume': [1300]})
predictedCO2 = regr.predict(input_data)
print('Predicted CO2 for the corresponding weight and volume:', predictedCO2)

```
## Output:

<img width="1451" height="613" alt="image" src="https://github.com/user-attachments/assets/76b88ba0-a649-4e73-9e33-0d5a326296df" />

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
