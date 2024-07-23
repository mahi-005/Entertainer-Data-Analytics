# Entertainer Data Analysis Project

## Project Overview

This project involves analyzing a dataset of entertainers to uncover insights and trends in the entertainment industry. The analysis includes merging multiple datasets, cleaning the data, and performing exploratory data analysis (EDA).

## Files in the Project

- `Entertainer - Basic Info.xlsx`: Contains basic information about entertainers.
- `Entertainer - Breakthrough Info.xlsx`: Contains information about entertainers' breakthrough moments.
- `Entertainer - Last work Info.xlsx`: Contains information about entertainers' last major works.

## Code Description

### Mounting Google Drive

```python
from google.colab import drive
drive.mount('/content/drive')
```

### Importing Libraries

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
%matplotlib inline
import seaborn as sns
```

### Loading the Datasets

```python
df1 = pd.read_excel('/content/drive/MyDrive/Entertainer Project/Entertainer - Basic Info.xlsx')
df2 = pd.read_excel('/content/drive/MyDrive/Entertainer Project/Entertainer - Breakthrough Info.xlsx')
df3 = pd.read_excel('/content/drive/MyDrive/Entertainer Project/Entertainer - Last work Info.xlsx')
```

### Verifying Column Names

```python
print("Columns in df1:", df1.columns)
print("Columns in df2:", df2.columns)
print("Columns in df3:", df3.columns)
```

### Merging the Dataframes

```python
inner_join1 = pd.merge(df1, df2, on='Entertainer', how='inner')
inner_join_final = pd.merge(inner_join1, df3, on='Entertainer', how='inner')
inner_join_final.head()
```

## How to Run the Code

1. **Mount Google Drive**: Ensure your Google Drive is mounted to access the datasets.
2. **Import Libraries**: Import necessary libraries for data manipulation and visualization.
3. **Load the Datasets**: Load the datasets from the specified paths.
4. **Verify Column Names**: Check the column names to ensure they match across datasets.
5. **Merge the Dataframes**: Merge the datasets on the 'Entertainer' column.

## Future Work

- Perform exploratory data analysis (EDA) to uncover trends and insights.
- Visualize the data using various plotting techniques.
- Apply machine learning models to predict future trends in the entertainment industry.

## Contact

For any questions or suggestions, feel free to reach out to me on LinkedIn.
