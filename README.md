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

# Import libraries and load the dataset
```
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
```
<img width="1244" height="221" alt="image" src="https://github.com/user-attachments/assets/beadc352-ab03-4857-a040-aa8b1847df94" />

# Line Plot
```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
<img width="702" height="545" alt="image" src="https://github.com/user-attachments/assets/1245d097-4824-4b65-8c4f-4de5ad830d98" />

# Multi-Line Plot
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
<img width="708" height="543" alt="image" src="https://github.com/user-attachments/assets/1e010ff0-d9c3-44ec-a96e-ff8497ebaefb" />

# Bar Plot
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
<img width="887" height="570" alt="image" src="https://github.com/user-attachments/assets/a2effa9e-3497-4dec-a5bd-5dabaf106bc1" />

# Scatter Plot
```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
<img width="736" height="553" alt="image" src="https://github.com/user-attachments/assets/54cc3b92-21e3-4d28-b42d-6987e64f0f6a" />

# Bubble Plot
```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
<img width="785" height="560" alt="image" src="https://github.com/user-attachments/assets/b02d627c-aa1b-45af-847e-19ccfd482ba1" />

# Histogram
```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
<img width="776" height="547" alt="image" src="https://github.com/user-attachments/assets/bc303983-ce85-4aa6-9c8b-bf7506bbd4a2" />

# Box Plot
```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
<img width="751" height="556" alt="image" src="https://github.com/user-attachments/assets/db182e92-3c86-4b6c-9abe-f596e2005bff" />

# Violin Plot
```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
<img width="748" height="559" alt="image" src="https://github.com/user-attachments/assets/c76f7c63-fb71-4615-86b8-f5aeaf5dac59" />

# Density Plot
```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```

<img width="764" height="563" alt="image" src="https://github.com/user-attachments/assets/e52b394d-0ed9-42a4-b9b3-c35576eae5ff" />

# Heatmap
```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
<img width="798" height="635" alt="image" src="https://github.com/user-attachments/assets/7e3bc95d-e22f-4dcd-a930-0bebdf5af41e" />


# Result:
Hence, data visualization using seaborn python library for the given dataset is successfully implemented. 

In this experiment, data visualization was performed using the Seaborn Python library on the Titanic dataset. Various types of plots were created to understand data patterns, relationships, and distributions. The visualizations included:

Line Plot and Multi-Line Plot: To show trends and comparisons across multiple data series.

Bar Plot: To compare the average fare across different embarkation points.

Scatter Plot & Bubble Plot: To visualize relationships between age and fare, with bubble size representing passenger class.

Histogram: To display the distribution of passenger classes with survival status.

Box Plot and Violin Plot: To compare the spread and distribution of fare and age across classes.

Density Plot: To visualize the age distribution smoothly.

Heatmap: To show correlations among numeric variables in the dataset.



