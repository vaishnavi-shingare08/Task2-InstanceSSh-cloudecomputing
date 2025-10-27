
**Task 2: Launch a Virtual Machine (VM) Instance)** 

---


# ☁️ Task 2: Launch a Virtual Machine (VM) Instance

## 🎯 Objective

To understand how **cloud virtual machines** work by creating, configuring, and connecting to a **cloud-based server instance** using a free-tier account.  
This task demonstrates the fundamentals of **Infrastructure-as-a-Service (IaaS)** and how to manage remote servers in the cloud.

---

## 🛠 Tools Used

- **AWS EC2 Free Tier** *(Amazon Web Services)*  
  or  
- **Google Cloud Compute Engine** *(any free-tier platform is acceptable)*  
- **Operating System:** Ubuntu 22.04 LTS  
- **Connection Method:** SSH (Secure Shell)

---

## 🚀 Steps to Launch and Connect to the VM

### 1️⃣ Login & Setup
- Logged in to **AWS Free Tier account**.  
- Navigated to **EC2 Dashboard → Instances → Launch Instance**.

### 2️⃣ Create the VM Instance
- **Name:** MyUbuntuServer  
- **AMI (OS):** Ubuntu Server 22.04 LTS (Free-tier eligible)  
- **Instance Type:** `t2.micro` (1 vCPU, 1GB RAM)  
- **Region:** Asia Pacific (Mumbai) `ap-south-1`

### 3️⃣ Configure Firewall
- Enabled **HTTP (port 80)** and **HTTPS (port 443)** for web access.  
- Allowed **SSH (port 22)** from my public IP for secure remote login.

### 4️⃣ Key Pair Setup
- Created a new key pair named `925-open.pem` for authentication.  
- Adjusted permissions using:
  ```bash
  chmod 400 925-open.pem
````

### 5️⃣ Launch & Connect

* Launched the instance and noted its **Public IP (e.g., 3.110.28.87)**.
* Connected via SSH:

  ```bash
  ssh -i 925-open.pem ubuntu@3.110.28.87
  ```

### 6️⃣ Verification

Once connected, verified system details:

```bash
uname -a
ls
whoami
```

✔️ Output confirmed successful SSH connection and active VM instance.

---

## 🖼️ Screenshots (Deliverables)

* ✅ Screenshot of **running VM instance** on the cloud console.
* ✅ Screenshot of **terminal access via SSH connection**.

---

## 🧾 VM Configuration Summary

| Parameter          | Description                   |
| ------------------ | ----------------------------- |
| **OS**             | Ubuntu 22.04 LTS              |
| **Region**         | ap-south-1 (Mumbai)           |
| **Machine Type**   | t2.micro (Free Tier Eligible) |
| **CPU / RAM**      | 1 vCPU / 1 GB RAM             |
| **Firewall Rules** | SSH, HTTP, HTTPS Enabled      |

---

## 💡 Outcome

By completing this task, I have:

* Understood how to **create and manage cloud-based virtual machines**.
* Learned how to **connect securely via SSH**.
* Gained practical experience in **IaaS (Infrastructure-as-a-Service)** concepts.

---

## 🧠 Author

**Name:** Vaishnavi
**Project:** Cloud Internship – Task 2
**Date:** October 2025
**Platform:** AWS EC2 (Free Tier)
