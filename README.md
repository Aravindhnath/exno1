# Exno:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# 1) Read and display DataFrame
```
import pandas as pd
df=pd.read_csv('/content/SAMPLEDS.csv')
df
```
## OUTPUT:
![Output](Op1-ds1.png)

## 2) Display head
```
df.head()
```
## OUTPUT:
![Output](Op2-ds1.png)

## 3) Display tail
```
df.tail()
```
## OUTPUT:
![Output](Op3-ds1.png)

## 4) Info of dataframe
```
df.info()
```
## OUTPUT:
![Output](Op4-ds1.png)

## 5) Describe about the dataframe
```
df.describe()
```
## OUTPUT:
![Output](Op5-ds1.png)

## 6) Shape of the dataframe
```
df.shape
```
## OUTPUT:
![Output](Op6-ds1.png)

## 7) Checking tha NUll values
```
df.isnull().sum()
```
## OUTPUT:
![Output](Op7-ds1.png)

## 8) Drop the Null values
```
x=df.dropna(how='any')
x
```
## OUTPUT:
![Output](Op8-ds1.png)

## 9) Drop the Null values in Total
```
tot=df.dropna(subset=['TOTAL'],how='any')
tot
```
## OUTPUT:
![Output](Op9-ds1.png)

## 10) FIll the Null values
```
df.fillna(0)
```
## OUTPUT:
![Output](Op10-ds1.png)

## 11) Finding the mean value
```
mn=df.TOTAL.mean()
mn
```
## OUTPUT:
![Output](Op11-ds1.png)

## 12) Final output
```
for x in df.index:
  if df.loc[x,"AVG"]>100:
    df.drop(x,inplace=True)
df
```
## OUTPUT:
![Output](Op12-ds1.png)

## Result
Hence the data was cleaned , outliers were detected and removed.


