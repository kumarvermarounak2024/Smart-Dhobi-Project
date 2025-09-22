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
- Git & GitHub – Version control
- AWS IAM – Secure user creation & role-based access 
- AWS VPC – Isolated virtual private cloud  
- AWS Subnet – Public subnet for EC2 hosting  
- AWS Route Table – Configured with internet access rule (0.0.0.0/0 → IGW)  
- AWS Internet Gateway (IGW) – Internet access for VPC  
- AWS EC2 (Ubuntu VPS inside VPC) – Hosting environment
- Jenkins (on EC2) – CI/CD automation
- Docker (on EC2) – Containerized application deployment
- Nginx (on EC2) – Reverse proxy & SSL termination
- Certbot (Let’s Encrypt) – SSL (HTTPS)
- AWS Route53 – DNS management (GoDaddy domain integration)
- GoDaddy – Domain provider

---

## ⚙️ Deployment Workflow

1. **IAM User Creation**  
   - IAM user created with limited permissions.  
   - Used Access Key & Secret Key for secure AWS operations. 

2. **VPC + Networking Setup**  
   - Created a VPC. 
   - Added a Subnet inside the VPC.  
   - Configured Route Table (0.0.0.0/0 → Internet Gateway).
   - Attached Internet Gateway (IGW) for public access.

3. **EC2 VPS Setup**  
   - Launched EC2 instance (Ubuntu) inside the Subnet.  
   - Installed Jenkins, Docker, and Nginx inside EC2.

4. **Code Push to GitHub**  
   - Developer pushes code to GitHub repository.

5. **CI/CD with Jenkins**
   - Jenkins pulls the latest code from GitHub.
   - Builds Docker images & deploys containers.

6. **Docker (on EC2 VPS)**
   - Runs frontend & backend services in containers.

7. **Nginx + Certbot (on EC2 VPS)**
   - Nginx configured as reverse proxy for Docker containers.
   - SSL enabled via Certbot (Let’s Encrypt).

8. **Domain & DNS (GoDaddy + Route53)**
   - Domain purchased from GoDaddy.
   - Route53 hosted zone configured for DNS.
   - A-record points to EC2 public IP.

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

