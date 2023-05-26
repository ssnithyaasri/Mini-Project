# Mini-Project
# DATA ANALYSIS

# AIM:

To Perform Data Analysis on the given dataset and save the data to a file.

# Explanation

Data analytics is important because it helps businesses optimize their performance.Implementing it into the business model means companies can help reduce costs by identifying more efficient ways of  doing business and by storing large amounts of data

# ALGORITHM

# STEP 1
Read the given Data

# STEP 2
Clean the Data Set using Data Cleaning Process

# STEP 3
Apply Feature generation and selection techniques to all the features of the data set

# STEP 4
Apply data visualization techniques to identify the patterns of the data.

# CODE:

```

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
df=pd.read_csv("/content/ds_salaries.csv",encoding="ISO-8859-1")
dfdf.isnull()
df.info()
df.describe()
sns.lineplot(x="work_year",y="salary",data=df,marker='o')
plt.title("work_year vs salary")
plt.xticks(rotation = 90)
plt.show()

sns.barplot(x="work_year",y="salary",data=df)
plt.xticks(rotation = 90)
plt.show()
df.shape
df1 = df[(df.salary>= 60)]
df1.shape

plt.figure(figsize=(30,8))
states=df1.loc[:,["job_title","salary"]]
states=states.groupby(by=["job_title"]).sum().sort_values(by="salary")
sns.barplot(x=states.index,y="salary",data=states)
plt.xticks(rotation = 90)
plt.xlabel=("job_title")
plt.ylabel=("salary")
plt.show()
plt.figure(figsize=(30,8))
states=df1.loc[:,["job_title","salary"]]
states=states.groupby(by=["job_title"]).sum().sort_values(by="salary")
sns.barplot(x=states.index,y="salary",data=states)
plt.xticks(rotation = 90)
plt.xlabel=("job_title")
plt.ylabel=("salary")
plt.show()
sns.lineplot(x="company_size",y="salary",data=df)
plt.show()
states=df.loc[:,["work_year","salary"]]
states=states.groupby(by=["work_year"]).sum().sort_values(by="salary")
sns.barplot(x=states.index,y="salary",data=states)
plt.xticks(rotation = 90)
plt.xlabel=("work_year")
plt.ylabel=("salary")
plt.show()
df.groupby(['work_year']).sum().plot(kind='pie', y='salary',figsize=(6,9),pctdistance=1.7,labeldistance=1.2)
df["work_year"].corr(df["salary"])
df_corr = df.copy()
df_corr = df_corr[["work_year","salary"]]
df_corr.corr()
sns.pairplot(df_corr, kind="scatter")
plt.show()
grouped_data = df.groupby('employment_type')[['work_year', 'salary']].mean()
# Create a bar chart of the grouped data
fig, ax = plt.subplots()
ax.bar(grouped_data.index, grouped_data['work_year'], label='work_year')
ax.bar(grouped_data.index, grouped_data['salary'], bottom=grouped_data['work_year'], label='salary')
ax.set_xlabel('employment_title')
ax.set_ylabel('Value')
ax.legend()
plt.show()
grouped_data = df.groupby(['job_title', 'company_size'])[['work_year', 'salary']].mean()
pivot_data = grouped_data.reset_index().pivot(index='job_title', columns='company_size', values=['work_year', 'salary'])
# Create a bar chart of the grouped data
fig, ax = plt.subplots()
pivot_data.plot(kind='bar', ax=ax)
ax.set_xlabel('job_title')
ax.set_ylabel('Value')
plt.legend(title='company_size')
plt.show()

```

# OUTPUT:

![image](https://github.com/Hemasonica774/Data-science.mini.project/assets/118361409/bc5555ed-ecad-4297-89c3-d47ce84ddb33)

![image](https://github.com/Hemasonica774/Data-science.mini.project/assets/118361409/a06f913d-4123-4a04-9a91-68d387856c58)

![image](https://github.com/Hemasonica774/Data-science.mini.project/assets/118361409/1db60ab1-ebe7-4f3a-8f88-5d954378a6ed)

![image](https://github.com/Hemasonica774/Data-science.mini.project/assets/118361409/0883b19c-7dc5-43a9-83ff-572892e30fad)

![image](https://github.com/Hemasonica774/Data-science.mini.project/assets/118361409/c395f591-6671-45ae-8803-4b4dc2e8a012)

![image](https://github.com/Hemasonica774/Data-science.mini.project/assets/118361409/f0ee262b-fb1a-4725-baeb-806fa87796f8)

![image](https://github.com/Hemasonica774/Data-science.mini.project/assets/118361409/fa2c535e-6862-423a-b697-f0fe66100680)

![image](https://github.com/Hemasonica774/Data-science.mini.project/assets/118361409/dd751bc0-9f5e-46ec-b9ea-64e329d1bd56)

![image](https://github.com/Hemasonica774/Data-science.mini.project/assets/118361409/06499592-b2ac-4583-b239-35e83329872c)

![image](https://github.com/Hemasonica774/Data-science.mini.project/assets/118361409/67528661-a204-492e-aa6a-10700c3bc3f6)

![image](https://github.com/Hemasonica774/Data-science.mini.project/assets/118361409/bbb4173f-2f2e-48f2-9fa2-495dc596fdfd)

![image](https://github.com/Hemasonica774/Data-science.mini.project/assets/118361409/a07c8aa4-1e9f-4033-b270-2db93e3239e0)

![image](https://github.com/Hemasonica774/Data-science.mini.project/assets/118361409/22d575ae-35fb-49ee-92fb-1e4768670803)

![image](https://github.com/Hemasonica774/Data-science.mini.project/assets/118361409/e7a357f7-f633-415a-b0f8-3f12ff2556e6)

![Screenshot 2023-05-21 185613](https://github.com/Hemasonica774/Data-science.mini.project/assets/118361409/87c9f635-6663-4e72-b50d-e74b8de59cff)


![image](https://github.com/Hemasonica774/Data-science.mini.project/assets/118361409/21db9512-0a49-4393-b795-45767fa2f62b)


# Result:

Thus, Data analysis is performed on the given dataset and save the data to a file
