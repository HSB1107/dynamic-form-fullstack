# Dynamic Form

A functional full-stack web application designed for creating, sharing, and collecting data through dynamic forms. This project focuses on the core lifecycle of form management: creation, persistence, and response collection.

## 🎯 Project Goal
The primary objective is to provide a seamless flow where a user can build a form, save it to a database, and share a link with others. The system ensures that multiple respondents can submit their data and that these responses are reliably persisted for the form creator.

---

## 🚀 Core Features (Initial Phase)
* **Form Builder:** An interactive interface to create forms with various question types (Short Answer, MCQ, etc.).
* **Form Persistence:** Save form structures to the database for future access or editing.
* **Public Sharing:** Generate unique, shareable links for each form.
* **Response Collection:** Enable multiple users to fill out forms via the shared link.
* **Data Storage:** All submitted responses are stored and linked back to the original form.

---

## 💻 Tech Stack
* **Frontend:** React (Vite) + TypeScript
* **Styling:** Tailwind CSS
* **Backend:** Java 17 + Spring Boot
* **Relational Database:** PostgreSQL (for User and Form Metadata)
* **Document Database:** MongoDB (for Dynamic Form Schemas and Responses)

---

## 🏗️ Initial Data Strategy
To handle the dynamic nature of forms, this project uses a **Polyglot Persistence** approach:
1.  **PostgreSQL:** Handles structured data like `Users` and `FormMetadata` (Title, Creator, Timestamps).
2.  **MongoDB:** Handles flexible data like `FormStructure` (the list of questions) and `Submissions` (the actual answers), allowing for varying question types without complex SQL migrations.

---

## 🛠️ Getting Started

### Prerequisites
* JDK 17 or higher
* Node.js & npm
* PostgreSQL & MongoDB (Local or Docker)

### Backend Setup
1. Navigate to the `backend` directory.
2. Update `src/main/resources/application.properties` with your database credentials.
3. Run the application:
   ```bash
   ./mvnw spring-boot:run
