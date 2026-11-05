# 🏢 ResidentOps – Apartment Governance & Operations Platform

ResidentOps is a web-based apartment management platform designed to simplify and digitalize apartment operations. It provides a centralized system for residents, committee administrators, vendors, and auditors to manage apartment activities efficiently.

## 📌 Project Overview

Managing an apartment involves several activities, such as maintenance requests, complaints, expenses, voting, notices, and vendor coordination. ResidentOps brings these activities together into one platform, improving transparency, communication, and accountability.

## ✨ Key Features

- **Dashboard:** Overview of apartment activities and important updates.
- **Maintenance Management:** Submit, track, and manage maintenance requests.
- **Complaint Management:** Register and resolve resident complaints.
- **Online Voting:** Create polls and conduct apartment voting with quorum support.
- **Expense Management:** Track and manage apartment expenses.
- **Notice Management:** Publish important announcements and updates.
- **Vendor Management:** Manage vendors and vendor-related concerns.
- **SLA-Based Escalation:** Automatically monitor maintenance deadlines and escalate overdue requests.
- **Audit Logging:** Maintain records of important system activities.
- **Role-Based Access:** Separate functionality for residents, administrators, vendors, and auditors.

## 🛠️ Technologies Used

| Component | Technology |
|---|---|
| Programming Language | Java 17 |
| Backend | Spring Boot 3.2 |
| Frontend | HTML5, CSS3, JavaScript |
| Database | MySQL |
| ORM | Hibernate / Spring Data JPA |
| Template Engine | Thymeleaf |
| Build Tool | Maven |
| IDE | IntelliJ IDEA |

## 🏗️ System Architecture

ResidentOps follows a modular, layered architecture.

1. **Frontend Layer:** Provides the user interface using HTML, CSS, JavaScript, and Thymeleaf.
2. **Controller Layer:** Handles HTTP requests and responses.
3. **Service Layer:** Implements application business logic.
4. **Repository Layer:** Communicates with the database using Spring Data JPA.
5. **Database Layer:** Stores users, maintenance requests, complaints, polls, votes, expenses, and other records.

## 👥 User Roles

| Role | Responsibilities |
|---|---|
| Resident | Submit requests, complaints, and participate in polls. |
| Committee Admin | Manage residents, maintenance, expenses, notices, and voting. |
| Vendor | Handle assigned maintenance work and vendor concerns. |
| Auditor | Review expenses and audit records. |

## 🧩 Design Patterns Used

The project demonstrates the following object-oriented design patterns:

- **Singleton Pattern:** Provides shared service instances.
- **Factory Method Pattern:** Creates maintenance request objects.
- **Observer Pattern:** Supports event-based notifications.
- **Strategy Pattern:** Supports different escalation strategies.

The project also demonstrates SOLID principles and GRASP design principles.

## 🗄️ Database

The application uses MySQL to store and manage apartment information.

Main database entities include:

- User
- MaintenanceRequest
- Complaint
- Poll
- Vote
- Expense
- VendorConcern
- FlatMember
- AuditLog
- FlatUpdateRequest
- PasswordResetRequest

Database initialization script:

`sql/schema_and_seed.sql`

## ⚙️ Installation and Setup

### Prerequisites

- Java JDK 17
- MySQL 8.x or compatible MariaDB
- IntelliJ IDEA
- XAMPP (optional, for local database management through phpMyAdmin)

### Step 1: Clone the Repository

```bash
git clone https://github.com/HimavarshiniReddy/ResidentOps.git
```

Open the project folder containing `pom.xml` in IntelliJ IDEA.

### Step 2: Configure the Database

1. Start MySQL from the XAMPP Control Panel.
2. Open phpMyAdmin at `http://localhost/phpmyadmin`.
3. Import the SQL file:

   `sql/schema_and_seed.sql`

4. The script creates and populates the `residentops` database.

### Step 3: Configure Database Connection

Open:

`src/main/resources/application.properties`

Configure your database credentials:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/residentops?createDatabaseIfNotExist=true&useSSL=false&allowPublicKeyRetrieval=true
spring.datasource.username=root
spring.datasource.password=
```

Replace the password with your actual MySQL password if required.

### Step 4: Load Maven Dependencies

Open `pom.xml` in IntelliJ IDEA and load or synchronize the Maven project.

### Step 5: Run the Application

Locate:

`src/main/java/com/residentops/ResidentOpsApplication.java`

Run the main application class.

Alternatively, use:

```bash
mvn spring-boot:run
```

### Step 6: Open the Application

Open your browser and visit:

**http://localhost:8080**

## 🔐 Demo Login Credentials

The following demo accounts are provided in the project:

| Role | Email | Password |
|---|---|---|
| Resident | arun@resident.com | pass123 |
| Admin | ravi@admin.com | pass123 |
| Vendor | ramesh@vendor.com | pass123 |
| Auditor | auditor@ops.com | pass123 |

These credentials are intended for local demonstration.

## ⏱️ SLA-Based Maintenance Escalation

ResidentOps uses priority-based Service Level Agreements (SLA) to monitor maintenance requests.

| Priority | Resolution Target |
|---|---|
| Critical | 2 Hours |
| High | 4 Hours |
| Medium | 24 Hours |
| Low | 48 Hours |

A scheduled task checks maintenance requests every five minutes and triggers escalation when deadlines are exceeded.

## 🎯 Project Objectives

- Digitalize apartment management operations.
- Improve communication between residents and administrators.
- Provide transparent expense and voting management.
- Track maintenance requests efficiently.
- Improve accountability through audit logging.
- Reduce delays through automated SLA escalation.

## 🚀 Future Enhancements

- Mobile application integration.
- Online payment gateway integration.
- Real-time chat and communication.
- Advanced analytics and reporting.
- Enhanced notification services.

## 👨‍💻 Project Information

**Project Name:** ResidentOps – Apartment Governance & Operations Platform

**Project Type:** Full-Stack Web Application

**Domain:** Apartment Management / Software Engineering

**Purpose:** Academic Project

