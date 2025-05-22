# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the necessary python packages using import statements.

2.Read the given csv file using read_csv() method and print the number of contents to be displayed using df.head().

3.Split the dataset using train_test_split.

4.Calculate Y_Pred and accuracy.

5.Print all the outputs.

6.End the Program.

## Program and Output:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: M.V.Vamsidhar Reddy
RegisterNumber: 212224040205

import chardet
file='spam.csv'
with open (file,'rb') as rawdata:
    result = chardet.detect(rawdata.read(100000))
result
import pandas as pd
data=pd.read_csv("spam.csv",encoding='windows-1252')
data.head()
```
![image](https://github.com/user-attachments/assets/cb03e943-02fc-4f36-a81c-ad3e5dead0e9)


```
data.info()
```
![image](https://github.com/user-attachments/assets/145af677-8d97-456c-959f-c752490dbff7)


```
data.isnull().sum()
```
![image](https://github.com/user-attachments/assets/14ca0be9-88b7-406d-9400-b6ecb7ce7f81)


```
x=data["v1"].values
y=data["v2"].values
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
from sklearn.feature_extraction.text import CountVectorizer
cv=CountVectorizer()
x_train=cv.fit_transform(x_train)
