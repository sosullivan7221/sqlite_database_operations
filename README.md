# sqlite_database_operations
504 WK 3 Assignment creating SQL tables within python

## Datasets

Selected two datasets, one from Stony Brook Hospital and one from New York Presbyterian Hospital. These datasets contained pricing info for procedures, factoring in costs after insurance

## Analysis

The data was looked at first for shape, followed by a visual analysis of sample rows from the dataset. Dataset 1 had a number of null values, as not each code and encounter will have price changes for every insurance column listed. Dataset 2 did not have null values but instead had a text value saying 'not separately payable' if there was no monetary data in the cell. Value counts were then taken for the description of the encounter and the type of facility the service is performed in (Inpatient/Outpatient). Both datasets had a smaller number of inpatient procedures. Dataset 1 contained more variety and a larger number of unique descriptions when compared to Dataset 2

## SQL Lite Setup

1. Establish a connection using conn=sqlite3.connect(<database_name>) and c=conn.cursor()
2. Create a table using the CREATE TABLE statement, followed by the column names and the respective data types. Execute the command by placing it inside of c.execute(<sql_command>)
3. Use the INSERT INTO statement to insert values into the selected table, first naming each column and then the values that you wish to insert.
4. To automatically put a pandas data frame into SQL, use the command df.to_sql(<table_name>, <connection>, <if_exists_paramater>. This SQL can be read using pd.read_sql(<table_name>, <connection>)
