# Big_Data_Statistical-Utilities-in-python-by-giving-any-data-set

## Aim :

To implement and demonstrate statistical utility functions in Python using a given dataset and calculate key statistical measures such as mean, median, mode, standard deviation, variance, range, skewness, and kurtosis.

## Equipments Required :

1. Python 3.x

2. Required libraries:


-- numpy for numerical operations


-- pandas for data handling


-- scipy.stats for statistical functions


3. Jupyter Notebook, Google Colab, or any Python IDE


## Procedure :

![image](https://github.com/user-attachments/assets/fc944818-1de3-40bc-822d-dc8e586dd065)


## Program :

```
Developed By : Niraunjana Gayathri G R
Register No. : 212222230096
```
```
import numpy as np
import pandas as pd
from scipy.stats import mode, skew, kurtosis

# Step 1: Define a dataset
data = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15]

# Step 2: Convert the dataset into a Pandas Series
data_series = pd.Series(data)

# Step 3: Calculate Measures of Central Tendency
mean_value = data_series.mean()
median_value = data_series.median()

# Mode calculation (fix for newer scipy versions)
mode_result = mode(data_series, keepdims=True)
mode_value = mode_result.mode[0] if len(mode_result.mode) > 0 else None

# Step 4: Calculate Measures of Dispersion
std_dev = data_series.std()
variance = data_series.var()
data_range = data_series.max() - data_series.min()

# Step 5: Analyze Distribution Shape
data_skewness = skew(data_series)
data_kurtosis = kurtosis(data_series)

# Step 6: Print all statistics
print("📊 Summary Statistics:")
print(f"Mean: {mean_value}")
print(f"Median: {median_value}")
print(f"Mode: {mode_value}")
print(f"Standard Deviation: {std_dev}")
print(f"Variance: {variance}")
print(f"Range: {data_range}")
print(f"Skewness: {data_skewness}")
print(f"Kurtosis: {data_kurtosis}")

```

## Output :

![image](https://github.com/user-attachments/assets/5e9f6b7e-85fc-4d0c-b96b-55b18773a4fb)


## Result :

The statistical utility functions were successfully implemented using Python. For the given dataset:


1. Central tendency measures indicate the dataset is symmetrically distributed (mean = median = 8).

2. Dispersion measures show moderate variability (Standard Deviation = 4.47).

3. Skewness is 0, confirming a perfectly symmetrical distribution.

4. Kurtosis < 0 indicates a platykurtic distribution (flatter than a normal distribution).


