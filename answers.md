# **Question 1**
- **Database:** -The actual collection of data stored in an organized manner
- **DBMS Software:** -The core software that manages the database. Provides tools for creating, updating, and querying data, as well as managing user access.
- **Query Processor:** Translates user queries written in high-level query languages (like SQL) into instructions that the database engine can execute. Ensures that queries are optimized for efficiency.
- **Database Engine:** The component responsible for data storage, retrieval, and updating.Handles transactions, maintains data consistency, and ensures data integrity.
- **Schema:** -The logical structure of the database that defines tables, relationships, views, and constraints.
Acts as a blueprint for organizing data.
- **Data Dictionary (Metadata):** -Stores information about the database structure, including details about tables, columns, data types, and constraints.Essential for query processing and ensuring consistency.
- **Transaction Manager:** -Ensures that database operations are completed successfully as part of a transaction. Provides features like atomicity, consistency, isolation, and durability (ACID properties).
  1. **Atomicity**:Ensures that a transaction is "all or nothing" — either all operations within a transaction are completed successfully, or none are applied to the database.<br>
   **Practical Implementation:**<br>
   **Commit and Rollback Mechanisms:**
If all operations in a transaction succeed, the Transaction Manager performs a commit, permanently applying changes to the database.<br>
If any operation fails, the Transaction Manager performs a rollback, reverting the database to its previous state.<br>
    **Example:**<br>
  A bank transfer where $100 is debited from Account A and credited to Account B:<br>
If the debit operation succeeds but the credit fails, the transaction is rolled back, ensuring no partial updates.
  2. **Consistency**:Ensures that the database transitions from one valid state to another, maintaining all defined rules, constraints, and relationships.<br>
**Practical Implementation:**<br>
**Integrity Constraints:**<br>
Enforces rules like foreign keys, unique constraints, and triggers to maintain data validity.<br>
**Pre- and Post-Transaction Validation:**<br>
The Transaction Manager checks database constraints before committing a transaction.<br>
**Example:**<br>
In an e-commerce system, if an order references a non-existent product ID, the Transaction Manager will abort the transaction, maintaining referential integrity.<br>
  3. **Isolation**:Ensures that transactions operate independently, without interference, even when executed concurrently.<br>
**Practical Implementation:**<br>
**Locking Mechanisms:**<br>
Uses locks (e.g., row-level, table-level) to prevent conflicts between concurrent transactions.<br>
**Isolation Levels:**
Provides different levels of isolation, such as:<br>
**Read Uncommitted:** Allows transactions to see uncommitted changes (least isolation).<br>
**Read Committed:** Ensures that a transaction only sees committed data.
Repeatable Read: Prevents changes to data read by a transaction until it completes.<br>
**Serializable:** Ensures complete isolation, simulating sequential transaction execution.<br>
**Example:**<br>
Two transactions updating the same product inventory:<br>
 - One transaction locks the row until its operation completes, preventing the other from making simultaneous changes.
  4. **Durability** Ensures that once a transaction is committed, its changes are permanent, even in the event of a system failure.<br>
**Practical Implementation:**<br>
**Write-Ahead Logging (WAL):**<br>
The Transaction Manager writes transaction details to a log before applying them to the database. This log is used to recover committed transactions after a crash.<br>
**Backup and Recovery Mechanisms:**<br>
Periodic backups ensure data is retrievable in case of a hardware failure.<br>
**Example:**<br>
If a power outage occurs after a transaction commits, the Transaction Manager uses the log to reapply the changes during recovery.

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
- **Data Redundancy Minimization** -Normalization reduces duplicate data, saving storage space.<br>
**How Normalization Reduces Redundancy**<br>
1. **Eliminating Duplicate Data:**

By breaking data into smaller tables and removing repeated groups of data.<br>
**Example:** Instead of storing a customer’s details repeatedly in an Orders table, a separate Customers table is created to store customer information, referenced by a unique ID in the Orders table.
2. **Preventing Data Anomalies:**
Reduces insertion anomalies (e.g., requiring duplicate data to insert a new record).<br>
Prevents update anomalies (e.g., needing to update the same data in multiple locations).<br>
Avoids deletion anomalies (e.g., losing important data when deleting a related record).<br>
3. **Promoting Efficient Data Storage:**
By storing each piece of data only once in its relevant table, normalization reduces the overall storage requirements.<br>
**Example:** Storing product details like name and price in a Products table, instead of duplicating them in each order record.<br>
**How Normalization Maintains Data Integrity**<br>
- **Establishing Relationships with Primary and Foreign Keys:**<br>
**Primary Keys:** Ensure each record in a table is unique.<br>
**Foreign Keys:** Link related tables, enforcing referential integrity (e.g., orders referencing customers).<br>
- **Enforcing Constraints:**<br>
Constraints like UNIQUE, NOT NULL, and CHECK ensure consistent and valid data across tables.<br>
- **Preserving Dependencies:**
By organizing tables based on functional dependencies (e.g., in 3rd Normal Form, attributes depend only on the primary key), normalization ensures accurate data representation.<br>

- **Transaction Management** -Supports ACID properties (Atomicity, Consistency, Isolation, Durability) for reliable operations.<br>
 ## **Practical Example**
In an e-commerce database:<br>

**Before normalization:**<br>
Orders table includes repeated customer details for each order.<br>
**After normalization:**<br>
Separate Customers and Orders tables: Customers table stores unique customer data (e.g., ID, name, address).<br>
Orders table references customer data via a foreign key (CustomerID), reducing redundancy while ensuring integrity.

# **Question 7**
- **Integer (INT)** -Stores whole numbers.Example: 123.
- **Varchar/Text** -Stores variable-length strings.Example: "John Doe".
- **Date/Time**-Stores dates and times.Example: 2024-11-24, 12:30:00.
- **Decimal/Float** -Stores numbers with decimals.Example: 45.67.

# **Question 8**
The purpose of a **Database Management System (DBMS)** is to efficiently store, organize, retrieve, and manage data while ensuring security, consistency, and accuracy. It provides tools for data access, concurrent user management, and reliable backup and recovery.


