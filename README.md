# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.

## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm:
### Step1
Get the independent variable X and dependent variable Y.

### Step2
Calculate the mean of the X -values and the mean of the Y -values.
  
### Step3
Find the slope m of the line of best fit using the formula. 
<img width="200" height="57" alt="image" src="https://github.com/user-attachments/assets/ce0881d0-3694-4f47-af5f-8644ff09cce6" />

### Step4
Compute the y -intercept of the line by using the formula: eqn2

### Step5
Use the slope m and the y -intercept to form the equation of the line.
Obtain the straight line equation Y=mX

## Program:
```
#Developed by: Mithun P
#Register number: 25008604

import pandas as pd
from sklearn import linear_model
df=pd.read_csv("car.csv")
x=df[['Weight','Volume']]
y=df['CO2']
regr=linear_model.LinearRegression()
regr.fit(x,y)
print('Coefficients:',regr.coef_)
print('Intercept:',regr.intercept_)
predictedCO2=regr.predict([[3300,1300]])
print('PredictedCO2 for the corresponding Weight and Volume : ',predictedCO2)

```
## Output:
'''
Coefficients: [0.00755095 0.00780526]
Intercept: 79.69471929115939
PredictedCO2 for the corresponding Weight and Volume :  [114.75968007]
'''

### Insert your output
<img width="828" height="392" alt="image" src="https://github.com/user-attachments/assets/59e34da1-a5d7-465f-8101-3d7269ce7930" />


## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
