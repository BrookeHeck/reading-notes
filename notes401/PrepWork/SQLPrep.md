# SQL Pre Work Notes
[SQL Bolt Tutorial](https://sqlbolt.com/lesson/introduction)
## Select Queries
- a statement which declares what dta we are looking for, where to find it, and possibly how to transform
- EXAMPLE:
``` 
SELECT column, another_column
FROM mytable;
```
- You can get all the data from a table with this command
```
SELECT *
FROM mytable;
```

## Queries with Constraints
- The WHERE clause in a query is used to filter out data by checking specific column values to determine whether it should be included in the results
- EXAMPLE:
```
SELECT column, another_column
FROM mytable
WHERE condition
  AND/OR another_condition
```
<img src="./../img/sqlConditions.png" width="500px" height="auto" />
<img src="./../img/sqlConditions2.png" width="500px" height="auto" />

## Filtering and Sorting Query Results
- Use the DISTINCT keyword to get rid of any rows that have a duplicate column value

```
SELECT DISTINCT colomn, another_column
FROM mytable
WHERE conditions(s)
```

- Use ORDER BY to sort your results by a given column in ascending or descending order
```
SELECT column, another_column, …
FROM mytable
WHERE condition(s)
ORDER BY column ASC/DESC
LIMIT num_limit OFFSET num_offset;
```
- LIMIT and OFFSET are used with ORDER BY to reduce the number or rows returned and where to begin counting the number of rows

## Multi-table Queries with JOINS
- the JOIN clause combines row data across two separate tables using a unique key
  - The INNER JOIN matches rows from a first and second table with the same key
  ```
  SELECT column, another_table_column, …
  FROM mytable
  INNER JOIN another_table 
    ON mytable.id = another_table.id
  WHERE condition(s)
  ORDER BY column, … ASC/DESC
  LIMIT num_limit OFFSET num_offset
  ```
  - LEFT, RIGHT, or FULL JOIN allow you to keep data in the results even if there is no match between the keys
  ```
    SELECT column, another_column, …
    FROM mytable
    INNER/LEFT/RIGHT/FULL JOIN another_table 
        ON mytable.id = another_table.matching_id
    WHERE condition(s)
    ORDER BY column, … ASC/DESC
    LIMIT num_limit OFFSET num_offset;
  ``` 

## NULLS in SQL
- Avoid getting null data by using defaults, such as 0
- When it's not possible to do this because default values will skew analysis of data, you can use IS/IS NOT NULL to filter null values

```
SELECT column, another_column, …
FROM mytable
WHERE column IS/IS NOT NULL
AND/OR another_condition
AND/OR …;
```

## Queries with Expressions


### Complete Tutorial Screen Shots
<img src="./../img/sqlTutorials/tutorial1.png" width="200px" height="auto" />
<img src="./../img/sqlTutorials/tutorial2.png" width="200px" height="auto" />
<img src="./../img/sqlTutorials/tutorial3.png" width="200px" height="auto" />
<img src="./../img/sqlTutorials/tutorial4.png" width="200px" height="auto" />
<img src="./../img/sqlTutorials/tutorial5.png" width="200px" height="auto" />
<img src="./../img/sqlTutorials/tutorial6.png" width="200px" height="auto" />
<img src="./../img/sqlTutorials/tutorial7.png" width="200px" height="auto" />
<img src="./../img/sqlTutorials/tutorial8.png" width="200px" height="auto" />
<img src="./../img/sqlTutorials/tutorial9.png" width="200px" height="auto" />
<img src="./../img/sqlTutorials/tutorial10.png" width="200px" height="auto" />
<img src="./../img/sqlTutorials/tutorial11.png" width="200px" height="auto" />
<img src="./../img/sqlTutorials/tutorial13.png" width="200px" height="auto" />
<img src="./../img/sqlTutorials/tutorial14.png" width="200px" height="auto" />
<img src="./../img/sqlTutorials/tutorial15.png" width="200px" height="auto" />
<img src="./../img/sqlTutorials/tutorial16.png" width="200px" height="auto" />
<img src="./../img/sqlTutorials/tutorial17.png" width="200px" height="auto" />
<img src="./../img/sqlTutorials/tutorial18.png" width="200px" height="auto" />

