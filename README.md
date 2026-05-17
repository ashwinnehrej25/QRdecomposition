# Algorithm for QR Decomposition
## Aim:
To implement QR decomposition algorithm using the Gram-Schmidt method.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
```
1. Get the input matrix using np.array()   
2. Find the 2-norm of the matrix using np.linalg.norm()
3. Print the norm of the matrix in two decimal places.
```

## Program:
```
'''
Program to find 2-norm of a matrix.
Developed by: K.Ashwin Nehrej
RegisterNumber: 212225220014
'''
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
import numpy as np

A = np.array(eval(input()))

one_norm = np.linalg.norm(A, 1)

print(f"{one_norm:.2f}")
```
```
'''
Program to find 2-norm of a matrix.
Developed by:K.Ashwin Nehrej
RegisterNumber: 212225220014
'''
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
import numpy as np

A = np.array(eval(input()))

l2_norm = np.linalg.norm(A, 2)

print(f"{l2_norm:.2f}")
```
```
'''
Program to find 2-norm of a matrix.
Developed by:K.Ashwin Nehrej
RegisterNumber: 212225220014
'''
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
A = eval(input())

max_sum = 0

for row in A:
    row_sum = sum(abs(x) for x in row)
    if row_sum > max_sum:
        max_sum = row_sum

print(f"{max_sum:.2f}")
```

## Output
1-Norm of a Matrix
<img width="1277" height="378" alt="image" src="https://github.com/user-attachments/assets/b440435a-3ca7-46d9-af92-a959f14970aa" />
2-Norm of a Matrix
<img width="1308" height="459" alt="image" src="https://github.com/user-attachments/assets/9aaadc0a-eb69-4bde-9b77-208fe7e8028d" />
Infinity Norm of a Matrix

<img width="1285" height="369" alt="image" src="https://github.com/user-attachments/assets/486adbe2-c390-4989-bf2e-ffa95f249033" />




## Result
Thus the QR decomposition algorithm using the Gram-Schmidt process is written and verified the result.
