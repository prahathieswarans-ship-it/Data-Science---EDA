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

import numpy as np

import pandas as pd

import seaborn as sns


data = pd.read_csv("titanic_dataset.csv")

df = pd.DataFrame(data)

print(df)

<img width="988" height="342" alt="image" src="https://github.com/user-attachments/assets/27a0e809-a887-4109-aa33-448a9026d8b3" />

import pandas as pd 
data  = pd.read_csv("titanic_dataset.csv")
df = pd.DataFrame(data)
df.info()

<img width="289" height="302" alt="image" src="https://github.com/user-attachments/assets/c243c844-b821-4d37-801f-adf899ac5840" />

import pandas as pd 
data  = pd.read_csv("titanic_dataset.csv")
df = pd.DataFrame(data)
df.nunique()

<img width="155" height="213" alt="image" src="https://github.com/user-attachments/assets/e4889c64-9126-4306-97b4-8249384e30b8" />

df["Survived"].value_counts()

<img width="192" height="69" alt="image" src="https://github.com/user-attachments/assets/48c66461-9e37-47f6-bbc2-5c578caac9f9" />

percentage  = ((df["Survived"].value_counts())/(df.shape[0])*100).round(2)
print(percentage)

<img width="547" height="35" alt="image" src="https://github.com/user-attachments/assets/13217f1f-784e-4779-acc8-5841078c4c01" />


percentage  = ((df["Survived"].value_counts())/(df.shape[0])*100).round(2)
print(percentage)


<img width="777" height="532" alt="image" src="https://github.com/user-attachments/assets/379915fc-01af-466a-a080-5adc83a1856f" />


print(df.Pclass.unique())


<img width="71" height="14" alt="image" src="https://github.com/user-attachments/assets/eecb9e16-b355-4fab-bd68-8d2e140b9b19" />


print(df.Pclass.unique())


<img width="979" height="287" alt="image" src="https://github.com/user-attachments/assets/d0f4fc4e-68ee-4854-b8af-2223c67738c3" />


sns.catplot(data=df,x="Gender",col="Survived",kind="count",height=5,aspect=.7)

<img width="1019" height="705" alt="image" src="https://github.com/user-attachments/assets/43a87275-f248-4818-b371-c1bb87f81f82" />


sns.catplot(data=df,hue="Gender",kind="count",x="Survived")

<img width="838" height="705" alt="image" src="https://github.com/user-attachments/assets/41c01f24-7423-42b9-89d0-2a2633022987" />


df.boxplot(column="Age",by="Survived")

<img width="759" height="566" alt="image" src="https://github.com/user-attachments/assets/1d8220df-2d00-44ef-ac0b-6f8d939265a5" />


sns.scatterplot(data=df,x=df["Age"],y=df["Fare"])

<img width="777" height="532" alt="image" src="https://github.com/user-attachments/assets/fbf66e30-b7f8-4294-99fc-87857e01adc7" />

sns.catplot(data=df,col="Survived",x="Gender",hue="Pclass",kind="count")

<img width="1516" height="705" alt="image" src="https://github.com/user-attachments/assets/d60e92a2-0e44-4866-8e7b-4ffbba013752" />




sns.pairplot(df)
<img width="2478" height="2478" alt="image" src="https://github.com/user-attachments/assets/9253911f-ef2f-4fdd-9c80-2cb00f29b434" />

# RESULT
        <<INCLUDE YOUR RESULT HERE>>
