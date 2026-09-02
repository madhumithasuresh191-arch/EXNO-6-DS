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

~~~
import pandas as pd
data = {
    'Order_ID': range(1, 21),
    'Month': [
        'Jan', 'Jan', 'Feb', 'Feb', 'Mar', 'Mar',
        'Apr', 'Apr', 'May', 'May', 'Jun', 'Jun',
        'Jul', 'Jul', 'Aug', 'Aug', 'Sep', 'Oct',
        'Nov', 'Dec'
    ],
    'Product': [
        'Laptop', 'Mobile', 'Laptop', 'Tablet', 'Mobile', 'Laptop',
        'Tablet', 'Accessories', 'Laptop', 'Mobile', 'Tablet', 'Laptop',
        'Mobile', 'Accessories', 'Laptop', 'Tablet', 'Mobile', 'Laptop',
        'Mobile', 'Laptop'
    ],
    'Category': [
        'Electronics', 'Electronics', 'Electronics', 'Electronics',
        'Electronics', 'Electronics', 'Electronics', 'Accessories',
        'Electronics', 'Electronics', 'Electronics', 'Electronics',
        'Electronics', 'Accessories', 'Electronics', 'Electronics',
        'Electronics', 'Electronics', 'Electronics', 'Electronics'
    ],
   'Region': [
        'North', 'South', 'East', 'West', 'North', 'South',
        'East', 'West', 'North', 'South', 'East', 'West',
        'North', 'South', 'East', 'West', 'North', 'South',
        'East', 'West'
    ],
    'Quantity': [
        5, 12, 7, 6, 15, 8, 10, 20, 9, 14,
        7, 11, 18, 25, 10, 8, 16, 12, 20, 15
    ],
    'Unit_Price': [
        60000, 25000, 62000, 30000, 27000, 65000,
        32000, 5000, 68000, 28000, 31000, 70000,
        30000, 4500, 72000, 33000, 29000, 75000,
        31000, 78000
    ],
    'Sales': [
        300000, 300000, 434000, 180000, 405000, 520000,
        320000, 100000, 612000, 392000, 217000, 770000,
        540000, 112500, 720000, 264000, 464000, 900000,
        620000, 1170000
    ],

'Profit': [
        60000, 45000, 85000, 27000, 65000, 90000,
        48000, 20000, 110000, 60000, 35000, 130000,
        85000, 25000, 120000, 40000, 70000, 150000,
        95000, 190000
    ],
    'Advertising': [
        20000, 18000, 25000, 12000, 22000, 28000,
        16000, 8000, 30000, 20000, 14000, 35000,
        26000, 10000, 32000, 15000, 24000, 40000,
        30000, 45000
    ]
}

df = pd.DataFrame(data)
df
~~~
 <img width="1920" height="1020" alt="Screenshot 2026-09-02 160121" src="https://github.com/user-attachments/assets/fc45cf0a-b716-4b34-8d38-1e0b3d447a38" />
<img width="1920" height="1020" alt="Screenshot 2026-09-02 160130" src="https://github.com/user-attachments/assets/f9dd37d1-73d0-48d4-a10f-3334928ea916" />
<img width="1920" height="1020" alt="Screenshot 2026-09-02 160144" src="https://github.com/user-attachments/assets/7aa4d4f3-9597-45b2-b782-94a478a0f0b2" />
<img width="1920" height="1020" alt="Screenshot 2026-09-02 160153" src="https://github.com/user-attachments/assets/5876af29-1581-4048-8781-3685666f3716" />

~~~
import seaborn as sns
import matplotlib.pyplot as plt
sns.set_theme(style="whitegrid")
~~~



~~~
sns.countplot(data=df, x='Product',hue='Category')
plt.title('Number of Orders by Product with category Differentaition')
plt.show()
~~~




<img width="1920" height="1020" alt="Screenshot 2026-09-02 160206" src="https://github.com/user-attachments/assets/9849f7ef-839e-4019-8ba7-e12a037dc578" />


~~~
sns.barplot(data=df,x='Product',y='Sales')
plt.title('Average Sales by Product')
plt.show()
~~~



<img width="1920" height="1020" alt="Screenshot 2026-09-02 160215" src="https://github.com/user-attachments/assets/98b0a4f2-13a5-4c77-811f-be8e8ac40b2d" />



~~~
sns.lineplot(data=df,x='Month',y='Sales',hue='Product',marker='o')
plt.title('Monthly Sales by Product')
plt.show()
~~~





<img width="1920" height="1020" alt="Screenshot 2026-09-02 160226" src="https://github.com/user-attachments/assets/ad1287e9-dd3e-4185-96ef-2d47b0e0fe18" />


~~~
sns.barplot(data=df,x='Sales',y='Region')
plt.title('Average Sales by Region')
plt.show()
~~~



<img width="1920" height="1020" alt="Screenshot 2026-09-02 160235" src="https://github.com/user-attachments/assets/18dc7af4-4609-46a5-b197-85dc684061cf" />



~~~
sns.scatterplot(
    data=df,
    x='Advertising',
    y='Sales'

)
plt.title('Adervertising vs Sales')
plt.show()
~~~



<img width="1920" height="1020" alt="Screenshot 2026-09-02 160245" src="https://github.com/user-attachments/assets/319a3baa-d5aa-4e60-b746-7a3dd6322f5e" />



~~~
sns.scatterplot(
    data=df,
    x='Advertising',
    y='Sales',
    hue='Product',
    size='Profit'

)
plt.title('Advertising vs Sales')
plt.show()
~~~





