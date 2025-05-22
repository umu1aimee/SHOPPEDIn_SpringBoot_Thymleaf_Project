# E-commerce Web Application

## Project Description
This project is a Mini Project for the Web Technology & Internet (INSY-413) course at the Faculty of Information Technology, Adventist University of Central Africa, Kigali, Rwanda. It is a simple e-commerce web application developed using Spring Boot for the backend and Thymeleaf for the frontend, adhering to the course requirements. The application supports two primary user roles—customers and admins—enabling distinct functionalities for each.

The backend leverages Spring Boot, Spring Data JPA, and Spring Security to handle business logic, database interactions, and role-based access control. The frontend, built with Thymeleaf and Spring MVC, provides a responsive user interface styled with Bootstrap. The application uses MySQL or PostgreSQL as the database and Maven as the build tool.

## Functionalities
### Customer Features
- **Product Browsing**: Displays a list of products with details retrieved via RESTful APIs
- **Shopping Cart Management**: Allows adding/removing products to/from a cart, viewing the cart, and calculating totals
- **Checkout and Payment**: Supports a checkout process with a payment interface (simulated or integrated via a payment gateway API)
- **Order Tracking**: Enables viewing order history and tracking order status (e.g., "Pending," "Shipped," "Delivered")
- **User Authentication**: Provides registration and login functionality to manage orders and user data

### Admin Features
- **Product Management**: Facilitates adding, updating, and deleting products through a dedicated admin panel
- **User Management**: Allows viewing a list of all registered users
- **Order Management**: Supports viewing all orders and updating their statuses

## Technical Implementation
### Backend (Spring Boot) 
- Implements role-based access control (USER, ADMIN) using Spring Security
- Provides CRUD APIs for product management with a `Product` entity and corresponding repository
- Manages orders through APIs for placing orders, viewing history, and updating statuses, using an `Order` entity with relationships to users and products
- Integrates payment processing (simulated or via API)
- Designs RESTful APIs with appropriate HTTP methods (GET, POST, PUT, DELETE) and JSON responses
- Applies server-side validation using Spring validations

### Frontend (Thymeleaf) 
- Features UI components for product browsing, cart management, order tracking, payment processing, and authentication
- Uses Bootstrap for responsive styling
- Integrates with backend APIs to fetch data, authenticate users, manage orders, process payments, and display order progress
- Includes login/signup forms linked with Spring Security
- Manages static resources (CSS, JavaScript) for enhanced interactivity
  ###Access the Application:

Open a browser and navigate to http://localhost:8080.
Use the default admin credentials (if configured) or register a new user.



### Additional Requirements
- Incorporates error handling mechanisms for backend and frontend
- Displays user-friendly error messages
- Deploys the application on a cloud platform (e.g., AWS, Azure, or Heroku)
- Hosts source code and documentation publicly on GitHub
- Submits the GitHub repository link via Google Classroom

## Submission Details
- **Due Date**: 18 May 2025
- **Course**: Web Technology & Internet (INSY-413)
- **Faculty**: Faculty of Information Technology, Adventist University of Central Africa
- **GitHub Repository**: To be shared publicly and submitted via Google Classroom at: https://classroom.google.com/c/Nze3NTAxMTguNhMw?zic=oso5ymdx

## Technologies Stack
- **Backend**: Spring Boot, Spring Data JPA, Spring Security
- **Frontend**: Thymeleaf, Spring MVC
- **Styling**: Bootstrap
- **Database**: MySQL or PostgreSQL
- **Build Tool**: Maven

## Prerequisites
- Java 17 or later
- Maven
- MySQL or PostgreSQL
- Git
- An IDE (e.g., IntelliJ IDEA, Eclipse) (optional)

## Setup Instructions
1. **Create a Spring Boot Project**:
   - Use Spring Initializr with Maven
   - Add dependencies: Spring Web, Spring Data JPA, Spring Security, Thymeleaf, and a database driver (e.g., MySQL)
2. **Configure Database**:
   - Set up a MySQL/PostgreSQL database named `ecommerce_db`
   - Update `src/main/resources/application.properties`:
   spring.datasource.url=jdbc:mysql://localhost:3306/ecommerce_db

   3. **Use Spring Data JPA**:
- Define entities: `Product`, `Order`, `User`
- Create repositories extending `JpaRepository`
4. **Implement Spring Security**:
- Define USER and ADMIN roles
- Configure access restrictions and authentication endpoints

## Steps to Run Locally
1. **Clone the Repository**:
git clone https://github.com/<your-username>/e-commerce-web-app.git</your-username>
3. **Configure Database**:
- Ensure MySQL/PostgreSQL is running
- Update `application.properties` with credentials
4. **Build the Project**:
mvn clean install
5. **Run the Application**:
mvn spring-boot:run
Alternatively, run via an IDE by executing the main class (e.g., `EcommerceApplication.java`)
6. **Access the Application**:
- Navigate to `http://localhost:8080`
- Register/login as a customer or admin to explore features

## Project Structure
- `src/main/java/`: Contains Java code (controllers, services, entities, repositories)
- `src/main/resources/`: Includes configuration files (`application.properties`) and Thymeleaf templates (`templates/`)
- `src/main/resources/static/`: Stores static resources (CSS, JavaScript)
- `pom.xml`: Maven configuration for dependencies and build settings
- `target/`: Generated after building (compiled classes and JAR file)
