Q1. List any five functions of the pandas library with execution.Here are five functions of the pandas library with examples of their execution:

1) read_csv() - This function is used to read a CSV file and return a pandas DataFrame.

2) head() - This function is used to return the first n rows of a DataFrame.

3) describe() - This function is used to generate descriptive statistics of a DataFrame.

4)groupby() - This function is used to group data by one or more columns and apply a function to the groups.

5)pivot_table() - This function is used to create a pivot table from a DataFrame.

```python
import pandas as pd

df = pd.read_csv('D:\\Data sets\\student_results.csv')
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Student ID</th>
      <th>Class</th>
      <th>Study hrs</th>
      <th>Sleeping hrs</th>
      <th>Social Media usage hrs</th>
      <th>Mobile Games hrs</th>
      <th>Percantege</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1001</td>
      <td>10</td>
      <td>2</td>
      <td>9</td>
      <td>3</td>
      <td>5</td>
      <td>50</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1002</td>
      <td>10</td>
      <td>6</td>
      <td>8</td>
      <td>2</td>
      <td>0</td>
      <td>80</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1003</td>
      <td>10</td>
      <td>3</td>
      <td>8</td>
      <td>2</td>
      <td>4</td>
      <td>60</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1004</td>
      <td>11</td>
      <td>0</td>
      <td>10</td>
      <td>1</td>
      <td>5</td>
      <td>45</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1005</td>
      <td>11</td>
      <td>4</td>
      <td>7</td>
      <td>2</td>
      <td>0</td>
      <td>75</td>
    </tr>
    <tr>
      <th>5</th>
      <td>1006</td>
      <td>11</td>
      <td>10</td>
      <td>7</td>
      <td>0</td>
      <td>0</td>
      <td>96</td>
    </tr>
    <tr>
      <th>6</th>
      <td>1007</td>
      <td>12</td>
      <td>4</td>
      <td>6</td>
      <td>0</td>
      <td>0</td>
      <td>80</td>
    </tr>
    <tr>
      <th>7</th>
      <td>1008</td>
      <td>12</td>
      <td>10</td>
      <td>6</td>
      <td>2</td>
      <td>0</td>
      <td>90</td>
    </tr>
    <tr>
      <th>8</th>
      <td>1009</td>
      <td>12</td>
      <td>2</td>
      <td>8</td>
      <td>2</td>
      <td>4</td>
      <td>60</td>
    </tr>
    <tr>
      <th>9</th>
      <td>1010</td>
      <td>12</td>
      <td>6</td>
      <td>9</td>
      <td>1</td>
      <td>0</td>
      <td>85</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.head(3)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Student ID</th>
      <th>Class</th>
      <th>Study hrs</th>
      <th>Sleeping hrs</th>
      <th>Social Media usage hrs</th>
      <th>Mobile Games hrs</th>
      <th>Percantege</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1001</td>
      <td>10</td>
      <td>2</td>
      <td>9</td>
      <td>3</td>
      <td>5</td>
      <td>50</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1002</td>
      <td>10</td>
      <td>6</td>
      <td>8</td>
      <td>2</td>
      <td>0</td>
      <td>80</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1003</td>
      <td>10</td>
      <td>3</td>
      <td>8</td>
      <td>2</td>
      <td>4</td>
      <td>60</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.describe()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Student ID</th>
      <th>Class</th>
      <th>Study hrs</th>
      <th>Sleeping hrs</th>
      <th>Social Media usage hrs</th>
      <th>Mobile Games hrs</th>
      <th>Percantege</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>10.00000</td>
      <td>10.000000</td>
      <td>10.000</td>
      <td>10.000000</td>
      <td>10.000000</td>
      <td>10.000000</td>
      <td>10.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>1005.50000</td>
      <td>11.100000</td>
      <td>4.700</td>
      <td>7.800000</td>
      <td>1.500000</td>
      <td>1.800000</td>
      <td>72.100000</td>
    </tr>
    <tr>
      <th>std</th>
      <td>3.02765</td>
      <td>0.875595</td>
      <td>3.335</td>
      <td>1.316561</td>
      <td>0.971825</td>
      <td>2.347576</td>
      <td>17.342626</td>
    </tr>
    <tr>
      <th>min</th>
      <td>1001.00000</td>
      <td>10.000000</td>
      <td>0.000</td>
      <td>6.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>45.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>1003.25000</td>
      <td>10.250000</td>
      <td>2.250</td>
      <td>7.000000</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>60.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>1005.50000</td>
      <td>11.000000</td>
      <td>4.000</td>
      <td>8.000000</td>
      <td>2.000000</td>
      <td>0.000000</td>
      <td>77.500000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>1007.75000</td>
      <td>12.000000</td>
      <td>6.000</td>
      <td>8.750000</td>
      <td>2.000000</td>
      <td>4.000000</td>
      <td>83.750000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>1010.00000</td>
      <td>12.000000</td>
      <td>10.000</td>
      <td>10.000000</td>
      <td>3.000000</td>
      <td>5.000000</td>
      <td>96.000000</td>
    </tr>
  </tbody>
</table>
</div>




```python
grouped = df.groupby(['Study hrs','Class']).groups
grouped
```




    {(0, 11): [3], (2, 10): [0], (2, 12): [8], (3, 10): [2], (4, 11): [4], (4, 12): [6], (6, 10): [1], (6, 12): [9], (10, 11): [5], (10, 12): [7]}




```python
df=pd.read_csv('D:\\Data sets\\Movie_rating.csv')
df
df.pivot_table(index='Genre',columns='Year')
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead tr th {
        text-align: left;
    }

    .dataframe thead tr:last-of-type th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr>
      <th></th>
      <th colspan="4" halign="left">Budget(M$)</th>
      <th colspan="4" halign="left">Ratings%</th>
    </tr>
    <tr>
      <th>Year</th>
      <th>2002</th>
      <th>2008</th>
      <th>2009</th>
      <th>2010</th>
      <th>2002</th>
      <th>2008</th>
      <th>2009</th>
      <th>2010</th>
    </tr>
    <tr>
      <th>Genre</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Action</th>
      <td>NaN</td>
      <td>30.0</td>
      <td>200.0</td>
      <td>20.0</td>
      <td>NaN</td>
      <td>52.5</td>
      <td>63.0</td>
      <td>52.0</td>
    </tr>
    <tr>
      <th>Adventure</th>
      <td>NaN</td>
      <td>105.0</td>
      <td>18.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>44.0</td>
      <td>84.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>Comedy</th>
      <td>8.0</td>
      <td>25.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>81.0</td>
      <td>70.5</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>


