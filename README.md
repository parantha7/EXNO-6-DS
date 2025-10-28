# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

## NAME   : PARANTHAMAN S
## REG.NO : 212224040232

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
df=pd.read_csv("titanic_dataset(1).csv")
df.head()
```
<img width="1498" height="369" alt="image" src="https://github.com/user-attachments/assets/b773e31e-fe0f-4430-ab74-015d80bee295" />

## Line Plot:

```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
<img width="948" height="696" alt="image" src="https://github.com/user-attachments/assets/16bc564e-49a8-45b1-8cfc-4c911259edfb" />

## Multi Line Plot:

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
<img width="996" height="792" alt="image" src="https://github.com/user-attachments/assets/c9e4bcc5-570e-44ba-90a9-9e7dd083cf39" />

## TO VISUALIZE RELATIONSHIPS
## 1.Bar Chart:
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
<img width="1533" height="874" alt="image" src="https://github.com/user-attachments/assets/cbc75f38-6696-4c24-af2d-925d0cd74409" />

## 2.Scatter Plot:
```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
<img width="831" height="679" alt="image" src="https://github.com/user-attachments/assets/acbdea49-7c07-4a52-b1b0-dd1e7be81309" />

## 3.Bubble Chart:
```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
<img width="916" height="691" alt="image" src="https://github.com/user-attachments/assets/a1e001ee-6989-42c3-9772-06b73b7ae195" />

## TO CAPTURE DISTRIBUTIONS
## 1.Histogram:
```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
<img width="876" height="683" alt="image" src="https://github.com/user-attachments/assets/0179debf-a769-426a-97c2-8e65ac036c01" />

## 2.Box Plot:
```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
<img width="1552" height="763" alt="image" src="https://github.com/user-attachments/assets/14bc6274-f82f-4507-9f08-43935dd142e7" />

## 3.Violin Plot:
```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
<img width="961" height="659" alt="image" src="https://github.com/user-attachments/assets/068f3a10-ff62-48f3-a522-70250830623c" />

## 4.Density Plot:
```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
<img width="868" height="789" alt="image" src="https://github.com/user-attachments/assets/661857cc-0ca0-451f-945c-77aef0774996" />

## 5.Heatmap:
```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
<img width="971" height="768" alt="image" src="https://github.com/user-attachments/assets/8176e54b-e338-4d06-a6df-bd3f8975410d" />


# Result:

```
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully.
```

