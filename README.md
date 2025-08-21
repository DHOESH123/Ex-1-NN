<H3>ENTER YOUR NAME</H3>
<H3>ENTER YOUR REGISTER NO.</H3>
<H3>EX. NO.1</H3>
<H3>DATE</H3>
<H1 ALIGN =CENTER> Introduction to Kaggle and Data preprocessing</H1>

## AIM:

To perform Data preprocessing in a data set downloaded from Kaggle

## EQUIPMENTS REQUIRED:
Hardware – PCs
Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook

## RELATED THEORETICAL CONCEPT:

**Kaggle :**
Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

**Data Preprocessing:**

Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis.
Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

**Need of Data Preprocessing :**

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set.
Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.


## ALGORITHM:
STEP 1:Importing the libraries<BR>
STEP 2:Importing the dataset<BR>
STEP 3:Taking care of missing data<BR>
STEP 4:Encoding categorical data<BR>
STEP 5:Normalizing the data<BR>
STEP 6:Splitting the data into test and train<BR>

##  PROGRAM:
```py
import pandas as pd
df1=pd.read_csv('/content/Churn_Modelling (3).csv')
df1
df1.head()
df1.tail()
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
scaler=StandardScaler()
numerical_cols1=['RowNumber', 'CustomerId', 'CreditScore', 'Age', 'Tenure', 'Balance', 'NumOfProducts', 'HasCrCard',
       'IsActiveMember', 'EstimatedSalary']
df1[numerical_cols1]=scaler.fit_transform(df[numerical_cols1])
df1
from sklearn.preprocessing import LabelEncoder
df1.drop('Surname',inplace=True,axis=1)
le=LabelEncoder()
df1['Geography']=le.fit_transform(df1['Geography'])
df1['Gender']=le.fit_transform(df1['Gender'])
df1
x=df1.drop('Exited',axis=1)
y=df1['Exited']
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=42)
print(x_train)
print(x_test)

```


## OUTPUT:
<img width="1446" height="615" alt="image" src="https://github.com/user-attachments/assets/656290f4-cff8-465d-9623-1502599c52b7" />
<img width="1403" height="330" alt="image" src="https://github.com/user-attachments/assets/8cee1d5d-9e41-46a1-bbeb-2c227a2e8fcf" />
<img width="1390" height="435" alt="image" src="https://github.com/user-attachments/assets/26220df7-19b4-45af-9fad-e01e11be91a2" />
<img width="779" height="535" alt="image" src="https://github.com/user-attachments/assets/5ec3fc64-8a53-4d61-bafd-17f595193334" />
<img width="405" height="647" alt="image" src="https://github.com/user-attachments/assets/e6f966bf-dc69-4a11-bd90-ac9ab5365d4b" />
<img width="1020" height="132" alt="image" src="https://github.com/user-attachments/assets/e7051c1f-0a24-4587-9174-4caf070e7244" />
<img width="1445" height="588" alt="image" src="https://github.com/user-attachments/assets/e9c52c03-8b4f-4b18-aeec-a7d24a43adb0" />
<img width="1425" height="578" alt="image" src="https://github.com/user-attachments/assets/fe3934ff-e06d-41f5-93c0-096d74ed07ea" />
<img width="1059" height="632" alt="image" src="https://github.com/user-attachments/assets/3579c2ac-8502-4493-8473-ae40a9840b38" />
<img width="709" height="325" alt="image" src="https://github.com/user-attachments/assets/1808abcd-15f8-4c57-9c2b-d71e4b703306" />
<img width="1009" height="660" alt="image" src="https://github.com/user-attachments/assets/768b9465-4dd1-4455-bc4e-d7af8dde8a76" />
<img width="496" height="369" alt="image" src="https://github.com/user-attachments/assets/19489a0f-6a4b-4dd1-b3d3-546c2004b84e" />














## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


