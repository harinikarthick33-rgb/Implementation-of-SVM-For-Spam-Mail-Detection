# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Read the dataset Load the spam.csv file and select the message and label columns. 2.Preprocess the data Convert labels (ham, spam) into numeric values (0, 1) and transform text messages into numerical features using TF-IDF. 3.Split the dataset Divide the data into training data and testing data using train_test_split(). 4.Train the SVM model Create the SVM classifier and train it using the training dataset. 5.Predict and evaluate Predict spam/ham messages for test data and display the confusion matrix using a heatmap graph. 


## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.feature_extraction.text import TfidfVectorizer
from sklearn.svm import SVC
from sklearn.metrics import confusion_matrix
import matplotlib.pyplot as plt
import seaborn as sns

data = pd.read_csv("spam.csv", encoding='latin-1')

data = data[['v1','v2']]
data.columns = ['label','message']

data['label'] = data['label'].map({'ham':0, 'spam':1})

X = data['message']
y = data['label']

vectorizer = TfidfVectorizer(stop_words='english')
X_vectorized = vectorizer.fit_transform(X)


X_train, X_test, y_train, y_test = train_test_split(
    X_vectorized, y, test_size=0.2, random_state=42)


model = SVC(kernel='linear')
model.fit(X_train, y_train)

y_pred = model.predict(X_test)

cm = confusion_matrix(y_test, y_pred)

plt.figure(figsize=(5,4))
sns.heatmap(cm, annot=True, fmt='d', cmap='Blues',
            xticklabels=['Ham','Spam'],
            yticklabels=['Ham','Spam'])

plt.xlabel("Predicted")
plt.ylabel("Actual")
plt.title("Confusion Matrix for SVM Spam Detection")
plt.show()
Developed by: Rachanaa.R
RegisterNumber: 212225040322 
*/
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: Harini V K
RegisterNumber:  212225220036
*/


## Output:
<img width="817" height="595" alt="image" src="https://github.com/user-attachments/assets/185486ad-2d7f-40e8-85de-c78f798969d8" />


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
