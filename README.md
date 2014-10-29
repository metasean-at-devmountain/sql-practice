    
sql-practice
============

Create a new database called `sql_practice` and start with this schema:

```
CREATE TABLE posts (
     id int auto_increment primary key, 
     title varchar(75), 
     body text
);
```
    

References:
* MySQL field data types: http://www.tutorialspoint.com/mysql/mysql-data-types.htm
* MySQL `NOW()`: http://dev.mysql.com/doc/refman/5.1/en/date-and-time-functions.html#function_now
* Finding the difference between two dates in MySQL: http://dev.mysql.com/doc/refman/5.1/en/date-and-time-functions.html#function_datediff

Use a MySQL Client Query window to complete the following tasks:

1. Add a column to represent when this post was created
	ALTER TABLE posts ADD createdAt DATE;
2. Add a column to represent what the current status is of the post (draft, publish, archive)
	ALTER TABLE posts ADD status VARCHAR(10);
3. Add a column to represent the number of views this post has received
	ALTER TABLE posts ADD views FLOAT;
4. Add a column to represent the subtitle for this post
	ALTER TABLE posts ADD subtitle VARCHAR(50);
5. Insert a published post created yesterday with a title and body of your choosing
	INSERT INTO posts (title, body, createdAt, status) VALUES ("Hello world", "Welcome to SQL", '2014-10-27', 'published');
6. Insert a published post created last Tuesday with 100 views and a title/body of your choosing
	INSERT INTO posts (title, body, createdAt, status, views) VALUES ("Hello galaxy", "See Sean rock SQL", 'published', '2014-10-21', 100);
7. Insert a post created today (now) that is a draft and a title/body of your choosing
	INSERT INTO posts (title, body, createdAt, status) VALUES ("Now", "seize the now!", NOW(), 'draft');
8. Select all posts that are published
	SELECT * from posts WHERE status='published';
9. Select the post with id = 2
	SELECT * from posts WHERE id='2';
10. Select all posts that have more than 1 view
	SELECT * from posts WHERE views>1;
11. (Black Diamond) Select all posts that were made in the last two days
	SELECT * from posts WHERE createdAt>DATE_SUB(NOW(), INTERVAL 2 DAY);
