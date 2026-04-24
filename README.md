# Event-Registration-and-Management-System
# Student Event Management and Registration Portal

## Overview

This project is a web-based Student Event Management and Registration Portal developed using Spring Boot, Hibernate (JPA), Thymeleaf, MySQL, and Spring Security.

The system automates event registration, participant management, event administration, reporting, and real-time monitoring through a centralized platform.

It was developed as a minor project with emphasis on MVC architecture, database design, concurrency, socket-based communication, and Sustainable Development Goal (SDG) alignment.

---

## Objectives

- Automate student event registration
- Provide centralized event management
- Manage participants and registrations efficiently
- Support administrative event creation and monitoring
- Implement concurrency and real-time networking features
- Support measurable educational engagement aligned with SDG 4

---

## Features

### Student Features
- View upcoming events
- Register for events
- View registration confirmation
- Participate in live registration monitoring

### Admin Features
- Secure login using role-based access
- Add and manage events
- Manage seat availability
- View participant records
- Filter participants by event
- Export participant data to CSV
- Monitor live registrations
- Generate scheduled registration reports

---

## Advanced Features

### Multithreading
The project includes a scheduled reporting module using Spring Scheduler.

- Automatic periodic registration count generation
- Background thread execution using `@Scheduled`

### Socket-Based Real-Time Monitoring
The project includes WebSocket-based live registration alerts.

- Real-time participant registration feed
- STOMP messaging over WebSocket
- Live monitoring dashboard

---

## Technology Stack

### Backend
- Java
- Spring Boot
- Spring MVC
- Hibernate / JPA
- Spring Security

### Frontend
- Thymeleaf
- HTML
- CSS
- Bootstrap

### Database
- MySQL

### Networking / Concurrency
- Spring Scheduler
- WebSocket
- STOMP
- SockJS

---

## Project Architecture

The project follows layered MVC architecture:

User Interface (Thymeleaf Views)

↓  

Controllers

↓  

Service Layer

↓  

Repository Layer

↓  

MySQL Database

Additional modules:
- Security Layer
- Scheduler Module
- WebSocket Module

---

## Database Design

Normalized relational schema with foreign key constraints:

### Tables
1. participants  
2. events  
3. organizers  
4. registrations  
5. users

### Relationships
- One organizer can manage many events
- One event can have many registrations
- One participant can have many registrations

---

## Project Structure

```text
src/main/java/com/event

controller/
model/
repository/
service/
config/
scheduler/

src/main/resources/templates

index.html
register.html
success.html
participants.html
addEvent.html
monitor.html
```

---

## Key Modules

### Registration Module
Handles student registration requests and persists participant records.

### Event Management Module
Allows administrators to create and manage events dynamically.

### Participant Management Module
Supports participant filtering and export functionality.

### Security Module
Implements Admin and Student role access control.

### Concurrency and Networking Module
Implements scheduled reporting and live registration monitoring.

---

## Setup Instructions

### Prerequisites

Install:

- Java 17+
- Maven
- MySQL
- Eclipse / VS Code

---

## Database Setup

Create database:

```sql
CREATE DATABASE eventdb;
```

Import/create required tables.

Update database credentials in:

```properties
application.properties
```

Example:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/eventdb
spring.datasource.username=root
spring.datasource.password=yourpassword
```

---

## Run the Application

Using Maven:

```bash
mvn spring-boot:run
```

or run:

```text
NewEventRegistrationSystemApplication.java
```

as Spring Boot application.

Application runs on:

```text
http://localhost:8083
```

---

## Default Login Credentials

Admin:

```text
Username: admin
Password: admin123
```

Student:

```text
Username: student
Password: student123
```

---

## SDG Alignment

This project supports:

SDG 4 — Quality Education

Measured through:
- student participation metrics
- event engagement tracking
- seat utilization analysis

---

## Future Enhancements

- Email/SMS notifications
- QR attendance tracking
- Mobile application support
- Analytics dashboard
- Online payment integration

---

## Academic Note

AI-assisted coding support and open-source documentation were used for learning and debugging assistance. All code was reviewed, adapted, and understood before integration.

---

## Authors

Akshit Paunikar  
Madhura Patil
