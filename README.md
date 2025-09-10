# ADVANCED PROGRAMMING: Programming Assignment #3

## Project Overview  
This project contains solutions to data analysis problems using the Pandas library as part of Advanced Programming Assignment 3.
It demonstrates how to identify, apply, and combine different Pandas functions to analyze datasets.
The problems cover essential concepts such as loading CSV files, displaying data frames, subsetting, slicing, and indexing.

## Getting Started
The code can be run in any Python environment or IDE. For this project, Jupyter Notebook was used through Anaconda Navigator to write and execute the solutions.

The dataset used in this assignment (cars.csv) was provided through the experiment instructions.
For convenience, the same CSV file is also uploaded in this GitHub repository alongside the Jupyter Notebook, so that users can run the code directly

## Problems and Solutions

### 1. Data Loading and Display Problem
- **Goal:** Load the provided .csv file into a Pandas DataFrame and display the first five and last five rows.

- **Code:**  Import the Pandas library and use the pd.read_csv() function to load the CSV file into a DataFrame named cars. To display the first five rows, call the .head() method, and to display the last five rows, call the .tail() method.
  ```python
  import pandas as pd
  cars = pd.read_csv('cars.csv')
  cars

This will load the .csv file into a Pandas DataFrame

  ```python
   cars.head()
```
- **Output:**
[Cars Head Output](FirstFive.png)

```python
   cars.tail()
```
- **Output:**
[Cars Tail Output](LastFive.png)
      

 ### 2. Data Subsetting and Indexing Problem 
- **Goal:** Using the DataFrame cars from Problem 1, extract specific information using subsetting, slicing, and indexing operations.
- **Code:** Begin by loading the CSV file into a DataFrame named cars using the pd.read_csv() function. Use the .loc[] method to filter rows and select specific columns based on conditions. For Problem a, select the first five rows with odd-numbered columns by explicitly listing the column names. For Problem b, apply a condition to select the row with the model 'Mazda RX4'. For Problem c, filter the DataFrame to select only the cyl column for the model 'Camaro Z28'. For Problem d, run separate .loc[] commands for each model (Mazda RX4 Wag, Ford Pantera L, and Honda Civic) to display their corresponding cyl and gear values. An alternative approach is to use the .isin() function to combine all three conditions in one run, but the original solution uses multiple lines of code.

a.
  ```python
   import pandas as pd
    cars = pd.read_csv('cars.csv')
  FirstFive_odd = cars.loc[[0,1,2,3,4],['Model', 'cyl', 'hp', 'wt', 'vs', 'gear']]
  FirstFive_odd
  ```
  - **Output:**
[Cars Head Output](Problem2A.png)

b.
  ```python
   cars.loc[cars['Model']=='Mazda RX4']
  ```
  - **Output:**
 [Problem 2B Output](Problem 2B.png)

c.
  ```python
   cars.loc[(cars['Model']=='Camaro Z28'), ['cyl']]
  ```
  - **Output:**
 [Problem 2C Output](Problem 2C.png)
  
d.
  ```python
   cars.loc[cars['Model'].isin(['Mazda RX4 Wag', 'Ford Pantera L', 'Honda Civic']), ['cyl', 'gear']]
  ```
  - **Output:**
 [Problem 2D Output](Problem 2D.png)

