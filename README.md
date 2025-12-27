# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.Input matrix dimensions and initialize augmented matrix and solution vector.

2.Populate the augmented matrix with user inputs.

3.Perform Gaussian elimination to reduce the matrix to upper triangular form, ensuring no division by zero.

4.Back substitute to compute solution values for the variables.

5.Print the solution vector formatted to two decimal places.



## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by:PRIYADHARSHAN.U
RegisterNumber:25017406
import numpy as np
def gauss_elimination(A,b):
    n = len(b)
    for k in range(n):
        if A[k][k] == 0:
            raise ValueError("Zero pivot encountered!")
        for i in range(k+1,n):
            factor=A[i][k]/A[k][k]
            for j in range(k,n):
                A[i][j] = A[i][j]-factor*A[k][j]
            b[i] = b[i]-factor*b[k]
    x=[0]*n
    for i in range(n-1,-1,-1):
        sum_ax = 0
        for j in range(i+1,n):
            sum_ax += A[i][j]*x[j]
        x[i] = (b[i]-sum_ax)/A[i][i]
    return x
a=int(input())
list2=[]
for i in range(a):
    list1=[]
    for j in range(a+1):
        b=int(input())
        list1.append(b)
    list2.append(list1)
list2=np.array(list2)
A=list2[:,:3]
b=list2[:,3]
x=gauss_elimination(A,b)
print(f"X0 = {x[0]:.2f} X1 = {x[1]:.2f} X2 = {x[2]:.2f}")

*/
```

## Output:
<img width="1919" height="905" alt="Screenshot 2025-12-27 134700" src="https://github.com/user-attachments/assets/6ef88e0e-8095-464c-8a34-edfe91d8161d" />


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

