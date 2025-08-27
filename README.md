# 🧺 Smart Dhobi - Premium Laundry Services

Smart Dhobi is a premium laundry service platform that allows customers to book laundry services online.  
It connects customers with professional dhobis in their area for quick, reliable, and convenient service.

🌐 Live Project: [https://smartdhobi.in](https://smartdhobi.in)  
🔗 API: [https://api.smartdhobi.in](https://api.smartdhobi.in)

---

## 🚀 Features
- Customer registration & login  
- Dhobi (service provider) registration  
- Laundry services booking system  
- Location-based search for nearby dhobis  
- Premium services (Wash & Fold, Dry Cleaning, Express Service)  
- Secure authentication system  
- Admin dashboard for managing services  

---

## 🛠️ Tech Stack

**Frontend:** React, TailwindCSS, Vite  
**Backend:** Node.js, Express, MongoDB  
**DevOps & Deployment:**  
- AWS EC2 (Ubuntu)  
- Docker  
- Jenkins (CI/CD)  
- Nginx (Reverse Proxy)  
- Git & GitHub (Version Control)  
- Route53 (DNS Management) with GoDaddy domain  
- Certbot (SSL HTTPS)  

---

## ⚙️ Deployment Workflow

1. **Code Push to GitHub**  
   - Developer pushes code to GitHub repository.

2. **CI/CD with Jenkins**  
   - Jenkins fetches the latest code.  
   - Runs build and Docker image creation.  
   - Pushes Docker image to container.  

3. **Docker + Nginx**  
   - Application runs inside Docker container.  
   - Nginx is configured as reverse proxy.  
   - SSL enabled using Let's Encrypt (Certbot).  

4. **Domain & DNS (GoDaddy + Route53)**  
   - Domain purchased from GoDaddy.  
   - Configured with AWS Route53 for DNS.  
   - A-records point to EC2 public IP.  

---

### 🏠 Home Page
![Home Page](/frontend/src/assets/screenshot-home.png)

### 📋 Services
![Services](/frontend/src/assets/screenshot-services.png)

### ℹ️ How it Works
![How it Works](/frontend/src/assets/screenshot-how-it-works.png)

### 📍 Find Nearby
![Find Nearby](/frontend/src/assets/screenshot-find-nearby.png)

### 👥 Customer Registration
![Customer Registration](/frontend/src/assets/screenshot-customer-registration.png)

### 🔑 Login
![Login](/frontend/src/assets/screenshot-login-page.png)

### 📊 Dashboard
![Dashboard](/frontend/src/assets/screenshot-dashboard.png)

### 🧺 Dhobi Manage
![Dhobi Manage](/frontend/src/assets/screenshot-dhobi-manage.png)

### 👤 User Manage
![User Manage](/frontend/src/assets/screenshot-user-manage.png)

### 📦 Order Manage
![Order Manage](/frontend/src/assets/screenshot-order-manage.png)

---

## 🚀 How to Run Locally

```bash
# Clone repository
git clone https://github.com/your-username/smart-dhobi.git
cd smart-dhobi

# Backend setup
cd backend
sudo npm install
node index.js OR npm run dev

# Frontend setup
cd frontend
sudo npm install
npm run dev

