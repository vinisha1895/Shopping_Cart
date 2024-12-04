# Spring Boot Shopping Cart Web App

## About

This is a demo project for practicing Spring + Thymeleaf. The idea was to build some basic shopping cart web app.

It was made using **Spring Boot**, **Spring Security**, **Thymeleaf**, **Spring Data JPA**, **Spring Data REST**. 
Database is in memory **H2**.

There is a login and registration functionality included.
Users can shop for products. Each user has his own shopping cart (session functionality).
Checkout is transactional.

## Configuration

### Configuration Files
Folder **src/resources/** contains config files for **shopping-cart** Spring Boot application.
* **src/resources/application.properties** - main configuration file. Here it is possible to change admin username/password,
as well as change the server port number.

## How to run
There are several ways to run the application. You can run it from the command line with java and Maven  
Once the app starts, go to the web browser and visit `http://localhost:8070/home`

Admin username: **admin**
Admin password: **admin**
User username: **user**
User password: **password**

#### Using Executable Jar

Build the JAR file with Maven
```bash
$ mvn clean package 
``` 

Then you can run the JAR file:
```bash
$ java -jar target/shopping-cart-0.0.1-SNAPSHOT.jar
```

### Maven

Open a terminal and run the following commands to ensure that you have valid versions of Java and Maven installed:

```bash
# java -version
java version "1.8.0_202"
Java(TM) SE Runtime Environment (build 1.8.0_202-b08)
Java HotSpot(TM) 64-Bit Server VM (build 25.202-b08, mixed mode)
```

```bash
# mvn --version
Apache Maven 3.9.9 (8e8579a9e76f7d015ee5ec7bfcdc97d260186937)
Maven home: /opt/tools/maven
Java version: 1.8.0_202, vendor: Oracle Corporation, runtime: /opt/tools/jdk1.8.0_202/jre
Default locale: en_US, platform encoding: UTF-8
OS name: "linux", version: "5.10.228-219.884.amzn2.x86_64", arch: "amd64", family: "unix"
```

#### Using the Maven Plugin

The Spring Boot Maven plugin includes a run goal that can be used to quickly compile and run your application. 
Applications run in an exploded form, as they do in your IDE. 
The following example shows a typical Maven command to run a Spring Boot application:
 
```bash
$ mvn spring-boot:run
``` 
To exit the application, press **ctrl-c**.

## Tests

Tests can be run by executing following command from the root of the project:

```bash
$ mvn test
```

## Helper Tools

### HAL REST Browser
Go to the web browser and visit `http://localhost:8070/`
You will need to be authenticated to be able to see this page.

### H2 Database web interface
Go to the web browser and visit `http://localhost:8070/h2-console`
```
jdbc:h2:mem:shopping_cart_db
```

In `/src/main/resources/application.properties` file it is possible to change both
web interface url path, as well as the datasource url.


