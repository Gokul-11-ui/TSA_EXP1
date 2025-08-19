# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date:19/08/2025 

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
```
from google.colab import files
uploaded = files.upload()

import pandas as pd
import matplotlib.pyplot as plt

# Replace with your uploaded file name
df = pd.read_csv("bitstamp (USD) 20211 - 2024.csv")

# Convert Timestamp column to datetime (if it exists)
df['Timestamp'] = pd.to_datetime(df['Timestamp'])
df.set_index('Timestamp', inplace=True)

# Show first few rows
df.head()

plt.figure(figsize=(12,6))
plt.plot(df['Close'], label='Close Price')
plt.title("Bitcoin Price Over Time")
plt.xlabel("Date")
plt.ylabel("Price (USD)")
plt.legend()
plt.grid(True)
plt.show()
```










# OUTPUT:<img width="1300" height="678" alt="Screenshot 2025-08-19 082901" src="https://github.com/user-attachments/assets/ae2a701e-5c9a-4b34-b5d7-7b6d7b6f0fd1" />







# RESULT:
Thus we have created the python code for plotting the time series of given data.