Q2. Given a Pandas DataFrame df with columns 'A', 'B', and 'C', write a Python function to re-index the DataFrame with a new index that starts from 1 and increments by 2 for each row.

```python
import pandas as pd

def reindex_df(df):
    
    n_rows = df.shape[0]
    
    new_index = []
    
    for i in range(n_rows):
        new_index.append(i*2+1)
        
    df.index = new_index
    return df

df = pd.DataFrame({'A':[1,2,3,4,5], 'B':['Male','Female','Male','Female','Male'],
                  'C':[9,4,5,6,8]})
df = reindex_df(df)
print(df)
```

       A       B  C
    1  1    Male  9
    3  2  Female  4
    5  3    Male  5
    7  4  Female  6
    9  5    Male  8
    
Q3. You have a Pandas DataFrame df with a column named 'Values'. Write a Python function that 
iterates over the DataFrame and calculates the sum of the first three values in the 'Values' column. The 
function should print the sum to the console.

For example, if the 'Values' column of df contains the values [10, 20, 30, 40, 50], your function should 
calculate and print the sum of the first three values, which is 60.

```python
import pandas as pd

def sum_of_first_three(df):
    
    first_three_values = df['Values'][:3]
    
    sum_first_three = sum(first_three_values)
    
    print("Sum of the first three values in the 'Values' column:", sum_first_three)

df = pd.DataFrame({'Values':[10,20,30,40,50]})
sum_of_first_three(df)
```

    Sum of the first three values in the 'Values' column: 60
    
