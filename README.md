## Developed By: SAFEEQ FAZIL A
## Register No: 212222240086
##  Date: 

# Ex.No: 01 PLOT A TIME SERIES DATA


# AIM:
To Develop a python program to Plot a time series data of vegetable price.

# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Plot the data according to need and can be altered monthly, or yearly.
4. Display the graph.

# PROGRAM:
```python
import pandas as pd
import matplotlib.pyplot as plt

# Load the dataset
file_path = '/content/vegpred.csv' 
data = pd.read_csv(file_path)

# Convert the 'Date' column to datetime format
data['Date'] = pd.to_datetime(data['Date'])

# Filter the data for a specific commodity (e.g., "Potato Red")
commodity_name = 'Potato Red'
commodity_data = data[data['Commodity'] == commodity_name]

# Plot the time series for the selected commodity
plt.figure(figsize=(10, 6))
plt.plot(commodity_data['Date'], commodity_data['Average'], marker='o')
plt.title(f'Average Price of {commodity_name} Over Time')
plt.xlabel('Date')
plt.ylabel('Average Price (in Rs)')
plt.grid(True)
plt.xticks(rotation=45)
plt.tight_layout()
plt.show()

```


# OUTPUT:
![tsaexp1](https://github.com/user-attachments/assets/bd570992-8f80-4682-b6e6-539b66569e8d)


# RESULT:
Thus the python code has created for plotting the time series of given data.
