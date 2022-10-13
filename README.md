# Database Keys 

# Summary

- Primary Key:  Any column in a table that can be used to uniquely identify each and every row in a table. Must be non nullable and unique
- Unique Key: Any column that can be used to uniquely identify each row in a table but can be nullable
- Foreign Key is a field (or collection of fields) in one table,  that refers to the primary  column in another table. It is used prevent actions that      would destroy links between two tables


# What if There are no Keys in Database

- Primary Key: If we dont include primary keys in a table, data duplication can occur.
  From a business stand point, it can cause the following issues:-
  - Lack of personalization for customers
  - Wastage of marketing budget 
  - Missing out on potential good customers

- Foreign Key
  - Potential data integrity problems: The obvious problem with the lack of foreign keys is that a database can't enforce referential integrity and if it                                          wasn't taken care of properly at the higher level then this might lead to inconsistent data
  - Difficulty with querying and reporting from the database for people who don't have knowledge of the database
  - Full Table Reload: Some databases, like data warehouses, staging, or interfacing databases, often require reloading data from external sources. This                          causes the data to be inconsistent at the time of reloading. That could be bypassed by disabling keys for the time of the reload.                          However, this introduces additional logic and complexity and another point of failure.

# Can and Do Relational Databases exist without keys - Real World Scenarios

Yes, databases can exist without keys. 
But if we create tables without primary keys, data duplication will occur. Creating tables without primary keys is a big No!

But tables without applying a foreign key constraint do exist.
  - Whenever we apply a foreign key constraint, the insert operation becomes expensive.
  - While integrating an external table with manual entries, it is possible that the potential foreign key column might have erroneous entries. If we apply     a foreign key constraint, we might end losing all the data in the rows without erroneous data in one column.

# Are there databases that actually don't need keys?

