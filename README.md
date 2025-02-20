# datafun-06-eda
This project is a custom exploratory data analysis project using many data analytics tools

## Project set up
Using template based on previous projects I created and set up the project 
1. Create repository in github named datafun-06-eda
2. Cloned down to local machine in VScode
``` 
cd ~
mkdir Projects
cd Projects
git clone https://github.com/s256657/datafun-06-eda
cd datafun-06-eda
code .
```
3. Added .gitignore and requirements.txt folders
4. created and activate virtual environment
```
python3 -m venv .venv
source .venv/bin/activate
```
5. Installed dependencies
```
python3 -m pip install --upgrade pip setuptools wheel
python3 -m pip install -r requirements.txt
```

## Import and test dataset
1. Create jupyter notebook mpg_eda.ipynb
2. Add markdown cell with title and purpose
3. Add code cell for imports
```
import pandas as pd
import seaborn as sns
import matplotlib
import jupyterlab
import pyarrow
```
4. Pull data set and test for confirmation
- I used a pre-created dataset through seaborn to perform analysis on
- Raw data also uploaded here https://github.com/s256657/datafun-06-eda/blob/main/mpg.csv
```
mpg_df: pd.DataFrame = sns.load_dataset('mpg')
mpg_df.columns
mpg_df.head()
```
- This should display the columns with a small section of the data to confirm it is pulled correctly.

## Initial Descriptive statistics and Data distribution
1. Check data for types in columns
2. Describe dataset
3. Create histograms of data
4. Value counts for all data columns

- All code can be found in mpg_eda.ipynb this step will show potential for analysis 

## Rename a column and add column
1. Rename name column to make/model
2. Create new column labeled mpg above 25
- This additional column will automatically group the mpg column into above and below 25 which will assist in creating visualizations later

## Visualizations
1. Visualization 1: 3 scatter plot charts showing relationships between horspower, weight, and mpg
2. Visualization 2: Pie chart showing the percentage above and below 25 mpg based on number of cylinders
3. Visualization 3: Stacked area chart showing origin of vehicle and representation of how many vehicles are above and below 25 mpg