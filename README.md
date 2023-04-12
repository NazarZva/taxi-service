![img_1.png](img_1.png)
# Taxi-service
This project is an imitation of a taxi service. The following technologies are used here: Java Servlets, SQL.
# Features
* Add, delete and get all saved drivers
* Add, delete and get all saved car manufacturer
* Add, delete and get all saved car
* Login and logout to service
* Only logged in drivers can work with all service
* Add driver on start page
# Getting Started
* Clone repository with GitHub
* Run the SQL script that located in ```src/main/resources/init_db.sql``` to create the database
* Replace the values of the ```URL```, ```USERNAME```, ```PASSWORD``` and ```JDBC_DRIVER``` properties with the appropriate values for your database setup
* Build the project using Maven: ```mvn clean install```
* Deploy the generated WAR file to servlet container such as Tomcat
# Structure
* controller: Servlets that handle HTTP requests and responses
  - AddCarController - POST ```/cars/add``` - add a new car
  - AddDriverToCarController - POST ```/cars/drivers/add``` - add a driver to a certain car
  - DeleteCarController - GET ```/cars/delete``` - deletes car
  - GetAllCarsController - GET ```/cars``` - get all saved cars
  - GetMyCurrentCarsController - GET ```/cars/all/driver``` - get all cars for the current driver
  - AddDriverController - POST ```/drivers/add``` - add a driver
  - DeleteDriverController - GET ```/drivers/delete``` - deletes driver
  - GetAllDriversController - GET ```/drivers``` - get all saved drivers
  - AddManufacturerController - POST ```/manufacturers/add``` - add new manufacturer
  - DeleteManufacturerController - GET ```/manufacturers/delete``` - deletes manufacturer
  - GetAllManufacturersController - GET ```/manufacturers``` - get all saved manufacturers
  - LoginController - POST ```/login``` - authentication
  - LogoutController - GET ```/logout``` - invalidate current session
  - IndexController - GET ```/index``` - show all corresponding pages
* dao: Data Access Object interfaces and their implementations
* exception: My current exceptions for working with the database and authentication
* lib: Injector and him annotation to implement Dependency Injection 
* model: Contains classes that represent data models
* service: Service interfaces and their implementations that perform business logic
* util: Utility class used in a project to create a database connection
* filter: Servlet filters used to intercept requests and responses
* resources: Non-Java files such as database scripts
* webapp: Contains web resources such as CSS, JSP files and configuration file
* views: Contains JSP files used as views in the application for cars, drivers, manufacturers, authentication and include css files (that contains CSS files used in the application)
# Used technologies
* Java ```v.17.0.5```
* Maven ```v.3.8.7```
* JDBC ```v.4.2```
* MySql ```v.8.0.32```
* Java Servlets ```v.4.0.1```
* Tomcat ```v.9.0.50```
# Authors
Nazar Zvarych
