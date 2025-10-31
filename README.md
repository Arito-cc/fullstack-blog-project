# Full-Stack MERN Blog Project 🚀

This is a complete full-stack blog application built with the MERN stack (MongoDB, Express, React, Node.js). It was created as a minor project for a full-stack development class.

The application features a secure RESTful API backend that handles user authentication with JWT and manages blog post data. The frontend is a modern, responsive Single Page Application (SPA) built with React and Vite, allowing users to register, log in, and perform full CRUD (Create, Read, Update, Delete) operations on their own posts.

---

## 🌐 Live Links & Test Credentials

You can test the fully deployed application right now!

* **Live Frontend:** **[https://frontend-blog-project.onrender.com/](https://frontend-blog-project.onrender.com/)**
* **Live Backend API:** [https://backend-blog-project-5lv7.onrender.com/](https://backend-blog-project-5lv7.onrender.com/)

### 🧪 Try it out!

Feel free to register as a new user or use these test credentials to log in:

* **Email:** `test1@example.com`
* **Password:** `password123`

---

## ✨ Key Features

* **Secure User Authentication**: Full registration and login system.
* **Password Hashing**: Passwords are never stored in plain text, using `bcrypt.js` for one-way hashing.
* **JWT Authorization**: The API is secured using JSON Web Tokens. Protected routes require a valid token.
* **Full CRUD for Posts**:
    * **Create**: Logged-in users can create new blog posts.
    * **Read**: All users (guests included) can read all posts.
    * **Update**: Users can **only** edit their own posts.
    * **Delete**: Users can **only** delete their own posts.
* **Author-Only Permissions**: The backend validates that the user making an edit/delete request is the original author.
* **Responsive Frontend**: The React UI, built with Tailwind CSS, is fully responsive.
* **Global State Management**: Uses React's Context API to manage the user's authentication state.

---

## 🛠️ Tech Stack

| Category | Technology | Description |
| :--- | :--- | :--- |
| **Frontend** | React (Vite) | JavaScript library for building user interfaces. |
| | React Router | For client-side routing and page navigation. |
| | Tailwind CSS | A utility-first CSS framework for styling. |
| | Axios | For making HTTP requests to the backend API. |
| | React Context | For managing global authentication state. |
| **Backend** | Node.js | JavaScript runtime environment. |
| | Express.js | Web framework for building the RESTful API. |
| | MongoDB | NoSQL database for storing user and post data. |
| | Mongoose | ODM library for modeling data in MongoDB. |
| | JWT (jsonwebtoken) | For creating and verifying user auth tokens. |
| | bcrypt.js | For hashing and comparing passwords. |
| **Deployment** | Render | Cloud platform for deploying the backend & frontend. |

---

## 🏁 Getting Started (Local Development)

To get a local copy up and running, follow these steps.

### Prerequisites

* [Node.js](https://nodejs.org/) (which includes npm)
* A [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) account (or a local MongoDB instance)
* [Postman](https://www.postman.com/) (Recommended for testing the API)

### 1. Backend Setup (`/server` folder)

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
    cd your-repo-name/server
    ```

2.  **Install dependencies:**
    ```bash
    npm install
    ```

3.  **Create your environment file:**
    Create a file named `.env` in the `/server` directory and add the following variables:

    ```.env
    # Your MongoDB connection string
    MONGO_URI=mongodb+srv://<user>:<password>@cluster0.qzhqs2d.mongodb.net/?appName=Cluster0

    # A strong, random secret for signing tokens
    JWT_SECRET=your_super_strong_secret_key_here

    # Port for the server to run on
    PORT=5000
    ```

4.  **Run the server:**
    ```bash
    # Runs the server with nodemon (auto-restarts on changes)
    npm run dev
    ```
    The backend API will now be running on `http://localhost:5000`.

### 2. Frontend Setup (`/client` folder)

1.  **Open a new terminal** and navigate to the client directory:
    ```bash
    cd ../client
    ```

2.  **Install dependencies:**
    ```bash
    npm install
    ```
3.  **Set API URL:**
    Go to `client/src/api/api.js` and change the `baseURL` to your local backend:
    `baseURL: 'http://localhost:5000/api',`

4.  **Run the client:**
    ```bash
    # Starts the Vite development server
    npm run dev
    ```
    Your React app will open in your browser, typically at `http://localhost:5173`.

---

## 📖 API Endpoints

All endpoints are prefixed with `/api`.

### Auth Routes

| Method | Endpoint | Description |
| :--- | :--- | :--- |
| `POST` | `/auth/register` | Register a new user. |
| `POST` | `/auth/login` | Log in a user and receive a JWT. |

### Post Routes

| Method | Endpoint | Description | Access |
| :--- | :--- | :--- | :--- |
| `GET` | `/posts` | Get all blog posts. | Public |
| `POST` | `/posts` | Create a new blog post. | Private |
| `PUT` | `/posts/:id` | Update a specific post. | Private (Author only) |
| `DELETE` | `/posts/:id` | Delete a specific post. | Private (Author only) |
