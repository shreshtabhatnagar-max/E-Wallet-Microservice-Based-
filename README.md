# 💳 E-Wallet Backend System

A backend system for a digital **E-Wallet platform** built using **Spring Boot**.  
The system is designed to handle wallet management, transactions, notifications, and secure user operations using modern backend technologies.

This project demonstrates a **scalable backend architecture** using messaging systems, caching, and secure APIs.

---

# 🚀 Features

- User Wallet Management
- Secure API endpoints
- Transaction processing
- Asynchronous event processing using Kafka
- Email notifications for transactions
- Redis caching for performance optimization
- Database persistence using JPA & MySQL
- Secure authentication using Spring Security

---

# 🏗 System Architecture

The application follows a **layered backend architecture**:
Client
|
REST API (Spring MVC Controllers)
|
Service Layer (Business Logic)
|
Repository Layer (Spring Data JPA)
|
MySQL Database
<img width="1321" height="799" alt="Screenshot 2026-03-10 084009" src="https://github.com/user-attachments/assets/4c912b1d-bebb-4f9a-bd22-d9910a75ecaf" />


Additional supporting components:Kafka → Event Driven Communication
Redis → Caching Layer
SMTP → Email Notifications
Spring Security → Authentication & Authorization



---

# 🛠 Tech Stack

| Technology | Purpose |
|------------|--------|
| Java 17 | Programming Language |
| Spring Boot | Backend Framework |
| Spring MVC | REST API Development |
| Spring Data JPA | Database ORM |
| MySQL | Relational Database |
| Apache Kafka | Event Streaming |
| Redis | Caching |
| Spring Security | Authentication & Authorization |
| Lombok | Reducing Boilerplate Code |
| Maven | Build Tool |

---

# 📁 Project Structure


E-Wallet
│
├── src/main/java/com/example/E_wallet
│ └── EWalletApplication.java
│
├── src/main/resources
│ ├── application.properties
│
├── pom.xml


Typical scalable structure (recommended):


controller
service
repository
entity
dto
config
security
kafka
util


---

# ⚙️ Setup & Installation

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/yourusername/e-wallet.git
cd e-wallet
2️⃣ Configure Database

Update application.properties

spring.datasource.url=jdbc:mysql://localhost:3306/ewallet
spring.datasource.username=root
spring.datasource.password=yourpassword

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
3️⃣ Configure Redis
spring.redis.host=localhost
spring.redis.port=6379
4️⃣ Configure Kafka
spring.kafka.bootstrap-servers=localhost:9092
5️⃣ Run the Application

Using Maven:

mvn spring-boot:run

Or run the main class:

EWalletApplication.java
🔐 Security

The project uses Spring Security to secure REST APIs.

Security features include:

Authentication

Authorization

Secure API endpoints

Protection against unauthorized access

📩 Event Driven Features

Kafka is used for:

Transaction events

Notification processing

Asynchronous operations

Example flow:

User Transaction
     |
Publish Event
     |
Kafka Topic
     |
Notification Service
     |
Email Sent
⚡ Caching

Redis is used to improve system performance by caching:

Wallet balances

Frequently accessed data

Session information

📬 Email Notifications

Spring Mail is used to send notifications such as:

Transaction confirmation

Wallet updates

Alerts
<img width="1145" height="788" alt="Screenshot 2026-03-10 085647" src="https://github.com/user-attachments/assets/8964be4e-1815-43ed-91a0-84fee81c9b2d" />

🧪 Testing

Testing dependencies included for:

JPA

Redis

Kafka

Security

Web Layer

📈 Future Improvements

Add JWT Authentication

Implement Microservices architecture

Add API Gateway

Add Docker support

Implement Payment Gateway integration

Add Swagger API documentation

👨‍💻 Author

Shrestha Bhatnagar
GitHub
https://github.com/shreshtabhatnagar-max/E-Wallet-Microservice-Based-
