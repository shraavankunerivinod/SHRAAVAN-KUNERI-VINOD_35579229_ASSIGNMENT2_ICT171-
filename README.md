
# NetShield Solutions - Cloud Server Project

**ICT171 Introduction to Server Environments and Architectures (S1, 2025)**  
**Assignment 2: Cloud Project & Video Explainer**  
**Student Name:** Shraavan Kuneri Vinod  
**Student Number:** 35579229  
**Project Title:** NETSHIELD SOLUTIONS - Cloud Server Project  
**Domain Name:** nssolutions.shop  
**Public IP Address:** 3.107.201.139  
**Video Explainer Link:** _[Insert your video link here]_  
**GitHub Repository Link:** _[Insert your GitHub repo URL here]_  

---

##  Development Timeline (Iterative Improvement Over 4 Weeks)
- **Week 1:** AWS EC2 instance setup and domain registration via GoDaddy.
- **Week 2:** Core HTML pages developed: index, login, dashboard, blog.
- **Week 3:** VPN & TeamSpeak integration, SSL cert setup.
- **Week 4:** Scripts, automation, UI polishing, testing, and documentation finalized.

---

##  Infrastructure Setup on AWS EC2

**Steps Followed:**
1. Logged into AWS Management Console.
2. Launched a new instance using **Ubuntu 22.04 (AMI)**.
3. Selected **t2.micro** instance type (free-tier eligible).
4. Created a **new key pair** and downloaded the PEM file.
5. Allowed **SSH traffic from the internet**.
6. Selected **8 GiB gp3** for storage.
7. Launched the instance and connected via SSH:

```bash
ssh -i "mytestserverkeypair.pem" ubuntu@ec2-3-107-201-139.ap-southeast-2.compute.amazonaws.com
```

---

##  Domain, DNS & SSL Configuration

- **Domain Provider:** GoDaddy  
- **Domain Name:** `nssolutions.shop`  
- **Public IP Address:** `3.107.201.139`

**SSL/TLS Certificate Configuration:**
```bash
sudo snap install --classic certbot
sudo ln -s /snap/bin/certbot /usr/bin/certbot
sudo certbot --apache
```

---

##  Website Functionality & Structure

### Pages Developed:
- **index.html:** Company introduction, services, navigation.
- **login.html:** Role-based login (Agent/Client) with localStorage.
- **dashboard.html:** User profile, stats, quick links, logout.
- **vpn.html:** Setup guide, download links, privacy check (ipleak.net).
- **teamspeak.html:** Mailto link for access request + confirmation.
- **blog.html:** Lists blog articles.
- **blogspot1.html:** Zero-day exploits.
- **blogspot2.html:** Top 10 cybersecurity tools.

### Key Features:
- Responsive UI (Orbitron font, dark theme).
- Custom JavaScript for login validation, redirection, and dashboard stats.
- TeamSpeak integration using `mailto:` for access.
- VPN setup with OpenVPN/WireGuard configuration.
- Blog sections for cybersecurity education.

---

## 🖹 HTML Code Snippets (Index Page Example)
```html
<!-- index.html -->
<header>
  <h1>NetShield Solutions</h1>
  <p>Delivering intelligent monitoring to protect data from unauthorized access using AI + human expertise.</p>
</header>
```

### Full code for all pages is available in the repository.

---

##  Script Details & Usefulness

### JavaScript Logic Implemented:
- Role selection (Agent/User) with display toggling.
- Local storage of session details.
- Fake dashboard stat generation.
- Session check and redirection on all protected pages.
- Logout logic.
- Mailto trigger for TeamSpeak support.

**Purpose:**
- Demonstrates frontend authentication simulation.
- Provides user experience simulation for a multi-role portal.
- Automates navigation and updates.

## TOTAL COST OF OWNERSHIP
- EC2 - $O(per year)
- GODADDY(DOMAIN) - $3(per year)
- STORAGE(8GiB) - $9.60(per year)
- TOTAL - $12.60(per year)
- For 5 years, the total cost of running this website will be $63.

##  Documentation & Replication

- **Setup Instructions Included** (EC2 + SSL + DNS).
- **Scripts Documented** inline in HTML + JS files.
- **Project is replicable** end-to-end using this README.

---

##  DNS & SSL Documentation

**DNS:** Configured via GoDaddy to point A record to EC2 IP.  
**SSL:** Enabled using Certbot + Apache, generating a secure `https://` URL.  
**Result:** Fully functional HTTPS-enabled site.

---

##  Cloud Online Project Availability

- **Public DNS:** [http://nssolutions.shop](http://nssolutions.shop)  
- **SSL:** Enabled via Certbot (HTTPS functional)  
- **Availability:** Monitored post-deployment, available without downtime.

---

### © 2025 NetShield Solutions - Shraavan Kuneri Vinod (35579229)
*Submitted as part of ICT171 - Murdoch University*
