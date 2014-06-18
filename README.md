    
sql-practice
============

Create a new database called `sql_practice` and start with this schema:

`CREATE TABLE posts (
     id int auto_increment primary key, 
     title varchar(75), 
     body text
);`
    

References:
* MySQL field data types: http://www.tutorialspoint.com/mysql/mysql-data-types.htm
* MySQL `NOW()`: http://dev.mysql.com/doc/refman/5.1/en/date-and-time-functions.html#function_now
* Finding the difference between two dates in MySQL: http://dev.mysql.com/doc/refman/5.1/en/date-and-time-functions.html#function_datediff

Use a MySQL Client Query window to complete the following tasks:

1. Add a column to represent when this post was created
2. Add a column to represent what the current status is of the post (draft, publish, archive)
3. Add a column to represent the number of views this post has received
4. Add a column to represent the subtitle for this post
5. Insert a published post created yesterday with a title and body of your choosing
6. Insert a published post created last Tuesday with 100 views and a title/body of your choosing
7. Insert a post created today (now) that is a draft and a title/body of your choosing
8. Select all posts that are published
9. Select the post with id = 2
10. Select all posts that have more than 1 view
11. (Black Diamond) Select all posts that were made in the last two days
