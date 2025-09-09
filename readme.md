# 📈 E-Commerce Spring Boot Project

A **full-featured e-commerce web application** built with **Spring Boot**, **Hibernate**, and **MySQL/MariaDB**. Designed with a **layered architecture** (Controller, Service, DAO, Model) for **maintainability, scalability, and clarity**.

---

## 🌟 Key Features

* **Secure Authentication & Authorization** – Admin & Customer roles
* **Admin Tools** – Manage products, categories, customers
* **Customer Experience** – Shopping cart, product listings, checkout
* **Dynamic Listings** – Real-time updates from DB
* **Auto Database Setup** – Hibernate generates schema automatically
* **JSP Views** – Clean MVC-based UI

---

## 🛠️ Prerequisites

Make sure you have:

* **Java 17+**
* **Maven 3.8+**
* **MySQL/MariaDB Server**
* IDE: IntelliJ IDEA (recommended) or Eclipse

---

## 🔧 Installation & Setup

### 1. Clone the Repository

```bash
git clone <repository-url>
cd <project-folder>
```

### 2. Configure the Database

Create a database in MySQL/MariaDB:

```sql
CREATE DATABASE ecommjava;
```

Edit `src/main/resources/application.properties`:

```properties
db.url=jdbc:mysql://localhost:3306/ecommjava?createDatabaseIfNotExist=true
db.username=<your-username>
db.password=<your-password>
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

> **Tip:** Avoid using `root` for security.

### 3. (Optional) Load Sample Data

Run `basedata.sql` to preload users, categories, and products.

---

## 💡 Running the Application

### **IntelliJ IDEA**

1. Open as a Maven project.
2. Set working directory: `Run Configurations > JtSpringProjectApplication > $MODULE_WORKING_DIR$`
3. Run `JtSpringProjectApplication.java`

### **Eclipse**

1. Import as Maven Project.
2. Right-click `JtSpringProjectApplication.java` > **Run As > Java Application**

Access the app at: **[http://localhost:8080/](http://localhost:8080/)**

---

## 🔐 Default Credentials

**Admin**

```
Username: admin
Password: 123
```

**Customer**

```
Username: lisa
Password: 765
```

---

## 🗂️ Project Structure

```
src/main/java
 ├─ controller/   # Handles HTTP requests
 ├─ service/      # Business logic
 ├─ dao/          # Database access
 ├─ model/        # Entities (Hibernate)
src/main/webapp/views # JSP files
```

---

## 🔍 Endpoints

* `/` – Home
* `/register` – Registration
* `/admin/products` – Product Management
* `/admin/customers` – Customer Management
* `/admin/categories` – Category Management
* `/admin/dashboard` – Admin Dashboard

---

## 📊 Workflow

1. **Controller Layer** – Handles HTTP requests & maps to views
2. **Service Layer** – Core business logic
3. **DAO Layer** – Communicates with DB via Hibernate
4. **Model Layer** – Entity definitions
5. **View Layer** – JSP renders UI

---

## 🚨 Troubleshooting

**Issue:** `Could not resolve placeholder 'db.driver'`

* Update MySQL Connector version in `pom.xml`
* Reload Maven project

**Issue:** Views not found

* Ensure working directory is `$MODULE_WORKING_DIR$`

---

## 📄 Useful Links

* [Spring Boot Docs](https://spring.io/projects/spring-boot)
* [Maven Docs](https://maven.apache.org/)
* [Hibernate Docs](https://hibernate.org/)

---

## 🖼️ Screenshots

*(Add screenshots of UI here)*

---

**🚀 This guide covers setup, structure, and usage of the E-Commerce Spring Boot Project. Start coding, and happy building!**
