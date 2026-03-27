# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm

STEP 1: Read the number of unknowns and initialize zero arrays for the augmented matrix and the solution vector.

STEP 2: Read the coefficients of the augmented matrix from the user input.

STEP 3: Perform forward elimination to transform the augmented matrix into an upper triangular matrix by making the elements below the main diagonal zero.

STEP 4: Apply back substitution to calculate the values of the unknowns from the last row upwards and print the final solution.

## Program:
```
import numpy as np
import sys

# Reading number of unknowns
n = int(input())

# Making numpy array of n x n+1 size and initializing 
# to zero for storing augmented matrix
a = np.zeros((n,n+1))

# Making numpy array of n size and initializing 
# to zero for storing solution vector
x = np.zeros(n)

# Reading augmented matrix coefficients
for i in range(n):
    for j in range(n+1):
        a[i][j] = float(input())

# Applying Gauss Elimination
for i in range(n):
    if a[i][i] == 0.0:
        sys.exit('Divide by zero detected!')
        
  for j in range(i+1, n):
        ratio = a[j][i]/a[i][i]
        
or k in range(n+1):
            a[j][k] = a[j][k] - ratio * a[i][k]

# Back Substitution
x[n-1] = a[n-1][n]/a[n-1][n-1]

for i in range(n-2,-1,-1):
    x[i] = a[i][n]
    
  for j in range(i+1,n):
        x[i] = x[i] - a[i][j]*x[j]
    
   x[i] = x[i]/a[i][i]

# Displaying solution
for i in range(n):
    print('X%d = %0.2f' %(i,x[i]), end = ' ')
```

## Output:

<img width="1235" height="553" alt="image" src="https://github.com/user-attachments/assets/1c503f3c-b228-4c38-8357-3524949caf7b" />


<img width="1273" height="728" alt="image" src="https://github.com/user-attachments/assets/72335d23-f262-45cc-a21a-fd195da949ef" />


<img width="1419" height="336" alt="image" src="https://github.com/user-attachments/assets/e6fc3169-df85-4f36-a184-ccc5d9c2b3d5" />




## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