<img width="1920" height="1020" alt="Screenshot 2026-09-02 160300" src="https://github.com/user-attachments/assets/b89b1789-d14e-42a3-b4b3-84d6b22e95b3" />


~~~
sns.histplot(
    data=df,
    x='Sales',
    bins=8
)
plt.title('Sales Distribution')
plt.show()
~~~



<img width="1920" height="1020" alt="Screenshot 2026-09-02 160309" src="https://github.com/user-attachments/assets/541002a3-98a8-4578-834b-2ab7d789519b" />



~~~
sns.histplot(
    data=df,
    x='Sales',
    bins=8,
    kde=True
)
plt.title('Sales Distribution with kde')
plt.show()
~~~


<img width="1920" height="1020" alt="Screenshot 2026-09-02 160318" src="https://github.com/user-attachments/assets/50599c51-4bd9-4a58-a78f-b972bb6f57de" />



~~~
sns.boxplot(
    data=df,
    x='Product',
    y='Sales'
)
plt.title('Sales distribution by Product')
plt.show()

~~~




<img width="1920" height="1020" alt="Screenshot 2026-09-02 160328" src="https://github.com/user-attachments/assets/836385fb-1674-4812-ba97-4a82db104b0b" />



~~~
sns.violinplot(
    data=df,
    x='Product',
    y='Sales'
)
plt.title('Sales distribution by Product')
plt.show()
~~~



<img width="1920" height="1020" alt="Screenshot 2026-09-02 160336" src="https://github.com/user-attachments/assets/017a71b6-30a7-4e23-acfd-71500b5bfb67" />



~~~
sns.stripplot(
    data=df,
    x='Product',
    y='Sales'
    
)
plt.title('Sales distribution by Product')
plt.show()
~~~



<img width="1920" height="1020" alt="Screenshot 2026-09-02 160344" src="https://github.com/user-attachments/assets/a16faeb2-86a9-4520-b8b2-f110828a8e57" />



~~~
sns.swarmplot(
    data=df,
    x='Product',
    y='Sales'
    
)
plt.title('Sales distribution by Product')
plt.show()
~~~


<img width="1920" height="1020" alt="Screenshot 2026-09-02 160354" src="https://github.com/user-attachments/assets/97c358d4-3b46-48f2-9e66-281de2f65807" />



~~~
corr=df[
    ['Quantity','Unit_Price','Sales','Profit','Advertising']

].corr()
corr
~~~


<img width="1920" height="1020" alt="Screenshot 2026-09-02 160403" src="https://github.com/user-attachments/assets/57dd4167-f972-4f64-bd22-58e78b082272" />


~~~
sns.heatmap(
    corr,
    annot=True,
    cmap='coolwarm'
)
plt.title('Correlation Heatmap')
plt.show()
~~~



<img width="1920" height="1020" alt="Screenshot 2026-09-02 160412" src="https://github.com/user-attachments/assets/0f1cac28-7b2a-4e5f-a162-d21c08bb9588" />



~~~
sns.pairplot(
    df[
        ['Quantity','Unit_Price','Sales','Profit','Advertising']
    ]
)
plt.show()
~~~


<img width="1920" height="1020" alt="Screenshot 2026-09-02 160422" src="https://github.com/user-attachments/assets/d940dd36-bbd3-4d72-ba26-976058edb438" />
<img width="1920" height="1020" alt="Screenshot 2026-09-02 160432" src="https://github.com/user-attachments/assets/fa9c5adb-cda6-4e6a-90af-17ce885686a6" />


~~~
sns.pairplot(
    df[
        ['Quantity','Unit_Price','Sales','Profit','Advertising','Product']
    ],
    hue='Product'
)
plt.show()
~~~



<img width="1920" height="1020" alt="Screenshot 2026-09-02 160445" src="https://github.com/user-attachments/assets/7f3d44cc-0c46-443a-9689-8dfb70e08d9d" />
<img width="1920" height="1020" alt="Screenshot 2026-09-02 160457" src="https://github.com/user-attachments/assets/d4dd6bb3-23cc-4d6b-ab70-c44194fc4e0d" />
<img width="1920" height="1020" alt="Screenshot 2026-09-02 160522" src="https://github.com/user-attachments/assets/2ea4cf0d-506a-4ce8-bf8a-b5315f7a3b1b" />


~~~
sns.jointplot(
    data=df,
    x='Advertising',
    y='Sales',
    kind='scatter'
)
plt.show()

~~~



<img width="1920" height="1020" alt="Screenshot 2026-09-02 160535" src="https://github.com/user-attachments/assets/54c81fb8-6ddd-4117-9459-235d19e0a539" />
<img width="1920" height="1020" alt="Screenshot 2026-09-02 160550" src="https://github.com/user-attachments/assets/32718bbc-1d7e-46fc-a632-6b0855637558" />
<img width="1920" height="1020" alt="Screenshot 2026-09-02 160559" src="https://github.com/user-attachments/assets/fa7eb838-a0f7-48ff-9a3f-153bc5b3a9e5" />
<img width="1920" height="1020" alt="Screenshot 2026-09-02 160608" src="https://github.com/user-attachments/assets/4c7680a5-ece3-4e57-8c66-9236421c475d" />
<img width="1920" height="1020" alt="Screenshot 2026-09-02 160617" src="https://github.com/user-attachments/assets/b32a04cd-3440-4735-92c1-61d87ab09758" />
<img width="1920" height="1020" alt="Screenshot 2026-09-02 160625" src="https://github.com/user-attachments/assets/fa0ca1fb-6c90-4052-a542-c666e6c57930" />



# Result:
 Include your result here
