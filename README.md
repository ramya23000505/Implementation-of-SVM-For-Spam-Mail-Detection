# Implementation-of-SVM-For-Spam-Mail-Detection
### Date:
## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
Step 1. Start the Program.

Step 2. Import the necessary packages.

Step 3. Read the given csv file and display the few contents of the data.

Step 4. Assign the features for x and y respectively.

Step 5. Split the x and y sets into train and test sets.

Step 6. Convert the Alphabetical data to numeric using CountVectorizer.

Step 7. Predict the number of spam in the data using SVC (C-Support Vector Classification) method of SVM (Support vector machine) in sklearn library.

Step 8. Find the accuracy of the model.

Step 9. End the Program.
## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: Ramya R
RegisterNumber:  212223230169
*/

import pandas as pd
data=pd.read_csv("Exp_11_spam.csv",encoding='windows-1252')

data.head()

dat.info()

data.isnull().sum()

x=data["v1"].values

y=data["v2"].values

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test= train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.feature_extraction.text import CountVectorizer
#CountVectorizer is a method to convert text to numerical data. The text is transformed to a sparse matrix
cv=CountVectorizer()

x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)

from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred

from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
```

## Output:
### Head Function:
![Screenshot 2024-10-24 090736](https://github.com/user-attachments/assets/8787566b-17b1-4fdf-b353-47a71c93e5c5)

### Data Information:
![Screenshot 2024-10-24 090745](https://github.com/user-attachments/assets/5587d8a2-d17c-4c83-abd5-29cdcd5d6b89)

### Y-Predict
![Screenshot 2024-10-24 090715](https://github.com/user-attachments/assets/32c2360d-c7d3-43b8-84c5-38d72ca79693)

### Accuracy:
![Screenshot 2024-10-24 090721](https://github.com/user-attachments/assets/ac19cb9c-7be5-4198-9f6b-0146383ec0cf)


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
