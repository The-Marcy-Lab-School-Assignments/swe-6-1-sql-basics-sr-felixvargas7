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

---

## Question 3

In one sentence, describe what this query does in plain English:

```sql
SELECT * FROM books WHERE genre = 'fiction' ORDER BY year DESC LIMIT 5;
```

Aim for something like: _"It returns the 5 most recently published fiction books."_

**Your answer:**

---

## Question 4

Why is it dangerous to run `DELETE FROM books` without a `WHERE` clause? What does it actually do?

**Your answer:**

---

## Question 5

What is the difference between `ORDER BY` and `LIMIT`? Could you use one without the other? Give an example to support your answer.

**Your answer:**
