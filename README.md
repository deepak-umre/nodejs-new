#CREATE DATABASE 

database script is as follows 

-- Create the database
CREATE DATABASE IF NOT EXISTS my_node_app_db;

-- Switch to the newly created database
USE my_node_app_db;

-- Create a table for user authentication
CREATE TABLE IF NOT EXISTS users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(50) NOT NULL,
    password VARCHAR(100) NOT NULL
);
---------------------------------------------------------------
copy all the files required in application directory
ex.
WORKDIR /APP
COPY . . 


--------------------------------------------------------------
craete dockerfile 
where you need to select nodejs image 
and install following dependencies 
npm init
npm install express 0
npm install body-parser 
npm install mariadb

--------------------------------------------------------------
expose application 
EXPOSE 3001
RUN node server.js 
---------------------------------------------------------------
* Build docker file * 
 docker build .
* Add tag to image
  docker image tag <image_id> my-app
* Run docker container
  docker run -d -P <image_id>
 -------------------------------------------------------------- 
*visit your application 
http://machine_ip:cootainer_port/login.html

--------------------------------------------------------------

