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
import seaborn as sns
import matplotlib.pyplot as plt
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
<img width="666" height="454" alt="Screenshot 2025-10-15 225140" src="https://github.com/user-attachments/assets/4b4f0c82-3f91-4a7b-8a12-47a3c1df3711" />

df=sns.load_dataset("tips")
df
<img width="492" height="409" alt="Screenshot 2025-10-15 225343" src="https://github.com/user-attachments/assets/603fa8d1-686f-4ddd-965a-ac377d802b35" />

ineplot(x="total_bill",ysns.l="tip",data=df,hue="sex",linestyle='solid',legend="auto")
<img width="654" height="490" alt="Screenshot 2025-10-15 225538" src="https://github.com/user-attachments/assets/a802db5a-ebb0-463a-b201-ae3760d3dffe" />

x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title("Multi-line Plot")
plt.xlabel('X Label')
plt.ylabel('Y Label')
import seaborn as sns
import matplotlib.pyplot as plt
tips=sns.load_dataset('tips')
avg_total_bill = tips.groupby('day')['total_bill'].mean()
avg_tip=tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
<img width="662" height="496" alt="Screenshot 2025-10-15 225709" src="https://github.com/user-attachments/assets/a4ba7c16-8b58-46e6-a21f-30cc66d1237b" />

<img width="890" height="608" alt="Screenshot 2025-10-15 225817" src="https://github.com/user-attachments/assets/35d03e88-d94c-483e-ba4e-22f6a5e8ca1c" />

years=range (2000, 2012)
apples = [0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939]
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
<img width="684" height="469" alt="Screenshot 2025-10-15 230027" src="https://github.com/user-attachments/assets/538ef71f-435f-41a8-a669-50c7ee5789e5" />

avg_total_bill = tips.groupby('time')['total_bill'].mean()
avg_tip = tips.groupby('time')['tip'].mean()
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip', width=0.4)

plt.xlabel('Time of Day')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Time of Day')
plt.legend()
<img width="726" height="500" alt="Screenshot 2025-10-15 230138" src="https://github.com/user-attachments/assets/db2b3283-15e6-406a-ab6a-f939bdec2076" />

import seaborn as sns
# Load the tips dataset
tips = sns.load_dataset('tips')
# Scatter plot of total bill vs. tip amount
sns.scatterplot(x= 'total_bill', y='tip', hue='sex',data=tips)
# Set labels and title
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
<img width="718" height="500" alt="Screenshot 2025-10-15 230304" src="https://github.com/user-attachments/assets/1e143738-af70-487b-b29f-f55ccd786d27" />

import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
np.random.seed(0)
marks = np.random.normal(loc=70, scale=10, size=100)
marks
<img width="659" height="404" alt="Screenshot 2025-10-15 230442" src="https://github.com/user-attachments/assets/4d67d690-3470-4908-9269-b34ea5ddcc15" />

sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6,
palette="Set3", inner="quartile")
# Add labels and title
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
<img width="706" height="523" alt="Screenshot 2025-10-15 230634" src="https://github.com/user-attachments/assets/221e5a39-9f06-4079-af64-d02fb305bdfb" />

import seaborn as sns
sns.set(style = 'whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x=tip["total_bill"])
<img width="684" height="494" alt="Screenshot 2025-10-15 230747" src="https://github.com/user-attachments/assets/22691558-91bd-4e51-8bda-185b3aabd19a" />

eplsns.kdot(data=tips,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='Set2',alpha=0.8)
<img width="722" height="506" alt="Screenshot 2025-10-15 231030" src="https://github.com/user-attachments/assets/6c44c609-9f72-441b-bf69-44c05c6a9236" />

# Result:
   The above programm is succesfully verified
