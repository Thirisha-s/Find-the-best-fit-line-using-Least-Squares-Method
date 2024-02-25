# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program and Output:

Program to implement univariate Linear Regression to fit a straight line using least squares.

Developed by: THIRISHA.S

RegisterNumber: 212222230160

```python
import numpy as np
x=np.array(eval(input()))
y=np.array(eval(input()))
```

<img width="74" alt="image" src="https://github.com/TejaswiniGugananthan/Find-the-best-fit-line-using-Least-Squares-Method/assets/121222763/354fa063-e650-4eb0-9662-aafe6424bf16">

```python
x_mean=np.mean(x)
y_mean=np.mean(y)
num=0
denom=0
for i in range(len(x)):
    num+=(x[i]-x_mean)*(y[i]-y_mean)
    denom+=(x[i]-x_mean)**2
m=num/denom
b=y_mean-m*x_mean
print("slope: ",m)
print("y-intercept: ",b)
y_predict=m*x+b
```

<img width="121" alt="image" src="https://github.com/TejaswiniGugananthan/Find-the-best-fit-line-using-Least-Squares-Method/assets/121222763/902bad3d-6574-4fec-b830-89c76b8999d6">

```python
import matplotlib.pyplot as plt
plt.scatter(x,y)
plt.plot(x,y_predict,color='blue')
```

<img width="375" alt="image" src="https://github.com/TejaswiniGugananthan/Find-the-best-fit-line-using-Least-Squares-Method/assets/121222763/bdba84f4-f681-4c91-8a07-4d1c9febea8c">



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
