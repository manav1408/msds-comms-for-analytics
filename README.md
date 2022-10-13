# Database Keys 

The objective of this presentation is to understand the challenges one can come across if we do not effectively apply database keys to tables , and what would be some pressing need to not apply certain type of keys to tables in real world scenarios.
We then proceed to discuss database technologies that donot enforce a defined schema or use of certain type of keys ,i.e the No SQL databases and briefly go over a document based no SQL database storage model.


# Summary

- Primary Key:  Any column in a table that can be used to uniquely identify each and every row in a table. Must be non nullable and unique
- Unique Key: Any column that can be used to uniquely identify each row in a table but can be nullable
- Foreign Key: A column in one table, that refers to the primary column in another table. It is used prevent actions that would destroy links between two                  tables


# What if There are no Keys in Database

- Primary Key: If we dont include primary keys in a table, data duplication can occur.
  From a business stand point, it can cause the following issues:-
  - Lack of personalization for customers
  - Wastage of marketing budget 
  - Missing out on potential good customers

- Foreign Key
  - Potential data integrity problems
  - Difficulty with querying and reporting from the database for people who don't have knowledge of the database
  - Full Table Reload: Some databases, like data warehouses, staging, or interfacing databases, often require reloading data from external sources. This                          causes the data to be inconsistent at the time of reloading.


# Can and Do Relational Databases exist without keys - Real World Scenarios

Yes, databases can exist without keys. 
But if we create tables without primary keys, data duplication will occur. Creating tables without primary keys is a big No!

But tables without applying a foreign key constraint do exist.
  - Whenever we apply a foreign key constraint, the insert operation becomes expensive.
  - While integrating an external table with manual entries, it is possible that the potential foreign key column might have erroneous entries. If we apply     a foreign key constraint, we might end losing all the data in the rows without erroneous data in one column.


# Are there databases that actually don't need keys?

By definition , no SQL databases move away from the traditional structured schemas and have flexibility in terms of how information is organized in the storage. They also do not employ the concept of foreign keys and referential integrity.
One such no SQL database is a document based data base model ,where data is stored in terms of key value pairs.
In this case , a key returns a JSON based document in which a larger entity and it’s associated entities are modeled as sub sections in a JSON structure. This helps to maintain relation between different entity objects with a single structure and eliminates the need to separately maintain the relations in a defined schema or usage of foreign keys.
