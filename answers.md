# **Question 1**
- **Database:** -The actual collection of data stored in an organized manner
- **DBMS Software:** -The core software that manages the database. Provides tools for creating, updating, and querying data, as well as managing user access.
- **Query Processor:** Translates user queries written in high-level query languages (like SQL) into instructions that the database engine can execute. Ensures that queries are optimized for efficiency.
- **Database Engine:** The component responsible for data storage, retrieval, and updating.Handles transactions, maintains data consistency, and ensures data integrity.
- **Schema:** -The logical structure of the database that defines tables, relationships, views, and constraints.
Acts as a blueprint for organizing data.
- **Data Dictionary (Metadata):** -Stores information about the database structure, including details about tables, columns, data types, and constraints.Essential for query processing and ensuring consistency.
- **Transaction Manager:** -Ensures that database operations are completed successfully as part of a transaction. Provides features like atomicity, consistency, isolation, and durability (ACID properties).
- **Concurrency Control Manager:** -Manages simultaneous data access by multiple users. Prevents conflicts like data corruption or deadlocks.
- **Storage Manager:** -Handles data storage on physical devices like hard disks or SSDs.
Manages space allocation, data retrieval, and backup operations.
- **User Interface (UI):** -Provides tools or interfaces (e.g., command-line tools, GUIs) for users to interact with the database.Simplifies database access for administrators and end-users.

# **Question 2**
A **relational database** is a type of database that organizes data into tables (also called relations) consisting of rows (records) and columns (fields). The relationships between these tables are established using keys like primary keys and foreign keys, enabling efficient data retrieval and management. Relational databases use Structured Query Language (SQL) for querying and managing data.
### **Examples** 
- MySQL
- PostgreSQL
- Oracle Database
- Microsoft SQL Server

# **Question 3**
1. **Data Definition Language (DDL)** : Used to define and manage database structures like tables and schemas.
- **CREATE** (to create tables or databases)
- **ALTER** (to modify database structures)
- **DROP** (to delete tables or databases)
2. **Data Manipulation Language (DML)**: Used to manipulate and retrieve data in tables.
- **INSERT** (to add data)
- **UPDATE** (to modify existing data)
- **SELECT** (to query data)
3. **Data Control Language (DCL)**: Used to control access to data and manage permissions.
- **GRANT** (to provide access rights)
- **REVOKE** (to remove access rights)

# **Question 4**
- A **Primary Key** uniquely identifies records in a table, while a **Foreign Key** links tables by referencing a primary key.

# **Question 5**
- An **Entity-Relationship Diagram (ERD)** is a visual representation of the structure of a database that illustrates how entities (data objects) relate to each other. It is a key tool in database design, used to model the logical relationships between different data elements.

# **Question 6**
**Structured and Organized Data** -Stores data in tables, making it easy to organize and retrieve.
- **Data Integrity** -Enforces constraints like primary keys and foreign keys to maintain accuracy and consistency.
**Flexibility** -Supports complex queries and relationships, enabling scalability.
- **Data Security** -Offers robust access control and permissions to protect sensitive data.
- **Standardized Language** -Uses SQL, a widely adopted and standardized query language.
- **Data Redundancy Minimization** -Normalization reduces duplicate data, saving storage space.
- **Transaction Management** -Supports ACID properties (Atomicity, Consistency, Isolation, Durability) for reliable operations.

# **Question 7**
- **Integer (INT)** -Stores whole numbers.Example: 123.
- **Varchar/Text** -Stores variable-length strings.Example: "John Doe".
- **Date/Time**-Stores dates and times.Example: 2024-11-24, 12:30:00.
- **Decimal/Float** -Stores numbers with decimals.Example: 45.67.

# **Question 8**
The purpose of a **Database Management System (DBMS)** is to efficiently store, organize, retrieve, and manage data while ensuring security, consistency, and accuracy. It provides tools for data access, concurrent user management, and reliable backup and recovery.


