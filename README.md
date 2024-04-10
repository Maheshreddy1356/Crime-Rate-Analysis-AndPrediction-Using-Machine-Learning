# INTRODUCTION:
"CRIME RATE ANALYSIS AND PREDICTION USING MACHINE LEARNING"

[
![image](https://github.com/Maheshreddy1356/Crime-Rate-Analysis-AndPrediction-Using-Machine-Learning/assets/123810091/0d0dff6f-815b-4716-ad3a-1e11711cdf77)
](url)

# Libraries used in this Project:
[
![image](https://github.com/Maheshreddy1356/Crime-Rate-Analysis-AndPrediction-Using-Machine-Learning/assets/123810091/2051a31a-6242-4ef7-8d20-bd6f3d997a9f)
](url)

[
![image](https://github.com/Maheshreddy1356/Crime-Rate-Analysis-AndPrediction-Using-Machine-Learning/assets/123810091/ab799e8b-1ea7-4573-b18f-4ae52e2ee7cd)
](url)
# Domain --->
[
![image](https://github.com/Maheshreddy1356/Crime-Rate-Analysis-AndPrediction-Using-Machine-Learning/assets/123810091/83901c4b-722c-47ee-908a-42bad2b322fa)
](url)
# Accuracy --->
[
![image](https://github.com/Maheshreddy1356/Crime-Rate-Analysis-AndPrediction-Using-Machine-Learning/assets/123810091/5584d84d-38ae-4d92-9812-a92c1db91dcc)
](url)   [
![image](https://github.com/Maheshreddy1356/Crime-Rate-Analysis-AndPrediction-Using-Machine-Learning/assets/123810091/4d53ba70-9859-4a00-8cc8-403500712b49)
](url)     [
![image](https://github.com/Maheshreddy1356/Crime-Rate-Analysis-AndPrediction-Using-Machine-Learning/assets/123810091/f4cce7f4-92bc-4c6a-b658-ab339cf12d0f)
](url)       [
![image](https://github.com/Maheshreddy1356/Crime-Rate-Analysis-AndPrediction-Using-Machine-Learning/assets/123810091/4d53ba70-9859-4a00-8cc8-403500712b49)
](url)     [
![image](https://github.com/Maheshreddy1356/Crime-Rate-Analysis-AndPrediction-Using-Machine-Learning/assets/123810091/7c533c1a-dde3-4853-b264-f443e5290d44)
](url)      [
![image](https://github.com/Maheshreddy1356/Crime-Rate-Analysis-AndPrediction-Using-Machine-Learning/assets/123810091/4f39aa44-36a2-4193-9ec4-09fd7de5bcb3)
](url)          <img width="960" alt="Screenshot 2024-04-10 230417" src="https://github.com/Maheshreddy1356/Crime-Rate-Analysis-AndPrediction-Using-Machine-Learning/assets/123810091/852e672d-3504-48ec-8d60-c5c86b6e048e">
# Module Descriptions --->

This project consists of six modules:

# 1.Data Collection Module:

Crime dataset from Kaggle is used in CSV format.

# 2.Data Preprocessing Module:

Before using libraries we have to import the libraries first.

import numpy as np

import pandas as pd

from matplotlib import pyplot as pt

d=pd.read_csv("crime.csv")

Load the data set by using pandas library and checks whether it has null values or not.

d.isnull().sum()

If the dataset consists of null values then we remove the null values in this module by using:

d=d.dropna()

# 3.Feature Selection Module:

Feature selection is done which can be used to build the model.The attributes used for feature selection  are Block,Location,District,etc.

![Screenshot 2024-04-11 004315](https://github.com/Maheshreddy1356/Crime-Rate-Analysis-AndPrediction-Using-Machine-Learning/assets/123810091/ad338f06-48af-41d6-a820-e6f13273aae5)


# 4.Building and Training Module:

After feature selection location and month attribute are used for training.The dataset is divided into pairs of X_train,Y_train,X_test,Y_test.

The algorithm model is imported from sklearn.

![Screenshot 2024-04-11 004251](https://github.com/Maheshreddy1356/Crime-Rate-Analysis-AndPrediction-Using-Machine-Learning/assets/123810091/2f47f914-4bbf-40f9-bd38-205d36f3dd30)


Building models is done using models. Fit(X_train,Y_train)

from sklearn.model_selection import train_test_split

X_train,X_tes,Y_train,Y_test = train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.ensemble import RandomForestClassifier

random_forest = RandomForestClassifier(n_estimators=100)

random_forest.fit(X_train,Y_train)

# 5.Prediction Module:

After the model is built using the above process,prediction is done using model.predict(X_test).

The accuracy is calculated using accuracy_score imported from metrics-metrics.accuracy_score(Y_test,pred).

pred=random_forest.predict(X_test)

from sklearn.metrics import accuracy_score,classification_report

acc = accuracy_score(pred,Y_test)

clf = classification_report(pred,Y_test)

# 6.Visualization Module:

Using matplotlib library from sklearn.Analysis of the crime dataset is done by plotting various graphs for best accuracy model.

from matplotlib import pyplot as plt;plt.rcdefaults()

objects = ('Random Forest','Logistic Regression','Support Vector')

y_pos = np.arange(len(objects))

performace = [acc1,acc2,acc3]

plt.bar(y_pos,performance,align='center',alpha=0.5)

plt.xticks(y_pos,objects)

plt.ylabel('Accuracy')

plt.title('RF vs LR vs SVM ')

plt.show()

<img width="960" alt="Screenshot 2024-04-10 230417" src="https://github.com/Maheshreddy1356/Crime-Rate-Analysis-AndPrediction-Using-Machine-Learning/assets/123810091/356ef19b-e3a2-4544-9135-693d65c77d27">

# Conclusion --->

This is focused on building predictive models for crime frequencies per crime type per year.

The proposed model is very useful for both investigating agencies and police officials in taking necessary steps to reduce crime.

This project helps to analyze the crime networks  by means of various interactive visualizations.











