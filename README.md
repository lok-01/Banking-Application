# Banking-Application
Banking Transaction Management System built using Spring Boot and MySQL, implementing RESTful APIs for account creation, deposits, withdrawals, and transactional data handling with layered architecture.

##  Features

- Create bank accounts
- Deposit money
- Withdraw money
- Transfer funds between accounts
- View transaction history
- Balance inquiry
- Proper validation for insufficient funds
- Global exception handling
- Layered architecture (Controller → Service → Repository)

---

##  Tech Stack

- Java
- Spring Boot
- Spring Data JPA (Hibernate)
- MySQL
- REST APIs
- Postman (API Testing)
- Git

---

##  Project Structure


com.bankapp
├── controller
├── service
├── repository
├── model
├── exception
└── BankingApplication.java


---

## 🗄 Database Schema

### Users Table
- id (Primary Key)
- name
- email

### Accounts Table
- id (Primary Key)
- accountNumber
- balance
- userId (Foreign Key)

### Transactions Table
- id (Primary Key)
- amount
- type (DEPOSIT / WITHDRAW / TRANSFER)
- timestamp
- accountId (Foreign Key)

---

## 🔗 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | /api/users | Create user |
| POST | /api/accounts | Create account |
| POST | /api/accounts/{id}/deposit | Deposit money |
| POST | /api/accounts/{id}/withdraw | Withdraw money |
| POST | /api/accounts/transfer | Transfer funds |
| GET  | /api/accounts/{id}/transactions | Get transaction history |

---

##  How to Run

1. Clone the repository:

git clone https://github.com/lok-01/banking-transaction-system.git


2. Configure MySQL database in `application.properties`

3. Run the application:

mvn spring-boot:run


4. Use Postman to test the APIs.

---

##  Key Engineering Concepts Applied

- RESTful API Design
- Layered Architecture
- Transaction Management
- Business Rule Validation
- Exception Handling
- Database Integration using JPA
- Clean Code Practices

---

## Future Enhancements

- Add authentication (Spring Security)
- Implement JWT-based login
- Add React frontend dashboard
- Dockerize the application
