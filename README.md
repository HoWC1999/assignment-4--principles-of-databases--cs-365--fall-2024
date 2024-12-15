# Fall 2024 Principles of Databases — Assignment 4

* **Do not start this project until you’ve read and understood these instructions. If something is not clear, ask.**

---

## ❖ Introduction ❖

For this assignment, you will write responses to nine questions based on different topics from our textbook, *Database Systems — The Complete Book* and to one question based on your notes. Reply to each question in the provided region using Markdown syntax.

---

## ❖ Questions ❖

### 1. [2.4] What is the difference between a Cartesian Product, a Natural Join, and Theta-Joins?
#### Cartesian Product:
Combines every tuple of the first relation with every tuple of the second relation.
Result size is the product of the sizes of the two relations.

#### Natural Join:
Combines tuples from two relations based on all common attributes.
Automatically removes duplicate columns.

#### Theta-Joins:
Combines tuples based on a specific condition using comparison operators.
More flexible as it allows conditions beyond equality.

The three are different in terms of the number of tuples produced, the attributes used for joining, and the flexibility of the join condition.

### 2. [2.5] What is a Referential Integrity Constraint?

A referential integrity constraint ensures that a foreign key value in one table either matches a primary key value in another table or is null. It maintains consistent and valid links between related tables in a relational database.

###  3. [2.5] What is a Key Constraint?

A key constraint is a rule that ensures certain attributes (columns) in a table uniquely identify each tuple (row) within that table. It enforces the uniqueness and, in some cases, the non-nullability of these attributes.

### 4. [4.1] What is an Entity/Relationship Model? What purpose does it serve in the process of creating/designing databases?

An Entity/Relationship (ER) model is a conceptual data model that represents the entities, attributes, and relationships between entities in a database. 
It uses entities to represent real-world objects which are represented as rectangles, attributes to describe properties of entities which are represented as ovals, and relationships to define connections between entities which are represented as diamonds. 
The ER model serves as a blueprint for designing databases by providing a visual representation of the data structure and relationships, helping database designers understand the data requirements and constraints of the system.

### 5. [4.4] What is a Weak Entity Set?

A weak entity set is an entity set that is dependent on another (Strong) entity set for its existence. It does not have a primary key attribute of its own and relies on a partial key attribute from the identifying entity set.
Weak entity sets are essential for modeling scenarios where certain entities inherently depend on others for their identification and existence, ensuring accurate and meaningful data relationships within the database.

### 6. [5.2.7; 6.3.8] Explain the concepts of Outerjoin, Natural Right Outer Joins, Natural Left Outer Joins, and Full Outer Joins.

#### Outer Join:
A join operation that returns all records from one or both tables, along with matched records. Unmatched records are filled with NULLs.

#### Natural Left Outer Join:
Combines a natural join with a left outer join. It returns all records from the left table and the matched records from the right table based on all common attributes. Returns NULLs on the right side where no match exists.

#### Natural Right Outer Join:
Combines a natural join with a right outer join. It returns all records from the right table and the matched records from the left table based on all common attributes. Returns NULLs on the left side where no match exists.

#### Full Outer Join:
Returns all records when there is a match in either the left or right table. Unmatched rows from both tables are filled with NULLs. It combines the results of both the left and right outer joins.

### 7. [6.6.3] What is the difference between the SQL command `TRANSACTION` and the execution of any statement in SQL?

#### TRANSACTION Command:
Groups multiple SQL statements into a single unit of work. For example, a series of INSERT, UPDATE, and DELETE statements can be grouped into a transaction.
Ensures atomicity, consistency, isolation, and durability (ACID properties).
Commands: BEGIN TRANSACTION, COMMIT, ROLLBACK.

#### Execution of Individual SQL Statements:
Executed independently.
Typically operate in autocommit mode, where each statement is a separate transaction, which can therefore fail independently, violating ACID properties.
Lack the atomicity and rollback capabilities of transactions.

### 8. [8] What is a Virtual View and what are its advantages?

A virtual view is a stored query that presents data from one or more tables without storing the data itself. 
#### Advantages:
Simplifies complex queries.
Enhances security by restricting data access.
Provides a consistent, reusable interface for data retrieval.

### 9. [8.3] What is an *index* and what are its advantages?

An index is a data structure that enhances the speed of data retrieval operations on a database table. It functions similarly to an index in a book, allowing the database to locate data without scanning the entire table.

#### Advantages:
Improved Query Performance: Significantly reduces the time required to execute queries, especially those involving large tables.
Efficient Searching and Sorting: Enhances the performance of WHERE, ORDER BY, and JOIN clauses by enabling quick data access.
Uniqueness Enforcement: Supports unique constraints by ensuring that duplicate values cannot exist in indexed columns.
Reduced I/O Operations: Minimizes disk access by allowing the database to locate data more efficiently.
Enhanced Performance for Aggregate Functions: Speeds up operations like COUNT, MAX, and MIN by quickly accessing relevant data.

### 10. Explain the concept of an MVC, or model, view, controller, framework for designing full stack applications

MVC is an architectural pattern that separates an application into three interconnected components: Model, View, and Controller. This separation promotes organized code structure, scalability, and maintainability in full-stack applications.
#### Model:
Manages the data and business logic of the application. It handles data retrieval, storage, and manipulation. The model serves the purpose of interacting with the database and processing data.

#### View:
Represents the user interface of the application. It displays the data to the user and captures user input. The view is responsible for presenting the data in a user-friendly format and interacting with the user. The view serves the purpose of rendering the user interface, formatting data for display purposes, and updating the UI. 

#### Controller:
Acts as an intermediary between the model and the view. It processes user input, updates the model, and updates the view. The controller serves the purpose of handling user requests, updating the model based on user input, and updating the view based on model changes. 

### Overview:
In a fullstack environment, the MVC pattern is used to separate the frontend (client-side) and backend (server-side) components of an application. The model represents the data layer, the view represents the presentation layer, and the controller represents the application logic layer.
With the MVC pattern, the application's components are decoupled, allowing for easier maintenance, testing, and scalability. The model, view, and controller work together to create a modular, organized, and efficient full-stack application.
---

## ❖ Due ❖

Sunday, 15 December 2024, at 10:00 AM.

---

## ❖ Grading ❖

| Item        | Points |
|-------------|:------:|
| Question 1  | `10`   |
| Question 2  | `10`   |
| Question 3  | `10`   |
| Question 4  | `10`   |
| Question 5  | `10`   |
| Question 6  | `10`   |
| Question 7  | `10`   |
| Question 8  | `10`   |
| Question 9  | `10`   |
| Question 10 | `10`   |

---

## ❖ Submission ❖

**NO late submissions will be accepted.**

You will need to issue a pull request back into the original repo, the one from which your fork was created for this project. See the **Issuing Pull Requests** section of [this site](http://code-warrior.github.io/tutorials/git/github/index.html) for help on how to submit your assignment.

**Note**: This assignment may **only** be submitted via GitHub. **No other form of submission will be accepted**.
