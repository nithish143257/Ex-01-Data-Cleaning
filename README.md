# Ex-01_DS_Data_Cleansing
# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Get the information about the data

## STEP 3
Remove the null values from the data

## STEP 4
Save the Clean data to the file

# CODE

# dataset
```

import pandas as pd
import numpy as np
data=pd.read_csv("/content/Data_set.csv")
data.head()
data.info()
data.isnull()
data.isnull().sum()
data['show_name']=data['show_name'].fillna(data['aired_on'].mode()[0])
data['aired_on']=data['show_name'].fillna(data['aired_on'].mode()[0])
data['original_network']=data['original_network'].fillna(data['aired_on'].mode()[0])
data.head()
data['rating']=data['rating'].fillna(data['rating'].mean())
data['current_overall_rank']=data['current_overall_rank'].fillna(data['current_overall_rank'].mean())
data.head()
data['watchers']=data['watchers'].fillna(data['watchers'].mean())
data.head()
data.info()
data.isnull().sum()
```

# Loan
```

import pandas as pd
import numpy as np
import seaborn as snb
df = pd.read_csv("/content/Loan_data.csv")
df.head(5)
df.info()
df.isnull().sum()
df['Gender'] = df["Gender"].fillna(df['Gender'].mode()[0])
df['Dependents'] = df["Dependents"].fillna(df['Dependents'].mode()[0])
df['Self_Employed'] = df["Self_Employed"].fillna(df['Self_Employed'].mode()[0])
df['Credit_History'] = df["Credit_History"].fillna(df['Credit_History'].mode()[0])
df.head()
df['Loan_Amount_Term'] = df["Loan_Amount_Term"].fillna(df['Loan_Amount_Term'].mean())
df.head()
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].median())
df.head()
df.info()
df.isnull().sum()

```

# OUPUT

# Dataset
![Data Cleaning](./images/img.jpeg)

![Data Cleaning](./images/img1.jpeg)

![Data Cleaning](./images/img2.jpeg)

![Data Cleaning](./images/img3.jpeg)

![Data Cleaning](./images/img4.jpeg)

# Loan

![Data Cleaning](./images/img7.jpeg)

![Data Cleaning](./images/img9.jpeg)

![Data Cleaning](./images/img10.jpeg)

![Data Cleaning](./images/img11.jpeg)

# Result 
Thus ,the given data is read,cleansed and the cleaned data is saved into file.
