### `query` filtering

`query` provides a flexible and expressive way to perform complex filtering. 
You can use various comparison operators, string methods, functions, and logical operators 
within the query expression to specify your filtering criteria. 

- Basic query filtering:
```python

# Filtering using the query method
filtered_data = df.query('column1 > 10 and column2 == "A"')
```
This applies a filter to the DataFrame df using the query() method. It selects rows where the 
values in the column 'column1' are greater than 10 and the values in the column 'column2' are equal 
to 'A'.

- Filtering with string methods:
```python
# Filtering based on string methods in query
filtered_data = df.query('column.str.contains("apple", case=False)')
```
This filters the DataFrame to include only the rows where the values in the 'column' 
column contain the substring 'apple'.

- Filtering with functions:
```python
# Filtering using custom functions in query
filtered_data = df.query('custom_function(column) > 10')
```
In this example, a custom function is defined and used within the query expression. 
It filters the DataFrame based on the result of the custom_function() applied to the values 
in the 'column' column.

- Filtering with multiple conditions:
```python
# Filtering with multiple conditions in query
filtered_data = df.query('(column1 > 10) & (column2 == "A" or column2 == "B")')
```
This filters the DataFrame using multiple conditions within the query expression. 
It selects rows where the values in 'column1' are greater than 10 and the values in 
'column2' are either 'A' or 'B'.

## Task
In the DataFrame, leave only the data that meets the following criteria:
1. Age is less than or equal to 60.
2. Name starts with A or D.
3. Surname is not "Brown".