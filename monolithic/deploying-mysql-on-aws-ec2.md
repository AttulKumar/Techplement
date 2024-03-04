Commands used to host MySql Server on AWS EC2 Instance

( IMAGES OF EACH STEP IS ADDED IN THE FOLDER )
Step 0: Create a instace named "ec2-eg"  

Step 1: Update the system and install MySql
sudo apt update
sudo apt install mysql-server

Step 2: Check the Status of MySql (Active or Inactive)
sudo systemctl status mysql

Step 3: Login to MySql as a root
sudo mysql

Step 4: Update the password for the MySql Server
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'place-your-password-here';
FLUSH PRIVILEGES;

Step 5: Test the MySql server if it is working by running sample sql queries
CREATE DATABASE mysql_test;

USE mysql_test;

CREATE TABLE table1 (id INT, name VARCHAR(45));

INSERT INTO table1 VALUES(1, 'Rohan'), (2, 'Ramit'), (3, 'Prakhar'), (4, 'Aaryan');

SELECT * FROM table1;
