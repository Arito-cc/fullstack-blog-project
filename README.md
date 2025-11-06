# 📰 VintageVerse | Full-Stack MERN Blog Project 🚀
**VintageVerse** is a complete full-stack blog application built using the **MERN stack (MongoDB, Express, React, Node.js)**.  
Developed as a **minor full-stack project**, it demonstrates secure authentication, clean REST APIs, and a responsive, modern frontend built with **React (Vite)** and **Tailwind CSS**.  
Users can **register**, **log in**, and perform **full CRUD (Create, Read, Update, Delete)** operations on their own posts — all within a smooth and minimal user interface.

---

## 🌐 Live Links & Test Credentials

### 🔗 Live Demo  
**Frontend:** [https://frontend-blog-project.onrender.com/](https://frontend-blog-project.onrender.com/)  
**Backend API:** [https://backend-blog-project-5lv7.onrender.com/](https://backend-blog-project-5lv7.onrender.com/)

### 🧪 Test Credentials  
You can log in using:  
**Email:** `test1@example.com`  
**Password:** `password123`  

Or simply create your own account!

---

## ✨ Key Features  
- 🔒 **Secure User Authentication** – Full registration & login system using JWT  
- 🧂 **Password Hashing** – Uses bcrypt.js for one-way encryption  
- 🪪 **JWT Authorization** – Protects routes and validates users  
- ✍️ **Full CRUD for Posts**  
  - **Create:** Logged-in users can create new posts  
  - **Read:** Anyone can view all posts  
  - **Update:** Only authors can edit their posts  
  - **Delete:** Only authors can delete their posts  
- 🧠 **Global State Management** – React Context API for user auth state  
- 📱 **Responsive Design** – Fully responsive with Tailwind CSS  
- 🧍 **Author-Only Permissions** – Enforced securely at the backend level  

---

## 🛠️ Tech Stack  
| Category | Technology | Description |  
|-----------|-------------|-------------|  
| **Frontend** | React (Vite) | Fast and modern frontend framework |  
|  | React Router | Client-side routing |  
|  | Tailwind CSS | Utility-first CSS styling |  
|  | Axios | HTTP requests |  
|  | React Context API | Auth and state management |  
| **Backend** | Node.js | JavaScript runtime environment |  
|  | Express.js | RESTful API framework |  
|  | MongoDB | NoSQL database |  
|  | Mongoose | ODM for MongoDB |  
|  | JWT (jsonwebtoken) | Token-based authentication |  
|  | bcrypt.js | Password hashing |  
| **Deployment** | Render | Cloud hosting for both frontend & backend |  

---

## 🏁 Getting Started (Local Development)  
Follow these simple steps to run **VintageVerse** locally 👇  

### ✅ Prerequisites  
- [Node.js](https://nodejs.org/) (includes npm)  
- [MongoDB Atlas](https://www.mongodb.com/atlas) account or local MongoDB  
- [Postman](https://www.postman.com/) *(optional for API testing)*  

---

### 1️⃣ Backend Setup (`/server` folder)

Clone the repository

```bash
git clone https://github.com/Arito-cc/vintageverse.git
cd vintageverse/server
```

Install dependencies

```bash
npm install
```

Create a .env file inside /server
```env
MONGO_URI=your_mongodb_connection_string_here
JWT_SECRET=your_super_strong_secret_key_here
PORT=5000
```

```bash
# Run the backend
npm run dev
```

Your backend will run at 👉 **http://localhost:5000**

---

### 2️⃣ Frontend Setup (`/client` folder)
```bash
# Open a new terminal
cd ../client

# Install dependencies
npm install
```
In `client/src/api/api.js`, set your API base URL
```js
baseURL: 'http://localhost:5000/api'
```
# Run the frontend
```bash
npm run dev
```

Your app will be available at 👉 **http://localhost:5173**

---

## 📖 API Endpoints  
All routes are prefixed with `/api`.

### 🔐 Auth Routes  
| Method | Endpoint | Description |  
|--------|-----------|-------------|  
| POST | `/auth/register` | Register a new user |  
| POST | `/auth/login` | Log in and receive JWT |  

### 📝 Post Routes  
| Method | Endpoint | Access | Description |  
|--------|-----------|---------|-------------|  
| GET | `/posts` | Public | Get all blog posts |  
| POST | `/posts` | Private | Create a new post |  
| PUT | `/posts/:id` | Private (Author only) | Update a post |  
| DELETE | `/posts/:id` | Private (Author only) | Delete a post |  

---

## 💾 Deployment  
The app is deployed on **Render.com** for both the frontend and backend.  
To deploy your own version:  
1. Fork this repository  
2. Connect your GitHub to [Render.com](https://render.com/)  
3. Deploy backend first → then frontend  
4. Update your frontend `baseURL` with the deployed backend link  

---

## 💡 Future Enhancements  
- 🗂️ Add post categories & tags  
- 💬 Comment system  
- 🖼️ Image upload support  
- 🔍 Search & filter posts  
- ❤️ Like, bookmark & share functionality  

---

## 👨‍💻 Author  
**Abhishek Chaudhary**  
📧 [contact.abhishek.cc@gmail.com](mailto:contact.abhishek.cc@gmail.com)  
🔗 [LinkedIn](https://www.linkedin.com/in/contactabhishekcc) | [GitHub](https://github.com/Arito-cc)  

---

## 🌟 Support  
If you found **VintageVerse** helpful or inspiring, consider giving it a ⭐ on GitHub!  
Your support motivates me to create more amazing projects ❤️
