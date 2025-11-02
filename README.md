# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:

```
 import pandas as pd
 import seaborn as sns
 import matplotlib.pyplot as plt
 df=pd.read_csv("titanic_dataset.csv")
 df.head()
```
<img width="1302" height="262" alt="image" src="https://github.com/user-attachments/assets/71bfa5e8-a986-4c90-835a-a4b1732a8f89" />


```
 x=[1,2,3,4,5]
 y=[3,6,2,7,1]
 sns.lineplot(x=x,y=y)
 plt.title('Line Plot')
```
<img width="691" height="585" alt="image" src="https://github.com/user-attachments/assets/f5e1849e-7e1d-4030-aa2c-7b868202541f" />

```
 x=[1,2,3,4,5]
 y1=[3,5,2,6,1]
 y2=[1,6,4,3,8]
 y3=[5,2,7,1,4]
 sns.lineplot(x=x,y=y1)
 sns.lineplot(x=x,y=y2)
 sns.lineplot(x=x,y=y3)
 plt.title('Multi Line Plot')
```
<img width="672" height="583" alt="image" src="https://github.com/user-attachments/assets/ba87c3f2-2c28-49bb-8114-f108d877d27b" />


```
 plt.figure(figsize=(8,5))
 sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
 plt.title("Fare Of Passenger By Embarked Town")
```
<img width="899" height="625" alt="image" src="https://github.com/user-attachments/assets/49430cc9-99c8-482d-85e9-9aa18633f915" />

```
 sns.scatterplot(x="Age", y="Fare", data=df)
 plt.title('Scatterplot of Age vs Fare')
 plt.show()
```
<img width="760" height="573" alt="image" src="https://github.com/user-attachments/assets/b6e5f655-130e-4483-884e-95ab6456c6c4" />

```
 sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
 plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
 plt.show()
```
<img width="755" height="567" alt="image" src="https://github.com/user-attachments/assets/81ff3c6e-1f37-48e2-8f48-c3aa555cec18" />

```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
<img width="727" height="572" alt="image" src="https://github.com/user-attachments/assets/57fff241-085b-448b-b8a7-b1173e8f6227" />

```
 sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
 plt.title("Age By Passenger Class")
```
<img width="738" height="597" alt="image" src="https://github.com/user-attachments/assets/89025a4b-b27a-499a-b396-4f7de6133b95" />

```
 sns.violinplot(x="Pclass", y="Fare", data=df)
 plt.title('Violin Plot of Fare by Passenger Class')
 plt.show()
```
<img width="741" height="555" alt="image" src="https://github.com/user-attachments/assets/b15acddb-26f9-4af2-bf91-1a8e931182b7" />

```
 sns.kdeplot(data=df['Age'], shade=True)
 plt.title('Density Plot of Passenger Ages')
 plt.show()
```
<img width="763" height="552" alt="image" src="https://github.com/user-attachments/assets/0956c39a-5c8e-4748-ae38-f9cc1f7a30f1" />

```
 numeric_df = df.select_dtypes(include=['float64', 'int64'])
 corr_matrix = numeric_df.corr()
 sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
 plt.title('Heatmap of Titanic Dataset')
 plt.show()
```
<img width="805" height="631" alt="image" src="https://github.com/user-attachments/assets/942a00b1-37a3-405c-b98b-fe70083aa569" />




# Result:
 Thus, the Data Visualization using seaborn python library for the given data is implemented successfully.
