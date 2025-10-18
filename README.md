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

<img width="737" height="588" alt="image" src="https://github.com/user-attachments/assets/d54768cc-2fe7-4455-b4a2-3a4222d97839" />


<img width="728" height="507" alt="image" src="https://github.com/user-attachments/assets/4609603b-b92c-418a-95df-d67a0ab16b0a" />



## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
