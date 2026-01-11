# Contacts Project (Part 1)

This project is a REST API for managing contacts, built with Node.js, Express, and MongoDB. It follows the MVC architecture pattern.

## 🚀 Deployment

**Render Link**: (Add your Render URL here after deployment)

## 🛠 Prerequisites

- Node.js
- MongoDB Atlas Account
- VS Code (Recommended)
- REST Client Extension (Recommended)

## 📦 Installation & Setup

1.  **Clone the repository** (if not already done).
2.  **Install dependencies**:
    ```bash
    npm install
    ```
3.  **Configure Environment**:
    Create a `.env` file in the root directory and add your MongoDB connection string (NOT on GitHub):
    ```
    MONGODB_URI=mongodb+srv://<username>:<password>@<cluster>.mongodb.net/project1
    ```
    *Note: The project uses the `project1` database and `contacts` collection.*
4.  **Run the Server**:
    ```bash
    npm start
    ```

## 🔗 API Endpoints

### 1. Home
- **GET /**
- Returns: "Hello World" (Verifies server is running)

### 2. Get All Contacts
- **GET /contacts**
- Returns: Array of all contacts in the database.

### 3. Get Single Contact
- **GET /contacts/:id**
- Returns: A single contact object matching the ID.

## 📹 Video Submission Guide

For your submission video, make sure to demonstrate the following to score full points on the rubric:

1.  **Show Deployment**:
    - Open your browser to your **Render URL** (e.g., `https://cse341-project.onrender.com/`).
    - Show that it loads "Hello World".
2.  **Show API Endpoints (on Render)**:
    - Change URL to `/contacts` (e.g., `https://cse341-project.onrender.com/contacts`).
    - Show that it returns your list of contacts (JSON).
    - Copy one ID from the list.
    - Change URL to `/contacts/<ID>` and show it returns that single contact.
3.  **Show Security**:
    - Show your `.env` file in VS Code (briefly showing the variable exists).
    - Show your `.gitignore` file to prove `.env` and `node_modules` are ignored.
    - Briefly show your GitHub repository to prove the `.env` file is **not** there.

## 📁 Architecture
- `server.js`: Main entry point.
- `routes/`: Defines API routes.
- `controllers/`: Contains the logic for handling requests.
- `db/`: Handles database connection.
