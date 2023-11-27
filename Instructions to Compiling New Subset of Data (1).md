# Instructions to Compiling New Subset of Data
Objective: Observing how socioeconomic status can impact healthcare outcomes 
### Procedures:
1. Importing Libraries
    1. Before writing down any form of code, import the pandas and numpy libraries 
    2. Type down ```import pandas as pd ``` and ```import numpy as np``` on the top most section of the file editor to be able to utilize the methods provided by these libraries.
2. Reading csv file
    1.  Copy the file path of the csv file by clicking the 3 dots that appears when mouse cursor is hovered over it
    2. Make a random variable like `read` for example, and use the function `pd.read_csv()` and put the copied path inside of the parentheses
3. Accessing a subset of the data given 
    1. A subset of data for a given state can be found using brackets and boolean selectors 
    2. First type the previously assigned variable `read` with brackets, so it looks like `read[]`
    3. Then, within the brackets, type `read['State'] == 'NC'` so only values for NC are selected and others are omitted
    4. Now make a copy of the sub dataset, which should look like `read[read['State'] == 'NC'].copy()`
    5. Lastly, assign it to a new variable called `NC` for example 
4. Accessing different values in the subset 
    1. Now to access data within the subset of the data that was extracted from the original file, create a new variable `NC_Health_Costs_Data` that goes with the data being extracted 
    2. If the desired data sets are `Health care costs` `Median household income` and `Could not see doctor due to cost`, then first type `NC[]` and within those brackets, type the desired column names separated by commas. For example, `NC[["State", "Year", "County", "Median household income", "Health care costs", "Could not see doctor due to cost"]]` (use year, county and state for a more detailed dataset)
    3. Now set that block of code to `NC_Health_Costs_Data` 
5. Exporting the dataset to a csv file 
    1. After accessing the desired sub dataset, to export it to a new csv file, the function `.to_csv()` can be used 
    2. Take the previously created variable `NC_Health_Costs_Data` and type `NC_Health_Costs_Data.to_csv()` and within those parentheses add the type the desired file name to be saved as, and if needed, omit the index values for the state. 
    3. Code should look like `NC_Health_Costs_Data.to_csv("NC_Health_Costs_Data", index=False)`
