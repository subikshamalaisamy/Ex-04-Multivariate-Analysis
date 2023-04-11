# Ex-04-Multivariate-Analysis

# AIM:
   To read the given data and perform multivariate analysis.
# Algorithm:

# Step 1:
Read the given Data

# Step 2:
Get the information about the data

# Step 3:
Get the data types of the each column

# Step 4:
Group the data according to the categories

# Step 5:
Get the description of the data

# Step 6:
Perform graphical analysis and print the distribution of quantitative data using barplot.

#Step 7:
Find the correlation value and perform heatmap for the given dataset.

# CODE
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv('/content/SuperStore (1).csv')
df.head()

df.info()

df.dtypes

# Barplot
states=df.loc[:,["State","Sales"]]
states=states.groupby(by=["State"]).sum().sort_values(by="Sales")
plt.figure(figsize=(17,7))
sns.barplot(x=states.index,y="Sales",data=states)
plt.xticks(rotation = 90)
plt.xlabel=("STATES")
plt.ylabel=("Sales")
plt.show()

# Heatmap
df.corr()

sns.heatmap(df.corr(),annot=True)

# OUTPUT:
<img width="722" alt="image" src="https://user-images.githubusercontent.com/87276633/231127296-043df558-847a-4e9b-99c2-3324cfe21da6.png">
<img width="220" alt="image" src="https://user-images.githubusercontent.com/87276633/231127425-724c4d10-87a8-404c-ae8f-1d79e78c9e2b.png">
<img width="145" alt="image" src="https://user-images.githubusercontent.com/87276633/231127513-4aeefd04-2cba-4a1d-91f3-804ca11ba6d5.png">
<img width="779" alt="image" src="https://user-images.githubusercontent.com/87276633/231128422-1bf4646a-ea61-4f0a-8690-1da391a899a7.png">
<img width="302" alt="image" src="https://user-images.githubusercontent.com/87276633/231128542-eda2d000-b473-4d0b-9852-3d5e5b018eb4.png">
<img width="400" alt="image" src="https://user-images.githubusercontent.com/87276633/231128769-865237d1-f6d2-4d61-9fbe-19ad4923c20e.png">

# RESULT:
Thus the multivariate analysis for the given data is performed successfully.
