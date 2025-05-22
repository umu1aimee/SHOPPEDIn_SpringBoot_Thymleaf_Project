# E-commerce Web Application 
E-commerce Web Application
Project Overview
This project is a simple e-commerce web application developed as a mini-project for the Web Technology & Internet (INSY-413) course at the Adventist University of Central Africa. The application allows customers to browse products, add them to a shopping cart, proceed to checkout, and manage their accounts. Admins can add and manage products and update order statuses. The application uses Spring Boot for the backend and Thymeleaf for the frontend, with a database for persistent storage.
User Stories

Customer:
Browse products and view their details.
Add products to the shopping cart.
View the shopping cart and proceed to checkout.
Register/login to manage orders.


Admin:
Add new products and manage existing ones.
View and update order statuses.



Technologies Stack

Backend: Spring Boot, Spring Data JPA, Spring Security
Frontend: Thymeleaf, Spring MVC
Database: MySQL/PostgreSQL (configurable)
Build Tool: Maven/Gradle
Deployment: Cloud platform (e.g., AWS, Azure, or Heroku)
Version Control: Git (hosted on GitHub)

Setup Instructions
Prerequisites

Java 17 or higher
Maven or Gradle
MySQL/PostgreSQL database
IDE (e.g., IntelliJ IDEA, Eclipse)
Git
Cloud platform account (e.g., AWS, Azure, or Heroku) for deployment

Steps to Set Up and Run Locally

Clone the Repository:
git clone https://github.com/your-username/ecommerce-webapp.git
cd ecommerce-webapp


Configure the Database:

Install MySQL/PostgreSQL and create a database (e.g., ecommerce_db).
Update the application.properties file in src/main/resources with your database credentials:spring.datasource.url=jdbc:mysql://localhost:3306/ecommerce_db
spring.datasource.username=your_username
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update




Build the Project:

If using Maven:mvn clean install


If using Gradle:./gradlew build




Run the Application:

If using Maven:mvn spring-boot:run


If using Gradle:./gradlew bootRun


The application will be accessible at http://localhost:8080.


Access the Application:

Open a browser and navigate to http://localhost:8080.
Use the default admin credentials (if configured) or register a new user.



Deployment

Deploy to a Cloud Platform:

Configure the cloud platform (e.g., AWS, Azure, or Heroku).
For Heroku:
Install the Heroku CLI.
Run:heroku create
git push heroku main


Configure the database on the cloud platform and update application.properties accordingly.


Ensure environment variables for sensitive data (e.g., database credentials) are set on the cloud platform.


Access the Deployed Application:

The cloud platform will provide a URL (e.g., https://your-app-name.herokuapp.com).



Project Structure
ecommerce-webapp/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/example/ecommerce/
│   │   │       ├── controller/    # REST controllers and Thymeleaf controllers
│   │   │       ├── entity/        # JPA entities (Product, Order, User)
│   │   │       ├── repository/    # Spring Data JPA repositories
│   │   │       ├── service/       # Business logic
│   │   │       └── config/        # Spring Security and other configurations
│   │   ├── resources/
│   │   │   ├── templates/         # Thymeleaf templates
│   │   │   ├── static/            # CSS, JavaScript, and other static resources
│   │   │   └── application.properties  # Configuration file
├── pom.xml  # Maven configuration (or build.gradle for Gradle)
└── README.md

Features

Backend:

RESTful APIs for CRUD operations on products and orders.
User authentication and role-based authorization (USER, ADMIN) using Spring Security.
Database interaction using Spring Data JPA.
Server-side validation for user inputs.
Error handling with meaningful responses.


Frontend:

Product browsing and detailed views using Thymeleaf.
Shopping cart management (add/remove products).
User authentication forms (login/signup).
Checkout process with total calculation.
Admin dashboard for managing products and orders.
Responsive design with CSS and JavaScript.



Error Handling

Backend: Custom exceptions and global exception handling for meaningful error responses.
Frontend: Displays user-friendly error messages for invalid inputs or failed operations.

How to Contribute

Fork the repository.
Create a new branch (git checkout -b feature-branch).
Make changes and commit (git commit -m "Add feature").
Push to the branch (git push origin feature-branch).
Create a pull request.

GitHub Repository

The source code is hosted at: https://github.com/your-username/ecommerce-webapp
The repository is public, and the link has been shared on Google Classroom.

Notes

Ensure all dependencies are correctly configured in pom.xml or build.gradle.
Test the application thoroughly before deployment.
For any issues, refer to the logs in the console or check the cloud platform's logs.

