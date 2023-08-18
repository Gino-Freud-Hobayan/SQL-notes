# SQL-notes

# DATE FUNCTIONS

<br>
<br>
<BR>

**DATEDIFF**

In Microsoft SQL Server (MS SQL), the `DATEDIFF` function is used to calculate the difference between two date or datetime values. The syntax for using the `DATEDIFF` function in MS SQL is as follows:

```sql
DATEDIFF(datepart, startdate, enddate)
```

Where:
- `datepart`: This specifies the unit of time for which you want to calculate the difference, such as 'day', 'month', 'year', etc.
- `startdate`: The starting date or datetime value.
- `enddate`: The ending date or datetime value.

Here's an example of how you might use the `DATEDIFF` function in MS SQL:

```sql
SELECT DATEDIFF(day, '2023-01-01', '2023-01-15') AS DaysDifference;
```

This query calculates the difference in days between January 1, 2023, and January 15, 2023.

<br>

Here are a few examples of other dateparts you can use with the `DATEDIFF` function in MS SQL:

```sql
-- Calculate difference in months
SELECT DATEDIFF(month, '2023-01-01', '2023-06-01') AS MonthsDifference;

-- Calculate difference in years
SELECT DATEDIFF(year, '2000-01-01', '2023-01-01') AS YearsDifference;
```

Remember that the supported dateparts and the behavior of the `DATEDIFF` function can vary depending on the version of SQL Server you're using. Always consult the official Microsoft SQL Server documentation for the specific version you're working with to ensure accurate usage.

<BR>
<BR>

In addition to the `DATEDIFF` function, there are several other common time-related functions available in SQL for working with dates and times. Here are some of the most frequently used time functions:

1. **GETDATE() / CURRENT_TIMESTAMP**: Returns the current date and time.

   ```sql
   SELECT GETDATE() AS CurrentDateTime;
   ```

<br>


2. **DATEADD**: Adds a specified number of date or time intervals to a given date.

   ```sql
   SELECT DATEADD(day, 7, '2023-08-18') AS NewDate;
   ```

   <br>

3. **DATEDIFF**: As mentioned earlier, calculates the difference between two dates or times.

<br>

4. **DATEPART**: Extracts a specific part (e.g., year, month, day) from a date or time.

   ```sql
   SELECT DATEPART(year, '2023-08-18') AS Year;
   SELECT DATEPART(month, '2023-08-18') AS Month;
   ```

<br>

5. **CONVERT / CAST**: Used to convert between different date and time data types or formats.

   ```sql
   SELECT CONVERT(VARCHAR, GETDATE(), 120) AS FormattedDate;
   SELECT CAST('2023-08-18' AS DATETIME) AS DateValue;
   ```

<br>

6. **FORMAT**: Formats a date or time value as a string according to a specified format.

   ```sql
   SELECT FORMAT(GETDATE(), 'yyyy-MM-dd HH:mm:ss') AS FormattedDate;
   ```

<br>


7. **DATEFROMPARTS**: Creates a date value from individual year, month, and day components.

   ```sql
   SELECT DATEFROMPARTS(2023, 8, 18) AS FullDate;
   ```

<br>

8. **DATEDIFF_BIG**: Similar to `DATEDIFF`, but returns a `BIGINT` result for larger date ranges.

   ```sql
   SELECT DATEDIFF_BIG(day, '2000-01-01', '9999-12-31') AS DaysDifference;
   ```

<br>

9. **SYSDATETIME()**: Returns the current date and time, including fractional seconds.

    ```sql
    SELECT SYSDATETIME() AS CurrentDateTime;
    ```

<br>

These are just a few examples of the time-related functions available in SQL. 

The specific functions and their behavior can vary depending on the SQL database system you're using, so be sure to refer to the documentation for your particular database for detailed information.
