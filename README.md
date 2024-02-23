# Exno:1
Data Cleaning Process

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

```py
# Developed By: Sanjay Ragavendar M K
# Register Number: 212222100045
```
<table>
  <tr>
    <td width=50%>


### 1) Read and display DataFrame
```Python
import pandas as pd
df=pd.read_csv('/content/SAMPLEDS.csv')
df
```
  </td>
  <td>
              
#### OUTPUT:
![image](https://github.com/SanjayRagavendar/Data-Cleaning-DataScience/assets/91368803/84fd997a-508e-4ad0-9364-a5a340049de2)
</td>
</tr>
<tr>
  <td width=50%>
              
### 2) Display head
```Python
df.head()
```
  </td>
  <td>
              
#### OUTPUT:

![image](https://github.com/SanjayRagavendar/Data-Cleaning-DataScience/assets/91368803/f8d966b2-943e-4438-ba6d-237c83ecab2b)
</td>
</tr>
<tr>
  <td width=50%>

### 3) Display tail
```Python
df.tail()
```
  </td>
  <td>
              
#### OUTPUT:

![image](https://github.com/SanjayRagavendar/Data-Cleaning-DataScience/assets/91368803/9ad3c798-1e37-41a6-8854-2bca1d8bbce4)
</td>
</tr>
<tr>
  <td width=50%>

### 4) Info about dataframe
```Python
df.info()
```
  </td>
  <td>
              
#### OUTPUT:

![image](https://github.com/SanjayRagavendar/Data-Cleaning-DataScience/assets/91368803/71c0f834-5412-4683-9470-621927f9c8e6)
</td>
</tr>
<tr>
  <td width=50%>

### 5) Description about the dataframe
```Python
df.describe()
```
  </td>
  <td>
              
#### OUTPUT:

![image](https://github.com/SanjayRagavendar/Data-Cleaning-DataScience/assets/91368803/dafd1fe1-c67c-4d41-a676-901ea7969a16)
</td>
</tr>
<tr>
  <td width=50%>

### 6) Shape of the dataframe
```Python
df.shape
```
  </td>
  <td>
              
#### OUTPUT:

![image](https://github.com/SanjayRagavendar/Data-Cleaning-DataScience/assets/91368803/de7ce1fa-865b-401f-88fa-0fd43b37d999)
</td>
</tr>
<tr>
  <td width=50%>

### 7) Checking tha NUll values
```Python
df.isnull().sum()
```
  </td>
  <td>
              
#### OUTPUT:

![image](https://github.com/SanjayRagavendar/Data-Cleaning-DataScience/assets/91368803/d60e8fd8-4ba3-400a-83b3-d7fdeea0e724)
</td>
</tr>
<tr>
  <td width=50%>

### 8) Drop the Null values
```Python
x=df.dropna(how='any')
x
```
  </td>
  <td>
              
#### OUTPUT:

![image](https://github.com/SanjayRagavendar/Data-Cleaning-DataScience/assets/91368803/1c0aa411-13a1-493b-95e7-647585a6ac46)
</td>
</tr>
<tr>
  <td width=50%>

### 9) Drop the Null values in Total
```Python
tot=df.dropna(subset=['TOTAL'],how='any')
tot
```
  </td>
  <td>
              
#### OUTPUT:

![image](https://github.com/SanjayRagavendar/Data-Cleaning-DataScience/assets/91368803/910f1b9e-4d09-4456-bc1f-6f5b19c2dc2e)
</td>
</tr>
<tr>
  <td width=50%>

### 10) Fill the Null values
```Python
df.fillna(0)
```
  </td>
  <td>
              
#### OUTPUT:

![image](https://github.com/SanjayRagavendar/Data-Cleaning-DataScience/assets/91368803/25d4d7fb-da49-4a2c-9a34-0021044c7978)
</td>
</tr>
<tr>
  <td width=50%>

### 11) Finding the mean value
```Python
mn=df.TOTAL.mean()
mn
```
  </td>
  <td>
              
#### OUTPUT:

![image](https://github.com/SanjayRagavendar/Data-Cleaning-DataScience/assets/91368803/64878c1f-5842-45e2-9097-2418147f748d)

</td>
</tr>
<tr>
  <td width=50%>

### 12) Fill Null value with Mean value
```Python
df.TOTAL.fillna(mn,inplace=True)
```
  </td>
  <td>
              
#### OUTPUT:

df
</td>
</tr>
<tr>
  <td width=50%>

### 13) Final output
```Python
for x in df.index:
  if df.loc[x,"AVG"]>100:
    df.drop(x,inplace=True)
df
```
  </td>
  <td>
              
#### OUTPUT:

![image](https://github.com/SanjayRagavendar/Data-Cleaning-DataScience/assets/91368803/356a6df0-e9cb-46b1-98c8-11b33712629f)

</td>
</tr>
<tr>
  <td width=50%>

### 14)Cut and paste portion of image
```Python
     import cv2
     image=cv2.imread('Deepika.jpg',1)
     image=cv2.resize(image,(400,400))
     tag =image[150:200,110:160]
     image[110:160,150:200] = tag
     cv2.imshow('partimage1',image)
     cv2.waitKey(0)
     cv2.destroyAllWindows()
```
  </td>
  <td>

#### OUTPUT:

![image](https://github.com/SanjayRagavendar/Data-Cleaning-DataScience/assets/91368803/ea192f39-26da-4c60-bb84-74a7ab8ee6ac)
 </td>
 </tr>
</table>

# Result
The data clearning has beeen done successfully.
