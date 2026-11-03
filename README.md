# Exno: 1 - Data Cleaning Process

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

# Coding and Output
```
import pandas as pd
a=pd.read_csv("/content/SAMPLEIDS.csv")
print(a)
```
<img width="1342" height="795" alt="image" src="https://github.com/user-attachments/assets/867fb08e-1de9-43ae-ad85-183bcd18f350" />

```
a.shape
```
<img width="1247" height="77" alt="image" src="https://github.com/user-attachments/assets/3ee72b87-9ec2-4d3e-90d3-5ecae050c559" />

```
a.head()
```

<img width="812" height="225" alt="image" src="https://github.com/user-attachments/assets/adcde978-4eef-4ec2-b877-cc56cda9119d" />

```
a.head(7)
```

<img width="867" height="292" alt="image" src="https://github.com/user-attachments/assets/5c5e2dbd-4831-4e1b-b026-62532ac29cba" />

```
a.tail()
```

<img width="955" height="255" alt="image" src="https://github.com/user-attachments/assets/976438a5-d6da-4914-9cf4-bbb47a46ba82" />

```
a.tail(3)
```

<img width="863" height="172" alt="image" src="https://github.com/user-attachments/assets/bc524ff0-c932-49c6-ba4d-bd772b560a9b" />

```
a.info()
```

<img width="950" height="377" alt="image" src="https://github.com/user-attachments/assets/6904b941-8076-45ba-b434-fa80c941a192" />

```
a.describe()
```

<img width="817" height="335" alt="image" src="https://github.com/user-attachments/assets/33e7ac8a-610a-4ff4-88bd-07e08acf15a4" />

```
a.isnull()
```

<img width="1041" height="717" alt="image" src="https://github.com/user-attachments/assets/ea6a7c2e-39a2-43d9-87bf-eb46906005d9" />

```
a.notnull()
```

<img width="802" height="701" alt="image" src="https://github.com/user-attachments/assets/08be4399-98f3-4927-9ee5-f5877656dc1c" />

```
a.isnull().sum()
```

<img width="450" height="462" alt="image" src="https://github.com/user-attachments/assets/71bc3184-0615-49d2-95b3-05e3bfc2857b" />

```
a.isnull().any()
```

<img width="497" height="471" alt="image" src="https://github.com/user-attachments/assets/a48ece0b-2381-4eee-b9cb-92143a147d65" />

```
a.dropna()
```

<img width="928" height="463" alt="image" src="https://github.com/user-attachments/assets/03dbd380-a5dc-43e8-b87b-c86adcf22e51" />

```
a.dropna(axis = 1)
```

<img width="462" height="685" alt="image" src="https://github.com/user-attachments/assets/2f547047-20c5-4692-a02f-3f779af53fe4" />

```
a.fillna(1)
```

<img width="1012" height="693" alt="image" src="https://github.com/user-attachments/assets/b8827d58-9444-4c3f-a5ee-dd8de1f1fed5" />

```
a.fillna(method = 'ffill')
```

<img width="1285" height="727" alt="image" src="https://github.com/user-attachments/assets/e28ffa44-dcf9-46bf-b75d-8568b7bed8cf" />

```
a.fillna({'GENDER':'MALE','NAME':'SRI','M4':'10'})
```

<img width="946" height="697" alt="image" src="https://github.com/user-attachments/assets/c38549dd-8c91-4604-96a0-89f2704a6cf4" />

```
ir=pd.read_csv("/content/iris.csv")
ir
```

<img width="763" height="445" alt="image" src="https://github.com/user-attachments/assets/acdf2ee2-73dc-435e-9d1e-0bf4e3977348" />

```
ir.head()
```

<img width="652" height="235" alt="image" src="https://github.com/user-attachments/assets/16ff73e5-7fe4-45dd-84e4-005854c96ac8" />

```
ir.tail()
```

<img width="613" height="241" alt="image" src="https://github.com/user-attachments/assets/ba846c80-6fc9-4c39-8221-c1a90afac057" />

```
ir.isnull()
```

<img width="762" height="432" alt="image" src="https://github.com/user-attachments/assets/b3468b64-9199-4447-bd64-ca142aa9cdb3" />

```
ir.isnull().sum()
```

<img width="445" height="262" alt="image" src="https://github.com/user-attachments/assets/247543d8-0331-45ec-bd9f-61fd8b1c514d" />

```
ir.notnull()
```

<img width="632" height="432" alt="image" src="https://github.com/user-attachments/assets/1f784c6b-13e2-4d93-9fd7-b5fc6fb9747a" />

```
import seaborn as sns
sns.boxplot(x='sepal_width',data=ir)
```

<img width="598" height="482" alt="image" src="https://github.com/user-attachments/assets/caf18bc7-2035-4289-9c22-b9c06fdaf2d3" />

```
sns.boxplot(x='sepal_length',data=ir)
```

<img width="748" height="476" alt="image" src="https://github.com/user-attachments/assets/8ee8e434-9d90-459c-811d-b8fc6fa4ca54" />

```
sns.boxplot(x='petal_width',data=ir)
```

<img width="681" height="468" alt="image" src="https://github.com/user-attachments/assets/8775b197-73ed-4a0a-9e59-80be4aab72c1" />

```
sns.boxplot(x='petal_length',data=ir)
```

<img width="641" height="475" alt="image" src="https://github.com/user-attachments/assets/3f043168-d02c-4fc4-9732-1aa3b682fcf7" />

```
sns.boxplot(x='species',data=ir)
```

<img width="741" height="472" alt="image" src="https://github.com/user-attachments/assets/5d36e63b-54f9-4442-b2f8-965e210045f3" />

```
Q1=ir.sepal_width.quantile(0.25)
Q3=ir.sepal_width.quantile(0.75)
(IQR)=Q3-Q1
print(IQR)
```

<img width="482" height="127" alt="image" src="https://github.com/user-attachments/assets/c8fb97da-0a02-4e24-a226-b4a2a8b6f932" />

```
ran=ir[((ir.sepal_width<(Q1-1.5*IQR))|(ir.sepal_width>(Q3+1.5*IQR)))]
ran['sepal_width']
```

<img width="667" height="257" alt="image" src="https://github.com/user-attachments/assets/d48313c1-fd15-4984-96e8-d8787923bdc9" />

```
ran=ir[~((ir.sepal_width<(Q1-1.5*IQR))|(ir.sepal_width>(Q3+1.5*IQR)))]
ran['sepal_width']
```

<img width="660" height="493" alt="image" src="https://github.com/user-attachments/assets/30108d6a-8380-4508-8bff-95a7eec07171" />

```
sns.boxplot(x='sepal_width',data=ran)
```

<img width="603" height="477" alt="image" src="https://github.com/user-attachments/assets/dced024c-2a53-4606-90f9-e95a4c46df43" />

```
import numpy as np
import scipy.stats as stats
z=np.abs(stats.zscore(ir['petal_length'])) 
z
```

<img width="966" height="592" alt="image" src="https://github.com/user-attachments/assets/a789ae7c-c226-4377-bab2-a43cacd33a48" />

```
ir1=ir[z<3] 
ir1
```

<img width="638" height="435" alt="image" src="https://github.com/user-attachments/assets/fb5b1dd3-420b-456d-b10a-6881a1f3b740" />


# Result

Thus the given data successfully performed data cleaning and saved the cleaned data to a file
