# Ex-01_DS_Data_Cleansing


## AIM
To read the given data and perform data cleaning and save the cleaned data to a file. 

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Get the information about the data
### STEP 3
Remove the null values from the data
### STEP 4
Save the Clean data to the file

# CODE 
## LOAN_DATA.CSV :
```python
import pandas as pd
df=pd.read_csv("Loan_data.csv")
print(df)
df.head(10)
df.info()
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()

df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()

df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()

df.info()
df.isnull().sum()
```
## DATA_SET.CSV :
```python
import pandas as pd
df=pd.read_csv("Data_set.csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()

df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()

df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()

df.info()
df.isnull()
df.isnull().sum()
```
# OUTPUT :
## FOR LOAN_DATA :
## DATA :
```python
import pandas as pd
df=pd.read_csv("Loan_data.csv")
print(df)
df.head(10)
```
![image](https://github.com/Hariharanashok/ODD2023-Datascience-Ex01/assets/120353431/9142d9e7-ab10-42d0-b4ba-a6ca0650e6f0)

## NON NULL BEFORE :
```python
df.info()
```
![image](https://github.com/Hariharanashok/ODD2023-Datascience-Ex01/assets/120353431/88e51be9-c510-48cb-828d-64c29276f9ec)

## MODE :
```python
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()
```
![Mode - loandata](https://github.com/Hariharanashok/ODD2023-Datascience-Ex01/assets/120353431/86e01dc0-d347-4f4b-860f-c20271f54989)

## MEAN :
```python
df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()
```
![image](https://github.com/Hariharanashok/ODD2023-Datascience-Ex01/assets/120353431/76c552d9-2e67-4101-886a-65f9d013beb5)

## MEDIAN :
```python
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()
```
![image](https://github.com/Hariharanashok/ODD2023-Datascience-Ex01/assets/120353431/4fa7a2e8-6468-426e-9d22-46b9099e8eca)

## NON NULL AFTER :
```python
df.info()
```
![image](https://github.com/Hariharanashok/ODD2023-Datascience-Ex01/assets/120353431/4d8429f3-7089-4684-bea7-3b3c7920329d)

```python
df.isnull().sum()
```
![image](https://github.com/Hariharanashok/ODD2023-Datascience-Ex01/assets/120353431/7519607c-c42e-46d7-842c-35b27845861c)

# FOR DATA_SET :
## DATA :
```python
import pandas as pd
df=pd.read_csv("Data_set.csv")
print(df)
df.head(10)
```
![EX 1 data output](https://github.com/Hariharanashok/ODD2023-Datascience-Ex01/assets/120353431/6a6398b4-2ee0-4671-a97c-fd116055eb7b)

## NON NULL BEFORE :
```python
df.info()
```
![image](https://github.com/Hariharanashok/ODD2023-Datascience-Ex01/assets/120353431/a3a5331b-8d61-44fb-a372-dc10200b022c)

```python
df.isnull()
```
![image](https://github.com/Hariharanashok/ODD2023-Datascience-Ex01/assets/120353431/728ad867-83a9-4c79-9901-5f3b57a2e383)

```python
df.isnull().sum()
```
![image](https://github.com/Hariharanashok/ODD2023-Datascience-Ex01/assets/120353431/b2b92ccb-6d8e-494b-be7e-bc2ddf16f46d)

## MODE :
```python
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()
```
![image](https://github.com/Hariharanashok/ODD2023-Datascience-Ex01/assets/120353431/6dab2484-d96a-4db7-b511-2b7d021fc215)

## MEAN :
```python
df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
```
![image](https://github.com/Hariharanashok/ODD2023-Datascience-Ex01/assets/120353431/10813f8e-52e2-4a08-afd3-e5d54a2c5cda)

## MEDIAN :
```python
df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()
```
![image](https://github.com/Hariharanashok/ODD2023-Datascience-Ex01/assets/120353431/81220334-5617-47d4-ab81-f9cbdd6eb9e8)

## NON NULL AFTER :
```python
df.info()
```
![image](https://github.com/Hariharanashok/ODD2023-Datascience-Ex01/assets/120353431/36f2412d-4970-4dd5-bf08-3779a2e2a010)

```python
df.isnull()
```
![image](https://github.com/Hariharanashok/ODD2023-Datascience-Ex01/assets/120353431/b9c0fd07-35ca-43d4-b088-22a71952aca1)

```python
df.isnull().sum()
```
![image](https://github.com/Hariharanashok/ODD2023-Datascience-Ex01/assets/120353431/7e348dfc-10cd-4c6e-9e71-7c5cb475c4da)

# RESULT :
Thus,the given data is read,cleansed and the cleaned data is saved into the file.







