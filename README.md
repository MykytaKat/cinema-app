# Cinema-app

REST web application for ticket reservation. It implements the main functions, such as:
1. displaying movies that are currently at the box office
2. shopping cart with the ability to add tickets to it and create an order based on the added tickets
3. searching for available movie sessions by date

### Detailed description of the functionality

- registration/login/logout
- view cinema halls, movies, available movie-sessions
- view/complete orders, buy tickets, view/update shopping cart as a user
- add cinema halls, movies, find user by email, add/update/delete/movie sessions as an admin

### Project structure 

- src/main/java - contains the entire source code of the program 
- src/main/resources - contains properties for connecting to the database

### Technologies used:
- Java 17
- Tomcat 9.0.75
- MySQL 8.0.22
- Maven 3.1.1
- Java Servlet 4.0.1
- JDBC
- Spring
- Spring-Web
- Spring-Security
- Hibernate

### Instructions for launching the project

1. Clone this project from GitHub
2. Install Apache Tomcat version 9.x.x. You can download it from the official Apache Tomcat website: https://tomcat.apache.org/download-90.cgi. Choose the appropriate installation package for your operating system. 
3. Install Postman for sending requests
4. Create an empty database using a local installation of MySQL.
5. Open the project in your preferred Integrated Development Environment. Locate the [db.properties](src/main/resources/db.properties) in the project. It should contain the database connection settings. Fill in the appropriate values for the following fields:
- JDBC driver
- url: The URL of your MySQL database. It should include the host, port, database name, and any additional parameters required for connection.
- username: The username for accessing your MySQL database.
- password: The password associated with the provided username.


![img.png](img.png)

6. Set up the configuration for tomcat

![img_1.png](img_1.png)

![img_2.png](img_2.png)

After these steps, you need to fix tomcat. You need to select the artifact to deploy 'taxi-service:war' and remove the Application context 'taxi_service_war' to leave only '/'

![img_4.png](img_4.png)

7. After starting Tomcat, you will be able to access your application by the URL