Q4. Given a Pandas DataFrame df with a column 'Text', write a Python function to create a new column 'Word_Count' that contains the number of words in each row of the 'Text' column

```python
import pandas as pd

def add_word_count_column(df):
    
    word_lists = df['Text'].str.split()
    
    df['Word_count'] = word_lists.apply(len)
    
    return df

df = pd.DataFrame({'Text': ['The quick brown fox', 'jumps over the lazy dog']})

df = add_word_count_column(df)

print(df)
```

                          Text  Word_count
    0      The quick brown fox           4
    1  jumps over the lazy dog           5
    
Q5. How are DataFrame.size() and DataFrame.shape() different?
Ans:
DataFrame.size returns the total number of elements in the DataFrame, which is the product of the number of rows and the number of columns.

DataFrame.shape returns a tuple containing the number of rows and columns in the DataFrame.

So, DataFrame.size returns a single integer value, while DataFrame.shape returns a tuple of two integers.

Q6. Which function of pandas do we use to read an excel file?
Ans:
import pandas as pd

df = pd.read_excel('file.xlsx')

This will read the Excel file 'file.xlsx' and create a pandas DataFrame df containing its data. By default, read_excel() reads the first sheet of the Excel file, but you can specify a particular sheet by passing its name or index as an argument to the function. You can also specify various options for reading Excel files, such as the range of rows and columns to read, the header row to use, and so on. You can find more information on the read_excel() function in the pandas documentation.Q7. You have a Pandas DataFrame df that contains a column named 'Email' that contains email 
addresses in the format 'username@domain.com'. Write a Python function that creates a new column 
'Username' in df that contains only the username part of each email address.

The username is the part of the email address that appears before the '@' symbol. For example, if the 
email address is 'john.doe@example.com', the 'Username' column should contain 'john.doe'. Your 
function should extract the username from each email address and store it in the new 'Username' 
column.

```python
def add_username_column(df):
    
    username_column = df['EMail'].str.split('@')
    
    df['Username'] = username_column.apply(lambda x : x[0])
    
    return df

df =pd.DataFrame({'EMail':['john.doe@example.com', 'jane.doe@example.com']})
df = add_username_column(df)
print(df)
```

                      EMail  Username
    0  john.doe@example.com  john.doe
    1  jane.doe@example.com  jane.doe
    
Q8. You have a Pandas DataFrame df with columns 'A', 'B', and 'C'. Write a Python function that selects all rows where the value in column 'A' is greater than 5 and the value in column 'B' is less than 10. The 
function should return a new DataFrame that contains only the selected rows.

For example, if df contains the following values:

   A   B   C

0  3   5   1

1  8   2   7

2  6   9   4

3  2   3   5

4  9   1   2

Your function should select the following rows:   A   B   C

1  8   2   7

4  9   1   2

The function should return a new DataFrame that contains only the selected rows

```python
import pandas as pd

def select_rows(df):
    
    return df[(df['A'] > 5) & (df['B'] < 10)]

df = pd.DataFrame({'A': [3, 8, 6, 2, 9], 'B': [5, 2, 9, 3, 1], 
                   'C': [1, 7, 4, 5, 2]})

selected_rows = select_rows(df)

print(selected_rows)
```

       A  B  C
    1  8  2  7
    2  6  9  4
    4  9  1  2
    
Q9. Given a Pandas DataFrame df with a column 'Values', write a Python function to calculate the mean, median, and standard deviation of the values in the 'Values' column.

```python
import pandas as pd

def calculate_stats(df):
    
    mean = df['Values'].mean()
    median = df['Values'].median()
    std_dev = df['Values'].std()
    return mean,median,std_dev

df = pd.DataFrame({'Values': [2, 5, 7, 3, 8, 6, 9, 1, 4]})

mean, median, std_dev = calculate_stats(df)
print('Mean:', mean)
print('Median:', median)
print('Standard deviation:', std_dev)
```

    Mean: 5.0
    Median: 5.0
    Standard deviation: 2.7386127875258306
    
