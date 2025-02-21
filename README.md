# 🏦 Banking System Project

A **Java-based** banking application that enables **account management**, **secure transactions**, and **financial data security** using **MySQL and JDBC**.

---

## 🚀 Features

👉 **Bank Management System**
- Accessible to **bank employees** with authorized credentials.
- Create, update, and manage **customer accounts**.
- Process transactions (**withdrawals, deposits**).
- **Close accounts** and generate daily statistics.
- Update **ATM PIN** via KYC with email verification.

👉 **ATM System**
- Perform **cash deposits and withdrawals**.
- **Check account balance** and print mini statements.
- Secure **ATM PIN updates** via email authentication.

---

## 🛠️ Tech Stack

- **Java (Swing & JDBC)** – GUI & backend logic.
- **MySQL** – Database management.
- **MySQL Workbench** – Database design & administration.
- **JDBC (Java Database Connectivity)** – MySQL integration.

---

## 📌 Database Schema

The **Banking System Database** consists of multiple relational tables for managing customers, transactions, accounts, and card details.

### **Tables Overview**

📝 **CustomerDetails**
- Stores personal information including **name, DOB, email, address**.
- Primary Key: **mobile_number**.

📝 **PersonalDetails**
- Additional details such as **religion, income, education, PAN, Aadhar**.
- Foreign Key: **mobile_number** (links to CustomerDetails).

📝 **Account**
- Stores **account type, number, associated card, PIN, and services**.
- Primary Key: **accountNumber**.

📝 **Transaction**
- Logs all **deposit and withdrawal transactions**.
- Foreign Key: **mobileNumber** (links to CustomerDetails).

📝 **Card**
- Stores **card number and PIN for ATM transactions**.
- Primary Key: **cardNumber**.

📝 **Balance**
- Tracks **current account balance**.
- Primary Key: **accountNumber**.

---

## 🏢 Security & Authentication

- Bank employees access the system using **secure login credentials**.
- ATM PIN updates require **email verification**.
- Transactions are **logged securely** to prevent fraud.

---

## 🛠️ Installation & Setup

### 1️⃣ **Clone the Repository**
```sh
git clone https://github.com/MitulRanpariya/Bank-Atm_Management.git
cd Bank-Atm_Management
```

### 2️⃣ **Configure Database**
Update `application.properties` with **MySQL credentials**:
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/banking_system
spring.datasource.username=root
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=update
```

### 3️⃣ **Run the Application**
```sh
mvn clean install
mvn spring-boot:run
```
🚀 **Application runs at** `http://localhost:8080/`

---

## 📚 Project Usage

- **Bank employees** manage accounts and transactions.
- **Customers** use the ATM system for deposits, withdrawals, and balance inquiries.
- **Security protocols** ensure safe financial operations.

---

## 📝 Contributing

Contributions are welcome! Feel free to **fork**, create a **pull request**, or open an **issue**.

---


