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
```
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

df.isnull().sum()

```
# OUPUT
# DATA:

![ex 1 png](https://user-images.githubusercontent.com/119559827/227534422-37ce09c4-d4c2-4587-b797-53f477dad7de.png)
![2](https://user-images.githubusercontent.com/119559827/227535217-04ef81ee-f09f-4e9c-86b5-ba46f2bfd923.png)
![3](https://user-images.githubusercontent.com/119559827/227535419-72881ada-ac4e-4592-a73c-9629c963f295.png)
![4](https://user-images.githubusercontent.com/119559827/227535551-87e006fd-33a2-4f41-bfe0-ead15eaecfe0.png)
![5](https://user-images.githubusercontent.com/119559827/227535598-cd2855a0-6c4a-4bd8-99c4-ff111375524d.png)
![6](https://user-images.githubusercontent.com/119559827/227535645-ab1efac7-d4fb-4079-8866-4f9786539212.png)
![7](https://user-images.githubusercontent.com/119559827/227535676-50e121f4-4eda-4562-bfeb-29f841b11e10.png)

# RESULT
Thus, the given data is read, cleansed and the cleaned data is saved into the file



