# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.

## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm:
### Step1
Import Pandas library.

### Step2
Import Linear_model from sklearn.
  
### Step3
Read the csv file using pandas library.

### Step4
Enter the parameters of the linear function.

### Step5
Print the parameters of the linear function.

## Program:
```
#Developed by: Mithun P
#Register number: 25008604

import pandas as pd
from sklearn import linear_model
df = pd.read_csv("carsemission.csv")
X = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:',regr.intercept_)
predictedCO2 = regr.predict([[3300, 1300]])
print('Predicted CO2 for the corresponding weight and volume',predictedCO2)

```
## Output:
<img width="1842" height="348" alt="image" src="https://github.com/user-attachments/assets/ec8406c9-f1e8-4266-a4f5-b00601994cff" />



## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
