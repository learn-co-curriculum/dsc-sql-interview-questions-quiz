
# SQL Interview Questions  - Quiz

## Introduction

In this lesson, we'll go through a short quiz containing the types of questions about SQL and relational databases that you can expect to see in an interview. 



## SQL Interview Questions

This quiz contains questions on topics you can expect to see in an interview pertaining to SQL and Relational Databases. Some of them are multiple choice, while some are short answer. For these short answer questions, double click on the Jupyter Notebook and type your answer below the line. 

## Question 1

what are the 4 main datatypes in SQLite3? Can we use other common types from other kinds of SQL?

Type your answer below this line:
_______________________________________________________________________________________________________________________________

* INTEGER: These are signed integer values. Up to 8 bytes can be used to store the integer value, depending on how large it is. 

* REAL: The SQLite equivalent of a Float value like we would see in python, REAL values are used to store decimal numbers.

* TEXT:  The SQLite equivalent of a string. Typically uses encodings such as `UTF-8`. 

* BLOB: Exactly as it sounds, a 'blob' of data that is stored exactly as it was input. For instance, if we stored an image in a SQLite database, it would be stored as a BLOB, and would not be touched or changed in any way. 



## Question 2

Explain the relationship between **Primary Keys** and **Foreign Keys**.

Type your answer below this line:
_______________________________________________________________________________________________________________________________

Primary keys are the unique keys assigned to every record in a table. A Foreign key is a column in a table that points to primary key of an record in a different table that an item has a relationship with. JOIN statements work by matching up rows where the foreign key in one table matches the primary key for a row (or rows) in a different table. 


## Question 3

Explain the different types of relationships entities can have in a SQL database. 

Type your answer below this line:
_______________________________________________________________________________________________________________________________

The different types of relationships entities can have in SQL databases are one-to-one, one-to-many, and many-to-many. One-to-one is self-explanatory--each record in the table is linked to one, and only one, record in a different corresponding table. An example of a one-to-many relationship would be a `Class` table and a `Student` table that we could use to store a class roster. Since one class can have many students, this would be a one-to-many relationship, that would created by giving the `Student` records a foreign key column that would reference the primary key of the class they are enrolled in. 

Many-to-Many relationships are more complex, because we can have an arbitrary number of records on either side of the relationship. 




## Question 4

Explain the various types of JOINs possible with SQL. 

Type your answer below this line:
_______________________________________________________________________________________________________________________________

The main JOIN types are Inner, Outer, and Left/Right. We can also do a full JOIN to create a Cartesian Product, but this isn't that useful and isn't often used. 

The easiest way to think about JOINs is to picture a Venn Diagram, with each circle representing a different table. The area where the circles overlap represents the rows where the Primary Keys from one table match the Foreign Keys from another. 

An INNER JOIN returns only the overlapping portion of the Venn Diagram, where the record's key matches a key in the other table. 

An OUTER JOIN returns only the rows from each table where there is no corresponding match in with the other table. 

A LEFT JOIN returns every record in the left table, and any rows from the right table that happen to have a key that matches with the left table. A Right table is the same thing, but flipped, returning every row in the right table and only the matches from the left. 

## Question 5

Explain the relationship between Aggregate functions and GROUP BY statements.

Type your answer below this line:
_______________________________________________________________________________________________________________________________

Aggregate functions are used to compute things like a COUNT or a MEAN. These functions perform these calculations on a 'group' that we must specify. For instance, assume we have a table containing the population for each country in the world, for each year in the last 20 years. If we wanted to get the mean of the population column, this could mean two different things. Without a GROUP BY statement, the SQL server would not know if we meant the mean population of a country across all 20 years, or the mean population of all countries for each given year. Both are mean values, and one is not more correct than the other, so the SQL server would throw an error because of the ambiguity. To make this work, we would need to specify whether we wanted the mean when the data is grouped by country (which would return the mean population over the 20 year span) or grouped by year (which would return the mean population of the average country for each of the separate years). 

## Question 6

What role do Associative Entities play (JOIN Tables) in many-to-many JOINs?


Type your answer below this line:
_______________________________________________________________________________________________________________________________

Associative Entities, also called JOIN Tables, are a type of table used to allow us to perform many-to-many JOINs. These tables act as a list that keep track of each of the different connections between an entity in one table and all of that entity's connections in another table. While we can JOIN tables directly for one-to-one and one-to-many relationships, we must use an Associative Entity in order to pull of a JOIN between two tables with a many-to-many relationship. 

## Summary

In this lesson, we practiced answering open-ended interview questions for SQL and Relational Databases. 
