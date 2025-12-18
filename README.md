# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
Devaloped BY:Bharathwaj P
Ref.no:25018022
```

import numpy as np
import matplotlib.pyplot as plt

# Given data
x = np.array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])
y = np.array([1, 3, 2, 5, 7, 8, 8, 9, 10, 12])

# Scatter plot of original data
plt.scatter(x, y)
plt.xlabel("X values")
plt.ylabel("Y values")
plt.title("Linear Regression from Scratch")
plt.show()

# Mean of x and y
x_mean = np.mean(x)
y_mean = np.mean(y)

# Calculate slope (m)
num = 0
den = 0
for i in range(len(x)):
    num += (x[i] - x_mean) * (y[i] - y_mean)
    den += (x[i] - x_mean) ** 2

m = num / den

# Calculate intercept (c)
c = y_mean - m * x_mean

print("Slope (m):", m)
print("Intercept (c):", c)

# Predicted y values
y_pred = m * x + c
print("Predicted y values:", y_pred)

# Plot regression line
plt.scatter(x, y)
plt.plot(x, y_pred, color="red")
plt.xlabel("X values")
plt.ylabel("Y values")
plt.title("Best Fit Line")
plt.show()





```
## Output

</br>
</br>
<img width="609" height="823" alt="image" src="https://github.com/user-attachments/assets/b880d1e5-b9b1-4a71-836d-694d93046ed2" />

</br>
</br>

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
