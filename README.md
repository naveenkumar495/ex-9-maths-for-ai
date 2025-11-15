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
```python
#Done By
#Reg NO: 212224230183
#Name: NAVEENKUMAR M

import numpy as np
x=np.array(eval(input()))
y=np.array(eval(input()))
mean_x=np.mean(x)
mean_y=np.mean(y)
num,den=0,0
for i in range(len(x)):
    num+=(x[i]-mean_x)*(y[i]-mean_y)
    den+=(x[i]-mean_x)**2
m=num/den
c=mean_y-m*mean_x
print("m:",m,"\nc:",c)
y_pred=m*x+c
print(y_pred)
import matplotlib.pyplot as plt
plt.scatter(x,y,color="red")
plt.plot(x,y_pred,color="blue")
plt.show()
```
## Output
<img width="1019" height="595" alt="image" src="https://github.com/user-attachments/assets/ecd5de22-f936-48b5-90ad-b4259504e0ae" />
<img width="1022" height="827" alt="image" src="https://github.com/user-attachments/assets/629d8ac5-d586-4a60-ad55-bc538b677a4e" />


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
