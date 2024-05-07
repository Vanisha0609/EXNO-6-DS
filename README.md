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
df=pd.read_csv("/content/titanic_dataset.csv")
df.head()
import seaborn as sns
import matplotlib.pyplot as plt
```
![image](https://github.com/Vanisha0609/EXNO-6-DS/assets/119104009/fb980e39-a84b-45f2-8454-b1915be0e2f7)

1.LINE PLOT
```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
``
![image](https://github.com/Vanisha0609/EXNO-6-DS/assets/119104009/a0159049-c043-4fb3-862f-a226d395be3d)

2.MULTI-LINE PLOT
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
<img src="https://github.com/Vanisha0609/EXNO-6-DS/assets/119104009/8b2cc673-95e9-4717-a1c1-04a28ff70d59" width="500" height="350">

TO VISUALIZE REALTIONSHIPS

1.BAR CHART
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
<img src="https://github.com/Vanisha0609/EXNO-6-DS/assets/119104009/423e14cc-4636-4760-9979-544f4bcc490d" width="500" height="360">

2.SCATTER PLOT
```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
<img src="https://github.com/Vanisha0609/EXNO-6-DS/assets/119104009/3a892da3-1b6e-4db6-bf1a-b972a4eed19a" width="500" height="360">

3.BUBBLE CHART
```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
<img src="https://github.com/Vanisha0609/EXNO-6-DS/assets/119104009/39e134aa-86b3-428d-b3b5-8e4b7afa4e0d" width="500" height="350">

TO CAPTURE DISTRIBUTIONS
1.HISTOGRAM

```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
![image](https://github.com/Vanisha0609/EXNO-6-DS/assets/119104009/621e24c3-49db-4932-9692-61fc84cad923)

2.BOX PLOT
```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
<img src="https://github.com/Vanisha0609/EXNO-6-DS/assets/119104009/4e8d405b-4359-418a-adeb-04a4f88599a5" width="500" height="350">

3.VIOLIN PLOT
```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
<img src="https://github.com/Vanisha0609/EXNO-6-DS/assets/119104009/7dbbb8fd-f5cb-423b-859a-06749058a611" width="450" height="350">

4.DENSITY PLOT
```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
<img src="https://github.com/Vanisha0609/EXNO-6-DS/assets/119104009/c367935d-7db9-40ef-8814-2c999ac5be02" width="500" height="380">

5.HEAT MAP
```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
<img src="https://github.com/Vanisha0609/EXNO-6-DS/assets/119104009/a1b3738a-972e-4419-8a58-dcd5ae88d59a" width="400" height="400">



# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
