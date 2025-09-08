# E-Commerce Spring Boot Project

This project is a complete e-commerce web application built using Spring Boot, Hibernate, and MySQL/MariaDB. It follows a layered architecture, with clear separation between the controller, service, DAO, and model layers, ensuring maintainability and scalability.

---

## Features

* User authentication and authorization (Admin and Customer roles)
* Product, Category, and Customer management (Admin)
* Shopping cart functionality (Customer)
* Dynamic product listings
* Database auto-creation and schema generation via Hibernate
* JSP-based views served by Spring MVC

---

## Prerequisites

Before you begin, ensure you have the following installed:

* **Java 17** or later
* **Maven 3.8+**
* **MySQL** or **MariaDB** server
* **IntelliJ IDEA** (recommended) or **Eclipse**

---

## Installation and Setup

### 1. Clone the Repository

```bash
git clone <repository-url>
cd <project-folder>
```

### 2. Configure the Database

1. Create a database in MySQL/MariaDB:

   ```sql
   CREATE DATABASE ecommjava;
   ```
2. Open `src/main/resources/application.properties` and set:

   ```properties
   db.url=jdbc:mysql://localhost:3306/ecommjava?createDatabaseIfNotExist=true
   db.username=<your-username>
   db.password=<your-password>
   spring.jpa.hibernate.ddl-auto=update
   spring.jpa.show-sql=true
   ```

   **Tip:** Avoid using `root` as the username for security reasons.

### 3. (Optional) Load Base Data

Run the `basedata.sql` script on your database to preload sample users, categories, and products.

---

## Running the Application

### IntelliJ IDEA

1. Open the project as a **Maven project**.
2. Ensure the working directory is set so that JSP views are correctly located:

   * Go to **Run Configurations** > Select `JtSpringProjectApplication` > Set **Working Directory** to `$MODULE_WORKING_DIR$`.
3. Run the `main` method in `JtSpringProjectApplication.java`.

### Eclipse

1. Import the project as a **Maven Project**.
2. Right-click `JtSpringProjectApplication.java` and choose **Run As > Java Application**.

Once started, access the app at:

```
http://localhost:8080/
```

---

## Default Credentials

If you imported the base data:

* **Admin**

  * Username: `admin`
  * Password: `123`
* **Customer**

  * Username: `lisa`
  * Password: `765`

---

## Project Structure

```
src/main/java
 ├─ controller/       # Handles HTTP requests and routes to views
 ├─ service/          # Contains reusable business logic
 ├─ dao/              # Data Access Objects interacting with the database
 ├─ model/            # Entity classes representing database tables
src/main/webapp/views # JSP view files
```

---

## Endpoints

* `/` – Home page
* `/register` – User registration
* `/admin/products` – Admin product management
* `/admin/customers` – Admin customer management
* `/admin/categories` – Admin category management
* `/admin/dashboard` – Admin dashboard

---

## Workflow

1. **Controller Layer** – Handles HTTP requests and returns `ModelAndView` objects.
2. **Service Layer** – Encapsulates business logic for reusability.
3. **DAO Layer** – Directly communicates with the database via Hibernate.
4. **Model Layer** – Defines entities and their relationships.
5. **View Layer** – JSP pages render data for the client.

---

## Troubleshooting

* **`Could not resolve placeholder 'db.driver'`**

  * Update the MySQL Connector dependency in `pom.xml` to match your MySQL version.
  * Reload the Maven project.
* **Views not found**

  * Ensure your working directory is set to `$MODULE_WORKING_DIR$` in your IDE.

---

## Useful Links

* [Spring Boot Documentation](https://spring.io/projects/spring-boot)
* [Maven Documentation](https://maven.apache.org/guides/index.html)
* [Hibernate Documentation](https://hibernate.org/orm/documentation/)

---

## Screenshots

> *Add your project screenshots here to showcase the UI.*

---

This completes the setup and usage guide for the E-Commerce Spring Boot Project.
