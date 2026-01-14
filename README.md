# Contacts Project (Part 1)

This project is a REST API for managing contacts, built with Node.js, Express, and MongoDB. It follows the MVC architecture pattern.

## 🚀 Deployment

**Render Link**: https://cse341-project-b06h.onrender.com

## 🛠 Prerequisites

- Node.js
- MongoDB Atlas Account
- VS Code 
- REST Client Extension 

## 📦 Installation & Setup

1.  **Clone the repository**.
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

## 🧪 Week 2: Testing Guide

You can test the new CRUD operations using **Swagger UI** or the **REST Client**.

### Option 1: Swagger UI (Easiest)
1.  **Start the server**: `npm start`
2.  Open your browser to: [http://localhost:8080/api-docs](http://localhost:8080/api-docs)
3.  **Create a Contact**:
    - Click **POST /contacts**.
    - Click **Try it out**.
    - Edit the JSON body (change the name/email).
    - Click **Execute**.
    - Copy the `insertedId` from the Response body.
4.  **Update a Contact**:
    - Click **PUT /contacts/{id}**.
    - Click **Try it out**.
    - Paste the ID you just copied.
    - Edit the JSON body.
    - Click **Execute**. (Expect 204 No Content)
5.  **Delete a Contact**:
    - Click **DELETE /contacts/{id}**.
    - Click **Try it out**.
    - Paste the ID.
    - Click **Execute**. (Expect 204 No Content)

### Option 2: VS Code REST Client
1.  Open `routes.rest` in VS Code.
2.  Click the small "Send Request" text above each URL.
3.  For Create/Update, make sure to change the JSON data if you want to see differences.
    - **Note**: For PUT and DELETE, you must replace the hardcoded ID in `routes.rest` with a real ID from your database.

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
