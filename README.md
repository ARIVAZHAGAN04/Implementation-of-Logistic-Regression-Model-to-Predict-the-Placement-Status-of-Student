# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the standard libraries such as pandas module to read the corresponding csv file.
2. Upload the dataset values and check for any null or duplicated values using .isnull() and .duplicated() function respectively.
3. Import LabelEncoder and encode the corresponding dataset values.
4. Import LogisticRegression from sklearn and apply the model on the dataset using train and test values of x and y and Predict the values of array using the variable y_pred. 5.Calculate the accuracy, confusion and the classification report by importing the required modules such as accuracy_score, confusion_matrix and the classification_report from sklearn.metrics module. 6.Apply new unknown values and print all the acqirred values for accuracy, confusion and the classification report.

## Program:

/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by: Arivazhagan G R
RegisterNumber:  212223040020
*/
```
import pandas as pd
data=pd.read_csv('Placement_Data.csv')
data.head()


data1=data.copy()
data1=data1.drop(["sl_no","salary"],axis = 1)#removes the specified row or column
data1.head()


data1.isnull().sum()


data1.duplicated().sum()


from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data1["gender"] = le.fit_transform(data1["gender"])
data1["ssc_b"] = le.fit_transform(data1["ssc_b"])
data1["hsc_b"] = le.fit_transform(data1["hsc_b"])
data1["hsc_s"] = le.fit_transform(data1["hsc_s"])
data1["degree_t"] = le.fit_transform(data1["degree_t"])
data1["workex"] = le.fit_transform(data1["workex"])
data1["specialisation"] = le.fit_transform(data1["specialisation"])
data1["status"] = le.fit_transform(data1["status"])
data1


x=data1.iloc[:,:-1]
x


y=data1["status"]
y


from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size = 0.2,random_state = 0)


from sklearn.linear_model import LogisticRegression
lr = LogisticRegression(solver = "liblinear")# a library for large
lr.fit(x_train,y_train)
y_pred = lr.predict(x_test)
y_pred
*/
```

## Output:
![the Logistic Regression Model to Predict the Placement Status of Student](sam.png)

![316213643-8b61269a-4626-484e-a1d9-54f2da9b7ab0](https://github.com/ARIVAZHAGAN04/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/161414455/0dd4df34-42c6-41a8-9943-fcecacf5dd18)

![316213689-36f6c46f-8248-49cc-986d-73a16ea24a49](https://github.com/ARIVAZHAGAN04/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/161414455/d7d83bb6-6259-4a8c-b7e6-a080dc65af4e)

![316213696-d6a44ea7-0dd1-4b4a-b1bc-54966a45d81d](https://github.com/ARIVAZHAGAN04/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/161414455/121d8e11-f336-49d5-960b-ba241ea49b8b)

![316213772-0da214d5-6ba3-47d6-b3c3-2fa1a9d99076](https://github.com/ARIVAZHAGAN04/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/161414455/c22fe549-0e20-41f5-af9b-cb01b30ad4b6)

![316213779-ac4e38bc-8f27-441b-9f87-77087a1fc0a2](https://github.com/ARIVAZHAGAN04/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/161414455/400e78b0-334a-4c15-a92f-6bd98ecbbb28)

![316213785-b692df9f-ea78-432d-8f6e-4d7da3c5d2cf](https://github.com/ARIVAZHAGAN04/Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student/assets/161414455/340e4604-43b4-4ef5-9f44-cd3d9163209e)





## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
