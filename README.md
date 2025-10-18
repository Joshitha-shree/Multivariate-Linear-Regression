# Implementation of Multivariate Linear Regression
## Developed By:JOSHITHA SHREE BS
## Register Number:212224230107

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
import numpy as np
import matplotlib.pyplot as plt
x = np.array([0,1,2,3,4,5,6,7,8,9])
y = np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(x,y)
plt.show()
xmean = np.mean(x)
ymean = np.mean(y)
num=0
den=0
for i in range(len(x)):
    num+=(x[i]-xmean)*(y[i]-ymean)
    den+=(x[i]-xmean)**2
m = num/den
b = ymean - m*xmean
print(m,b)
ypred = m*x+b
print(ypred)

plt.scatter(x,y,color='Red')
plt.plot(x,ypred,color='Blue')
plt.show()





```
## Output:

### Insert your output

<img width="960" height="403" alt="image" src="https://github.com/user-attachments/assets/2f5bf288-0b6c-4338-87ab-5f99b8d2a756" />



## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
