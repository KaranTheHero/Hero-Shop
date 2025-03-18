# 🚀 Hero Shop - E-Commerce Website (Deployed on Vercel & Render)

Welcome to **Hero Shop**, a fully functional and modern e-commerce platform. This guide provides a **step-by-step setup**, deployment instructions, and everything you need to run the project **locally** or on **the cloud**.

---

## 🌍 Live Deployment
- **Frontend (Vercel):** [Hero Shop on Vercel](https://karan-the-hero-shop.vercel.app)
- **Backend (Render):** [Hero Shop API on Render](https://hero-shop.onrender.com)

---

## 📁 Project Structure
```
Hero Shop/
├── backend/       # Node.js + MongoDB API
│   ├── config/       # Database connection
│   ├── controllers/  # Authentication & Payment Logic
│   ├── middleware/   # Error handling & security
│   ├── models/       # Database schemas
│   ├── routes/       # API endpoints
│   ├── .env          # Environment variables (DO NOT SHARE)
│   ├── .gitignore    # Git Ignore File
│   └── server.js     # Main backend server file
├── frontend/      # HTML + CSS + JavaScript (Client-side)
│   ├── img/          # Images Folder
│   ├── products/     # Product Assets
│   ├── index.html    # Home Page
│   ├── about.html    # About Page
│   ├── cart.html     # Shopping Cart Page
│   ├── contact.html  # Contact Page
│   ├── login.html    # Login Page
│   ├── product.html  # Product Details Page
│   ├── signup.html   # Signup Page
│   ├── styles.css    # Website Styling
│   └── scripts.js    # API Interactions
```

---

## ✅ Prerequisites
Ensure the following software is installed on your system:

| Software                                | Download Link                                                            |
| --------------------------------------- | ------------------------------------------------------------------------ |
| Node.js                                 | [Download Node.js](https://nodejs.org/)                                  |
| MongoDB Compass (Optional for local DB) | [Download MongoDB Compass](https://www.mongodb.com/try/download/compass) |
| Git                                     | [Download Git](https://git-scm.com/downloads)                            |
| VS Code                                 | [Download VS Code](https://code.visualstudio.com/)                       |

---

## 🔑 Environment Variables Setup
Inside the **backend** folder, create a `.env` file with the following content:

```env
MONGODB_URI=mongodb+srv://Username:Password@Clustername.mongodb.net/hero-shop
PORT=5000
JWT_SECRET=YourCustomSecret
JWT_EXPIRES_IN=90d
RAZORPAY_KEY_ID=YourRazorpayKey
RAZORPAY_KEY_SECRET=YourRazorpaySecret
```

✅ **Never share your `.env` file online or commit it to GitHub!**

---

## 📌 Backend Installation & Setup
1. Clone the repository:
```bash
git clone https://github.com/YourUsername/HeroShop.git
cd HeroShop/backend
```
2. Install dependencies:
```bash
npm install
```
3. Install development dependencies for auto-restart:
```bash
npm install nodemon --save-dev
```
4. Start the backend server **locally**:
```bash
npm run dev  # For Development Mode (Auto Restart)
```
✅ **If successful, you will see:**
```
MongoDB Connected...
Server running on port 5000
```

### 🚀 Deploying Backend to Render
1. Go to [Render](https://render.com/) and create an account.
2. Click **New Web Service** → Connect your GitHub repository.
3. Set **Start Command** to:
```bash
npm start
```
4. Add the environment variables from `.env` into Render.
5. Click **Deploy**, and your backend will be live!

✅ **Your API will be available at:** `https://your-render-api.com`

---

## 🌐 Frontend Setup
1. Navigate to the frontend folder:
```bash
cd ../frontend
```
2. Open `index.html` in **Live Server** (for local testing).
3. Ensure API endpoints in `scripts.js` are correct:
```js
const endpoints = {
    signup: 'https://your-render-api.com/api/auth/signup',
    login: 'https://your-render-api.com/api/auth/login'
};
```
4. Refresh your browser – the website should be live!

### 🚀 Deploying Frontend to Vercel
1. Go to [Vercel](https://vercel.com/) and create an account.
2. Click **New Project** → Connect your GitHub repository.
3. Set **Framework Preset** to **HTML/CSS/JS**.
4. Click **Deploy**, and your frontend will be live!

✅ **Your website will be available at:** `https://karan-the-hero-shop.vercel.app`

---

## 🔌 MongoDB Local Setup (Optional)
If you want to use a local MongoDB instance instead of the cloud:
```
mongodb://localhost:27017/hero-shop
```

---

## 🎯 Running the Full Application
| Step                     | Command                                     | Folder       |
| ------------------------ | ------------------------------------------- | ------------ |
| Install Backend          | `npm install`                               | **backend**  |
| Install Dev Dependencies | `npm install nodemon --save-dev`            | **backend**  |
| Start Backend Locally    | `npm run dev`                               | **backend**  |
| Deploy Backend (Render)  | [Follow Render Setup](https://render.com/)  | **backend**  |
| Start Frontend Locally   | Open with **Live Server**                   | **frontend** |
| Deploy Frontend (Vercel) | [Follow Vercel Setup](https://vercel.com/)  | **frontend** |

---

## 🚀 Pushing to GitHub
To upload your project to GitHub:

1. Create a new repository on [GitHub](https://github.com/).
2. In the project root, initialize Git:
```bash
git init
git add .
git commit -m "Initial Commit"
git remote add origin https://github.com/YourUsername/YourRepositoryName.git
git push -u origin main
```
✅ Your project is now on GitHub!

---

## 💡 Final Notes
- **Your project is fully deployed on Vercel (frontend) & Render (backend).**
- **Follow security best practices:** Never expose your `.env` file.
- **Ensure your API and frontend URLs are correct after deployment.**
- **This project is fully tested and working!** 🚀

👨‍💻 Happy Coding!