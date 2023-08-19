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
## Loan data csv
```
import pandas as pd
df=pd.read_csv("/Loan_data.csv")
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
## Data set csv
```
import pandas as pd
df=pd.read_csv("/Data_set.csv")
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
# Output
## Data
```
import pandas as pd
df=pd.read_csv("/Loan_data.csv")
print(df)
df.head(10)
```
![261756098-5e950834-9ca4-4422-b9c9-920d6c7e662e](https://github.com/BejinB/ODD2023-Datascience-Ex01/assets/118367518/1f5f727f-56a3-4315-b32b-1078c12d4bc7)

## Non Null Before
```
df.info()
```
![261756451-174c518c-46ce-4737-a5bd-104a0bb7ff84](https://github.com/BejinB/ODD2023-Datascience-Ex01/assets/118367518/91de341a-93a8-4a2e-ab14-f39f116821cd)

## Mode
```
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()
```
![261756765-8856a967-f478-4c7c-87e9-3416e31cb4aa](https://github.com/BejinB/ODD2023-Datascience-Ex01/assets/118367518/3b1acd15-826e-4370-9686-b63aee9d4fb1)
## Mean
```
df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()
```
![261756933-b96d1f12-e128-48eb-8d4c-2b410e437b10](https://github.com/BejinB/ODD2023-Datascience-Ex01/assets/118367518/2392948d-0bc9-44d6-b8c5-bb554ca3ca06)
## Median
```
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()
```
![261757075-1ae6e95d-5752-4fa8-9376-0f40a89f9694](https://github.com/BejinB/ODD2023-Datascience-Ex01/assets/118367518/d8616629-7fdd-4788-b9ef-a04ac449fcfc)
## Non Null After
```
df.info()
```
![261757259-e0f9387e-170f-4c8c-9e64-bc9ac5ecd33a](https://github.com/BejinB/ODD2023-Datascience-Ex01/assets/118367518/cd25f2a2-c45f-4602-bb7a-b5ab51d79468)
```
df.isnull().sum()
```
![261757294-948461fd-dbef-4110-98a7-25d23af5858b](https://github.com/BejinB/ODD2023-Datascience-Ex01/assets/118367518/2e4de4ed-5d32-4299-9a18-0ffa8c93716a)
# For Data Set
## Data
```
import pandas as pd
df=pd.read_csv("/Data_set.csv")
print(df)
df.head(10)
```

![261757368-77d617c6-1167-4db1-a074-1bb62ded4062](https://github.com/BejinB/ODD2023-Datascience-Ex01/assets/118367518/9259e1a1-f90b-43ab-91db-81e4710b30a7)
## Non null before
```
df.info()
```
![261757395-8ab7f078-1843-4e49-83c2-356ac0653b32](https://github.com/BejinB/ODD2023-Datascience-Ex01/assets/118367518/6da33f55-4f67-4d6d-9bc7-f05f3a22b888)
```
df.isnull()
```
![261757541-97f25a5b-5524-4703-a20f-0f3d71bcae9f](https://github.com/BejinB/ODD2023-Datascience-Ex01/assets/118367518/7eed9837-4411-474c-a1c8-e80372c1dc16)

## Mode
```
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()
```

![261757947-1e4538f0-b049-4ae4-882f-2a0d1d8e8090](https://github.com/BejinB/ODD2023-Datascience-Ex01/assets/118367518/6e78ac4b-d293-4c06-9111-e3ec2e4397a7)

## Mean
```
df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
```
![261758246-1ee02f2b-cd0f-40da-96d1-07cb512c01ae](https://github.com/BejinB/ODD2023-Datascience-Ex01/assets/118367518/2d4e9535-84e3-4541-8ae8-517896c62ba6)

## Median
```
df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()
```
![261758573-492fc25f-09cd-4c49-a5b8-d9fae3f2c462](https://github.com/BejinB/ODD2023-Datascience-Ex01/assets/118367518/af041282-3949-4957-83bb-c362b3d877ba)
## Non null after
```
df.info()
```
![261758839-16a37c11-b4ac-4f75-bfed-39179e9f16e8](https://github.com/BejinB/ODD2023-Datascience-Ex01/assets/118367518/d2b502af-53e1-46ee-addb-a838ffbe5e2c)

```
 df.isnull()
```
![261759495-5da302fb-fc71-4baa-9566-24811ede6975](https://github.com/BejinB/ODD2023-Datascience-Ex01/assets/118367518/14dc9d24-b17e-4dbf-8121-f21f817305d8)
```
df.isnull().sum()
```
![261759676-e7d8752f-8504-4506-ae7f-d260d6bd8808](https://github.com/BejinB/ODD2023-Datascience-Ex01/assets/118367518/22ab4f88-bd24-444f-a4ea-bedbbc268d28)
# Result
Thus,the given data is read,cleansed and the cleaned data is saved into the file.


