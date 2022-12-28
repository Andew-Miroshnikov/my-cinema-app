# <h1><img src="https://cdn-icons-png.flaticon.com/512/1067/1067089.png" width="100"/>Cinema app</h1>
:clapper: **Cinema-app** is a simple web-application that supports <em>registration</em>, <em>authentication</em> and other <em>CRUD</em> operations. Application compile with <i>REST</i> architecture style, <i>SOLID</i> and other ***OOP*** principles. Application supports Role access for endpoints, <i>JSON</i> content-type.

:dart: Features
---
|Operation|Endpoint `http://localhost:8080`...|Role|
|---------|--------|----|
|Register new user|POST: `/register`|anonymous|
|Get list of movies, cinema halls <p>Get movie session by movie</p>|GET:`/cinema-halls`, `/movies` <p>GET:`/movie-sessions/available`</p>|USER, ADMIN|
|Get user|GET: `/users/by-email`|ADMIN|
|Add new cinema hall, movies,<p>movie-session</p>|POST: `/cinema-halls`, `/movies`,<p>POST: `/movie-sessions`</p>|ADMIN|
|Update movie session|PUT: `/movie-sessions/{id}`|ADMIN|
|Delete movie session|DELETE: `/movie-sessions/{id}`|ADMIN|
|Get list of orders, shopping-carts|GET: `/orders`, `/shopping-carts/by-user`|USER|
|Add order|POST: `/orders/complete`|USER|
|Update shopping-cart|PUT: `/shopping-carts/movie-sessions`|USER|

## :pancakes: Structure
----
|<img src="https://spaces-cdn.clipsafari.com/cehwijh0e7m9jv1r9g7hrgz5u70i" alt="comp" width="30"/>|
|----------|
|<div align="center">:arrow_double_down::arrow_double_up:</div>|
|<div align="center">Filter</div><div align="center">Controller</div>|
|<div align="center">:arrow_down::arrow_up:</div>|
|<div align="center">Service</div>|
|<div align="center">:arrow_down::arrow_up:</div>|
|<div align="center">Dao</div>|
|<div align="center">:arrow_double_down::arrow_double_up:</div>|
|<div align="center"><img src="https://spaces-cdn.clipsafari.com/bsu2nc68wv4cpli10l62sotq9ma4" alt="database" width="30"/></div>|

## :key: Entity relations in DB
---
<img src="https://user-images.githubusercontent.com/112484426/209444011-ccf39ec5-4c01-45a6-b5b6-d1f6407a7b16.png" alt="drawing" width="400"/>

## :electron: Technologies
---
+ ![JDK](https://img.shields.io/badge/JDK-11-red)
+ ![maven](https://img.shields.io/badge/Maven-4.0.0-blue)
+ ![mysql](https://img.shields.io/badge/Mysql-8.0.22-lightgrey)
+ ![servlet](https://img.shields.io/badge/ServletAPI-4.0.1-brightgreen)
+ ![spring](https://img.shields.io/badge/Spring-5.2.2.RELEASE-green)
+ ![hibernate](https://img.shields.io/badge/Hibernate-5.4.27.Final-red)
+ ![Tomcat](https://img.shields.io/badge/Tomcat-9.0.69-green)

## :rocket: Run the app
---
+ [ ] Clone the project from the GitHub
+ [ ] Create schema in [MySql](https://dev.mysql.com/downloads/installer/) database. ```CREATE SCHEMA IF NOT EXISTS `cinema-app` DEFAULT CHARACTER SET utf8;```
+ [ ] Configure [**src/main/resources/db.properties**](https://github.com/Andew-Miroshnikov/my-cinema-app/blob/main/src/main/resources/db.properties)
    + [ ] write your **db.username**
    + [ ] write your **db.password**
    + :warning: if u use not [MySql](https://dev.mysql.com/downloads/installer/) database, don't forgot to change dependency in **pom.xml**
      ```java
      <dependencies>
        <dependency>
            <groupId>mysql</groupId>
            <artifactId>mysql-connector-java</artifactId>
            <version>8.0.22</version>
        </dependency>
        ```
    + [ ] write your **db.url**
        + :eyes: pay attention for this part `?serverTimezone=UTC`
    + [ ] write your **db.driver**
        + :warning: if you have problems with this part, you can easily find it in internet, just write "***YOUR DATABASE NAME*** *driver class name*"
+ [ ] Configure [Tomcat](https://tomcat.apache.org/download-90.cgi) local server
    + :warning: not recommended to use tomcat 10 version , because you can need extra settings
+ [ ] Download [Postman](https://www.postman.com) desktop version and write your data in query :octocat:
+ [X] Admin username: admin@i.ua, password: admin123
+ 