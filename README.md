# 📚 Digital Library 

A **Spring Boot–based RESTful API** that simulates a Digital Library System — allowing users to sign up, browse available books, rent them, and return them.

This project demonstrates **end-to-end backend development** using **Java**, **Spring Boot**, **MySQL**, **Redis caching**, and **Swagger API documentation**.

---

## 🚀 Features

- 🧑‍💻 User Registration and Login  
- 📖 View all available books  
- 📦 Rent and Return books  
- ⚡ Redis Caching for faster book retrieval  
- 📘 Swagger UI for easy API exploration  
- 💾 MySQL database integration using Spring Data JPA  

---

## ⚙️ Prerequisites

Before running this project, ensure you have the following installed:

- **Java 17+**  
- **Maven 3.9+**  
- **MySQL Server**  
- **Redis 5.0.14 for Windows**  
- **Any IDE** of your choice (IntelliJ IDEA / Eclipse)

---

## 🧾 Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/<your-username>/DigitalLibrary.git
cd DigitalLibrary
```

---

### 2. Configure the Database

Make sure your MySQL server is running locally.  
The default configuration in `application.properties` expects:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/digital_library
spring.datasource.username=root
spring.datasource.password=yourpassword
```

If your MySQL credentials differ, update them accordingly.  
Then, create the database:

```sql
CREATE DATABASE digital_library;
```

---

### 3. Start Redis Server

Make sure Redis v5.0.14 is running locally before you start the application.  

To start Redis (on Windows):

```bash
redis-server.exe
```

---

### 4. Build and Run the Application

You can run the application in the following way:

#### 👉 Using your IDE:

1. Open the project in **IntelliJ** or **Eclipse**.  
2. Run the main class:  
   ```
   src/main/java/com/digitallibrary/DigitalLibraryApplication.java
   ```

---

## 🌐 Exploring the APIs via Swagger UI

This project includes **Swagger UI** for interactive API testing.

Once the application is running, open your browser and go to:  
👉 [http://localhost:8080/swagger-ui/index.html](http://localhost:8080/swagger-ui/index.html)

You will see all available API endpoints grouped by controller:

- `/api/v1/users` – for user registration & authentication  
- `/api/v1/books` – for viewing and managing books  
- `/api/v1/borrow` – for renting and returning books  

Each endpoint includes:
- Description  
- Required parameters  
- Example request & response  
- “Try it out” button for live testing  

---

![Swagger UI Screenshot](https://github.com/user-attachments/assets/42a0348f-6c7a-4092-98a6-afe072ec69df)

---

## 🧠 Key Learnings and Highlights

- Implemented **caching using Redis** to reduce book query response time.  
- Applied **Spring Boot layered architecture** (Controller → Service → Repository).  
- Used **Spring Data JPA** for ORM and MySQL integration.  
- Integrated **Swagger** for live API documentation.  
- Demonstrates a **real-world backend workflow** — from user registration to resource management.  

---

## 🛠️ Tech Stack

| Category | Technology |
|-----------|-------------|
| Language | Java 17 |
| Framework | Spring Boot |
| Database | MySQL |
| Caching | Redis |
| Documentation | Swagger |
| Build Tool | Maven |

---

## 💡 Future Improvements

- Add JWT-based authentication  
- Implement pagination and search for books  
- Introduce roles (Admin, User) for better access control  
- Add Docker setup for containerized deployment  
