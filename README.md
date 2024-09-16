# EXNO2DS
# AIM:
      To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT
```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
df=pd.read_csv("/content/titanic_dataset.csv")
df
```
![image](https://github.com/user-attachments/assets/561973e0-6e95-4300-8b7a-73b37dac957a)
```
df.info()
```
![image](https://github.com/user-attachments/assets/ca928143-a484-4d0d-8c0c-1f351bcc423a)
```
df.shape
```
![image](https://github.com/user-attachments/assets/26941e2d-e495-4ad4-86cd-072d97efbc24)
```
import pandas as pd
df=pd.read_csv("/content/titanic_dataset.csv")
df.set_index("PassengerId",inplace=True)
print(df.set_index)
```
![image](https://github.com/user-attachments/assets/a4335420-5a41-4b38-83e4-42f9cb9c5f35)
```
df.describe()
```
![image](https://github.com/user-attachments/assets/0218413d-5a9b-4539-8976-5f6181498855)
```
df.nunique()
```
![image](https://github.com/user-attachments/assets/700df77a-162f-4749-974c-24c10a087303)
```
df["Survived"].value_counts()
```
![image](https://github.com/user-attachments/assets/c27e00b5-578c-4437-966c-006c033092c1)
```
per=(df["Survived"].value_counts()/df.shape[0]*100).round(2)
per
```
![image](https://github.com/user-attachments/assets/2f2d58b6-4bbc-47fd-a2ab-8096eb2be6c0)
```
sns.countplot(data=df,x="Survived")
```
![image](https://github.com/user-attachments/assets/1f4420f1-f4a0-45ef-aee5-5935d18807e3)
```
df
```
![image](https://github.com/user-attachments/assets/ea4bedc6-4d58-40f2-8954-dc5c208263bc)
```
df.Pclass.unique()
```
![image](https://github.com/user-attachments/assets/9823f924-8e0f-42ce-9193-37d45ebc5b77)
```
df.rename(columns={'sex':'Gender'},inplace=True)
df
```
![image](https://github.com/user-attachments/assets/57f5712e-2b50-4cac-84ed-37874fed4f30)
```
import seaborn as sns
df=pd.read_csv("/content/titanic_dataset.csv")
sns.catplot(x="Sex",col='Survived',kind="count",data=df,height=5, aspect=.7)
```
![image](https://github.com/user-attachments/assets/22458922-7e2f-458a-8cdb-92c9717f27c4)
```
sns.catplot(x='Survived',hue='Sex',data=df,kind='count')
```
![image](https://github.com/user-attachments/assets/7cbf8864-a0ac-41cd-98d7-542b5ce435fb)
```
df.boxplot(column='Age',by="Survived")
```
![image](https://github.com/user-attachments/assets/926b965d-3a6f-446b-b74d-d9aa3ff30ec3)
```
sns.scatterplot(x=df['Age'],y=df["Fare"])
```
![image](https://github.com/user-attachments/assets/e38e33b5-90bf-481d-ba65-80e0f2ffa896)
```
sns.catplot(data=df,col='Survived',x='Sex',hue='Pclass',kind='count')
```

![Screenshot 2024-09-16 133521](https://github.com/user-attachments/assets/f14987b2-30d2-4809-91e9-595a39a6bec3)

```
import seaborn as sns
corr=df.corr()
sns.heatmap(corr,annot=True)
```
![Screenshot 2024-09-16 133655](https://github.com/user-attachments/assets/547e87fa-b791-476f-b09e-bdd31bda31dc)
```
sns.pairplot(df)
```

![Screenshot 2024-09-16 134245](https://github.com/user-attachments/assets/2dfab896-dbff-46ef-a4a5-7c815e8da1de)


# RESULT
      Code are sucessfully executed. 
