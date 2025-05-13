# Word-Count
## AIM:
To write a python program for getting the word count from a text.
## EQUIPEMENT'S REQUIRED: 
PC
Anaconda - Python 3.7
## ALGORITHM: 
### Step 1:  
Import the required libraries: `pandas` for data manipulation and `linear_model` from `sklearn` for regression.  

### Step 2:  
Load the dataset using `pd.read_csv()` and store it in a DataFrame.

### Step 3:  
Separate the features (independent variables) and the target (dependent variable):  
- Assign the relevant columns to `X` (features).  
- Assign the target column to `y` (output).  

### Step 4:  
Create a linear regression model using `linear_model.LinearRegression()` and fit it to the data using `regr.fit(X, y)`.  

### Step 5:  
Print the regression coefficients (`regr.coef_`) and intercept (`regr.intercept_`).  

### Step 6:  
Use the trained model to make predictions using `regr.predict()` with the given input values.  

### Step 7:  
Display the predicted output.

## PROGRAM:
```python
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

### OUTPUT:

![Screenshot 2025-05-13 114446](https://github.com/user-attachments/assets/5e6884da-bc5c-44a4-8ae1-6c2b02b192e1)

## RESULT:
Thus the program is written to find the word count from a text.
