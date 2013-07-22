# Exercises 


In order to learn SQL, we'll go through some simple exercises to start

1. Given the following statement:

  ``` sql
  CREATE TABLE `users` (
    `id` int(11) unsigned NOT NULL AUTO_INCREMENT,
    `email` varchar(255) NOT NULL,
    `password` varchar(32) NOT NULL,
    PRIMARY KEY (`id`)
  );
  ```
  * What does the `AUTO_INCREMENT` flag do?
  - each time a new entry is added without the 'id' field specified it will increment the number by 1 for the id field of the new entry

  * What does `int(11)` mean?
  - specifies that the format of the entry is a whole number that goes from 0 to 99999999999

  * What is `users` in this statement?
  - users is the name of the database table within the database that contains the column names 'id', 'email', 'password' and the primary key is 'id'

2. Explain the concept of a primary key.
  - a primary key is a unique value assigned to a column in a table that uniquely identifies each row

3. Explain the concept of a foreign key.
  - a foreign key is a field in one database table that uniquely identifies a row in another table

## Queries

All the following questions deal with the attached SQL database. Make sure you follow the directions in the Google Doc on how to import the database.

1. Get a list of all the usernames from the users table.
SELECT `email` FROM `users` (no `usernames` field so using `email`)

2. Get the name of all users who have placed orders for an iPhone
SELECT users.email 
FROM users, products
WHERE users.id = products.id AND products.name = "iPhone"

3. Get a list of all the users (id's are fine) who have placed orders over 300$. _N.B._ The cost in the products table is in cents, not dollars.
SELECT id
FROM products
WHERE cost > 30000