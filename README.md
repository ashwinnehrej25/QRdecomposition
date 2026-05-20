# Algorithm for QR Decomposition
## Aim:
To implement QR decomposition algorithm using the Gram-Schmidt method.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
```
1.Intialize the matrix Q and u
2.The vector u and e is given by
```
<img width="263" height="97" alt="ex4" src="https://github.com/user-attachments/assets/8b89fe26-1ef0-4770-9724-a7d97f791f0f" />
<img width="82" height="52" alt="ex6" src="https://github.com/user-attachments/assets/f0a7cc5c-1767-4249-94ad-90cb604f57cf" />
<img width="90" height="56" alt="ex3" src="https://github.com/user-attachments/assets/ee976b14-0c42-4894-94fb-d39fc67e14c7" />

3.Obtain the Q matrix

<img width="181" height="37" alt="ex1" src="https://github.com/user-attachments/assets/990f86fb-f714-4da7-89af-0a711940507c" />

4.Construct the upper triangular matrix R<img width="232" height="80" alt="ex2" src="https://github.com/user-attachments/assets/62e92340-60cc-4746-88fb-99d75b26bcb2" />



## Program:
```
'''
''' 
Program to QR decomposition using the Gram-Schmidt method
Developed by:K.Ashwin Nehrej
RegisterNumber: 212225220014
'''
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
import numpy as np
a = np.array(eval(input()),float)
n=a.shape[1]
q=np.zeros_like(a)
r=np.zeros((n,n))
for i in range(n):
    v=a[:,i]
    for j in range(i):
        r[j,i]=np.dot(q[:,j],a[:,i])
        v=v-r[j,i]*q[:,j]
    r[i,i]=np.linalg.norm(v)
    q[:,i]=v/r[i,i]
print("The Q Matrix is\n",q)
print("The R Matrix is\n",r)
```

## Output
<img width="1261" height="633" alt="image" src="https://github.com/user-attachments/assets/9c72857f-131c-446d-8a11-10ca39885fed" />




## Result
Thus the QR decomposition algorithm using the Gram-Schmidt process is written and verified the result.
