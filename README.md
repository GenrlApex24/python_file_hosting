# Python local file hosting system

## A python based file hosting system that lets you store html/php files then serve them using python

# !!! Not fully working yet

### Database<br>
- I would recommend using a <a href="http://mysql.com/">MySql</a> database as that is what i have been using
How to create/Structure<br>
- Make sure you have a running installation of your chosen database
- Create a database with the relevant command for your sql database service
- Then create a table using the command bellow (may not work with other sql database types)

CREATE TABLE websites (
id INT AUTO_INCREMENT PRIMARY KEY,
name varchar(64) NOT NULL UNIQUE,
description varchar(255),
file LONGBLOB NOT NULL,
file_type ENUM('html', 'php') NOT NULL
)

Once your database has been created and your table is set up you will need to put the relevant database credentials into the db_config dictionary at the top of the connect_db.py file
