# Short Response: SQL Basics

Answer each question below. Write in complete sentences (3–5 per answer).

---

## Question 1

What is a database? Why do we use one instead of storing data in a JavaScript array on your server?

**Your answer:**
A **database** is any collection of data, structured in an organized manner. Databases allow for **persistent** data structures, meaning that data is written in disk or hard drive storage, rather than the random access memory (RAM). Since we are able to use hard drive/disk instead of RAM, any modifications made to the data remain, whereas using RAM, which is where data like a JavaScript array lives, will result in data resets when the server is reset. This means that by using a database, our servers can be shut down for updates, crash, and restart without disrupting any data.

## Question 2

What is a primary key? Why does every table need one?

**Your answer:**
When utilizing tables, data is stored within rows and columns. Rows represent a single record in a table, and columns represent an attribute of that record. A **primary key** refers to a unique identifier present for a row in a table, typically being named after its table. Primary keys are necessary for uniquely identifying a specific record. Another use case for primary keys is for allowing multiple tables to form a relationship. This use case for primary keys means that when referenced in other tables, they are referred to as **foreign keys**.

## Question 3

In one sentence, describe what this query does in plain English:

```sql
SELECT * FROM books WHERE genre = 'fiction' ORDER BY year DESC LIMIT 5;
```

Aim for something like: _"It returns the 5 most recently published fiction books."_

**Your answer:**
It returns the books in the table where the genre of the book matches 'fiction', ordered by descending order, limited to 5 books total returned.

## Question 4

Why is it dangerous to run `DELETE FROM books` without a `WHERE` clause? What does it actually do?

**Your answer:**
It is dangerous to run `DELETE FROM books` without a `WHERE` clause, because this command will end up deleting _all_ books in the table, when we would've wanted to delete specific books. Deleting all books is irreversible without a backup, making it another dangerous command. Using the `WHERE` clause allows us to create a condition that limits which books get deleted.

## Question 5

What is the difference between `ORDER BY` and `LIMIT`? Could you use one without the other? Give an example to support your answer.

**Your answer:**
The difference between `ORDER BY` and `LIMIT`, is that `ORDER BY` sorts results from one or more columns in a table, while `LIMIT` restricts the number of rows returned. The main difference lies in their use cases; `ORDER BY` is for organization, `LIMIT` caps the number of rows returned from a query. It is possible to use one without the other, as both serve different purposes. This can be showcased as:

```sql
-- Orders books from newest to oldest
SELECT * FROM books ORDER BY year DESC;

-- Shows first 5 books
SELECT * FROM books LIMIT 5;

-- Combining both (order books from newest to oldest and returns first 5 books )
SELECT * FROM books ORDER BY year DESC LIMIT 5;
```