Q10. Given a Pandas DataFrame df with a column 'Sales' and a column 'Date', write a Python function to create a new column 'MovingAverage' that contains the moving average of the sales for the past 7 days for each row in the DataFrame. The moving average should be calculated using a window of size 7 and should include the current day.

```python
import pandas as pd

def add_moving_average(df):
    df['MovingAverage'] = df['Sales'].rolling(window=7, min_periods=1).mean()
    return df

df = pd.DataFrame({'Sales': [10, 15, 12, 18, 20, 25, 22, 28, 30, 35],
                   'Date': ['2022-01-01', '2022-01-02', '2022-01-03', '2022-01-04', '2022-01-05',
                            '2022-01-06', '2022-01-07', '2022-01-08', '2022-01-09', '2022-01-10']})

df['Date'] = pd.to_datetime(df['Date'])

df.set_index('Date',inplace = True)

df = add_moving_average(df)

print(df)
```

                Sales  MovingAverage
    Date                            
    2022-01-01     10      10.000000
    2022-01-02     15      12.500000
    2022-01-03     12      12.333333
    2022-01-04     18      13.750000
    2022-01-05     20      15.000000
    2022-01-06     25      16.666667
    2022-01-07     22      17.428571
    2022-01-08     28      20.000000
    2022-01-09     30      22.142857
    2022-01-10     35      25.428571
    
Q11. You have a Pandas DataFrame df with a column 'Date'. Write a Python function that creates a new column 'Weekday' in the DataFrame. The 'Weekday' column should contain the weekday name (e.g. Monday, Tuesday) corresponding to each date in the 'Date' column.

For example, if df contains the following values:

         Date

0  2023-01-01

1  2023-01-02

2  2023-01-03

3  2023-01-04

4  2023-01-05

Your function should create the following DataFrame:


         Date    Weekday

0  2023-01-01    Sunday

1  2023-01-02     Monday

2  2023-01-03    Tuesday

3  2023-01-04    Wednesday

4  2023-01-05    Thursday

The function should return the modified DataFrame.

```python
import pandas as pd

def add_weekday_column(df):
    
    df['Date'] = pd.to_datetime(df['Date'])
    
    df['Weekday'] = df['Date'].dt.day_name()
    
    return df

df = pd.DataFrame({'Date':[ '2023-01-01','2023-01-02','2023-01-03'
                           ,'2023-01-04','2023-01-05']})

df = add_weekday_column(df)

df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Date</th>
      <th>Weekday</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2023-01-01</td>
      <td>Sunday</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2023-01-02</td>
      <td>Monday</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2023-01-03</td>
      <td>Tuesday</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2023-01-04</td>
      <td>Wednesday</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2023-01-05</td>
      <td>Thursday</td>
    </tr>
  </tbody>
</table>
</div>


Q12. Given a Pandas DataFrame df with a column 'Date' that contains timestamps, write a Python function to select all rows where the date is between '2023-01-01' and '2023-01-31'.

```python
import pandas as pd

def select_date_time_range(df):
    
    df['Date'] = pd.to_datetime(df['Date'])
    
    date_range = (df['Date'] >= '2023-01-01') &  (df['Date'] >= '2023-01-31')
    
    return df[date_range]

df = select_date_time_range(df)
print(df)
   
```

    Empty DataFrame
    Columns: [Date, Weekday]
    Index: []
    
Q13. To use the basic functions of pandas, what is the first and foremost necessary library that needs to be imported?The first and foremost necessary library that needs to be imported to use the basic functions of pandas is pandas itself. This can be done using the import statement, like so:

import pandas as pd

Here, we are importing the pandas library and giving it the alias pd to make it easier to refer to throughout our code. Once we have imported pandas, we can use its functions and classes to create, manipulate, and analyze data stored in pandas objects such as Series and DataFrame.


```python

```
