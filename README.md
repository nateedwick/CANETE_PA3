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

  ```python
   import pandas as pd
    cars = pd.read_csv('cars.csv')
  FirstFive_odd = cars.loc[[0,1,2,3,4],['Model', 'cyl', 'hp', 'wt', 'vs', 'gear']]
  FirstFive_odd
  ```
  - **Output:**
 [Problem 2A Output](
- 
    words = sentence.split()                  # split into list of words
    new_words = []                            # empty list para istore bagong version ng words

    for w in words:                           # go through each word one by one
        lw = w.lower()                        # make the word lowercase
        if lw in d:                           # check in dictionary
            new_words.append(d[lw])           # replace with emoticon
        else:
            new_words.append(w)               # retain orig. word pag wala sa dictionary

    return " ".join(new_words)                # compile lahat ng nasa new_words with spaces in between\

- **Output:**
  ```python
  print(emotify("Make me smile"))   # Make me :)
  print(emotify("I am mad"))        # I am >:(

> Make me :)\
> I am >:(

### 3. Unpacking List Problem
- **Goal:** Unpack the list writeyourcodehere into three variables, being first, middle, and last, with middle being everything in between the first and last element. Then print all three variables.
- **Code:**  Create a list called lst that contains several numbers. To unpack it, assign the first element lst[0] to the variable first, all elements in between lst[1:-1] to the variable middle, and the last element lst[-1] to the variable last. The expression lst[0] directly accesses the first element in the list. The slice lst[1:-1] takes everything except the first and last elements, which makes up the middle part of the list. The expression lst[-1] accesses the last element using negative indexing.
  
  ```python
    lst = [1, 2, 3, 4, 5, 6]
    
    first = lst[0]                                # take first item in the list (index 0 = 1)
    middle = lst[1:-1]                            # take all items except yung first at yung last ([2,3,4,5])
    last = lst[-1]                                # take last item in the list (index -1 = 6)


- **Output:**
  ```python
    print("first:", first)                       
    print("middle:", middle)
    print("last:", last)

> first: 1\
> middle: [2, 3, 4, 5]\
> last: 6
