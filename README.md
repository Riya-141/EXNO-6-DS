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
import seaborn as sns
import matplotlib.pyplot as plt

df=sns.load_dataset("tips")
df
```
<img width="1263" height="523" alt="image" src="https://github.com/user-attachments/assets/ae274231-1653-47f2-a16e-b6ea0bf88202" />

```
sns.lineplot(x="total_bill", y="tip", data=df, hue="sex", linestyle="solid", legend="auto", palette="Set1")
```
<img width="1265" height="587" alt="image" src="https://github.com/user-attachments/assets/70c1aae8-2d50-48e5-aff8-4702ad1d81e7" />

```
x=[1, 2, 3, 4, 5]
y1=[3, 5, 2, 6, 1]
y2=[1, 6, 4, 3, 8]
y3=[5, 2, 7, 1, 4]
sns.lineplot(x=x, y=y1)
sns.lineplot(x=x, y=y2)
sns.lineplot(x=x, y=y3)
plt.title("Multi-Line Plot")
plt.xlabel('X Label')
plt.ylabel("Y Label")
```
<img width="1275" height="773" alt="image" src="https://github.com/user-attachments/assets/2a915ab2-9f89-4210-8569-7ccd03decb5e" />

```
tips = sns.load_dataset("tips")
avg_total_bill = tips.groupby("day")["total_bill"].mean()
avg_tip = tips.groupby("day")["tip"].mean()

plt.figure(figsize=(8,6))

p1 = plt.bar(avg_total_bill.index, avg_total_bill, label="Total Bill")
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label="Tip")

plt.xlabel("Day of the week")
plt.ylabel("Amount")
plt.title("Average Total Bill and Tip by Day")
plt.legend()
plt.show()
```
<img width="1060" height="780" alt="image" src="https://github.com/user-attachments/assets/969190dd-83fe-48ca-a602-282d88627412" />

```
avg_total_bill=tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time')['tip'].mean()

p1=plt.bar(avg_total_bill.index,avg_total_bill,label="Total Bill",width=0.4)
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label="Tip",width=0.4)

plt.xlabel("Time of the day")
plt.ylabel("Amount")
plt.title("Average Total Bill and Tip by Time of the Day")
plt.legend()
```
<img width="1272" height="792" alt="image" src="https://github.com/user-attachments/assets/10645cce-5098-4f9a-9c50-83737be0eccd" />

```
import seaborn as sns
df=sns.load_dataset("tips")
sns.barplot(x="day",y="total_bill",hue="sex",data=df,palette='Set3')
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Total Bill by Day and Gender")
```
<img width="1270" height="715" alt="image" src="https://github.com/user-attachments/assets/141e47cf-c991-4d50-9692-760d435d7299" />

```
import seaborn as sns
df=sns.load_dataset("tips")
sns.scatterplot(x="total_bill",y="tip",hue="sex",data=df,palette="Set1")
plt.xlabel("Totsl Bill")
plt.ylabel("Tip")
plt.title("Scatter Plot of Total Bill vs Tip Amount")
```
<img width="1265" height="708" alt="image" src="https://github.com/user-attachments/assets/7482ecb1-70c0-4a59-96be-d34631b5ec02" />

```
sns.histplot(data=df,x="total_bill",hue="smoker",kde=True,palette="Set1")
plt.xlabel("Total Bill")
plt.ylabel("Frequency")
plt.title("Distribution of Total Bill by Gender")
```
<img width="1265" height="673" alt="image" src="https://github.com/user-attachments/assets/951a6d0a-eebe-4e56-94e7-7e4f041e34e4" />

```
import seaborn as sns
import pandas as pd
df=sns.load_dataset('tips')
sns.boxplot(x='day',y='total_bill',hue='sex',data=df,palette='Set2')
```
<img width="1269" height="646" alt="image" src="https://github.com/user-attachments/assets/50a2c920-cec9-4e33-ad76-6739ddad8f16" />

```
sns.boxplot(x="day",y="total_bill",hue="smoker",data=df,linewidth=2,width=0.6,fliersize=7,flierprops={"marker":"o","markerfacecolor":"grey"},boxprops={"facecolor":"red","edgecolor":"black"},whiskerprops={"color":"darkblue","linestyle":"--","linewidth":"-","linewidth":2},palette="Set1")
```
<img width="1273" height="612" alt="image" src="https://github.com/user-attachments/assets/ec1b66af-5c76-464a-83ac-39baac1a7767" />

```
sns.violinplot(x="day",y="total_bill",hue="smoker",data=tips,linewidth=2,width=0.6,palette="Set1",inner="quartile")
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
<img width="1268" height="674" alt="image" src="https://github.com/user-attachments/assets/fb6907ec-9c16-448b-8298-cfc8856f534e" />

```
import seaborn as sns
sns.set(style="whitegrid")
tip = sns.load_dataset("tips")
sns.violinplot(x="day", y="tip", data=tip, palette="Set2")
```
<img width="1268" height="654" alt="image" src="https://github.com/user-attachments/assets/b0735891-0f47-45e1-bcc4-027de57b0fe5" />

```
import seaborn as sns
sns.set(style="whitegrid")
tip = sns.load_dataset("tips")
sns.violinplot(x=tip["total_bill"],palette="Set1")
```
<img width="1278" height="648" alt="Screenshot 2025-10-17 101418" src="https://github.com/user-attachments/assets/8fba7531-9ac5-4b96-935f-cb8e7a055b13" />

```
import seaborn as sns
sns.set(style="whitegrid")
tip = sns.load_dataset("tips")
sns.violinplot(x="tip",y="day",data=tip,palette="rainbow")
```
<img width="1266" height="653" alt="image" src="https://github.com/user-attachments/assets/d76549c6-9ae7-48ff-9d35-2a7612e8b31e" />

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple="layer",linewidth=3,palette="Set2",alpha=0.8)
```
<img width="1276" height="595" alt="image" src="https://github.com/user-attachments/assets/ae4f0e18-ab47-49a9-bfaf-24fbd0d37a99" />

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple="stack",linewidth=3,palette="Set3",alpha=0.8)
```
<img width="1272" height="589" alt="image" src="https://github.com/user-attachments/assets/0cee64e1-5f82-434b-8ba8-3cdaa7a0a0c2" />

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple="fill",linewidth=3,palette="Set1",alpha=0.8)
```
<img width="1271" height="605" alt="image" src="https://github.com/user-attachments/assets/9f642476-3311-4937-ab65-0e5812c29868" />

```
import seaborn as sns
tip = sns.load_dataset("tips")
num = tips.select_dtypes(include=['float64','int64']).columns
corr = tips[num].corr()
sns.heatmap(corr,annot=True,cmap='YlGnBu')
```
<img width="1272" height="658" alt="image" src="https://github.com/user-attachments/assets/07e06b00-2a75-47c5-81db-5f5e33851bd2" />

```
sns.heatmap(corr,cmap='YlGnBu')
```
<img width="1268" height="583" alt="image" src="https://github.com/user-attachments/assets/972598f2-6527-44d4-b3b5-288310809455" />

# Result:

Thus, all the data visualization technique of seaborn has been implemented.

