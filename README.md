
# 🔐 Task 4: Setup and Use a Firewall on Linux (UFW)

## 🎯 Objective
Configure and test basic firewall rules to allow or block network traffic using **UFW (Uncomplicated Firewall)** on Kali Linux.

---

## 🛠 Tools Used
- **Operating System:** Kali Linux
- **Firewall Utility:** UFW (Uncomplicated Firewall)

---

## ⚙️ Steps Performed

### 1️⃣ Install and Enable UFW
First, I updated the system and installed UFW, then enabled it to start filtering traffic:
```bash
sudo apt update
sudo apt install ufw -y
sudo ufw enable
```

### 2️⃣ Allow SSH on Port 22
SSH (port 22) is allowed to enable secure remote access:
```bash
sudo ufw allow 22
```

### 3️⃣ Block Telnet on Port 23
Telnet (port 23) is an outdated and insecure protocol. It was blocked using:
```bash
sudo ufw deny 23
```

### 4️⃣ Check Firewall Rules
Used the following command to verify current active rules:
```bash
sudo ufw status numbered
```

### 5️⃣ Remove the Test Rule (Telnet Block)
To revert the test block, I removed the Telnet rule:
```bash
sudo ufw delete deny 23
```

---

## 🧠 What I Learned
- How to install and enable UFW on a Linux system.
- How to allow and deny specific ports using firewall rules.
- Importance of securing or blocking unused services (e.g., Telnet).
- How to verify and delete firewall rules as needed.

---

## 🔑 Key Concepts

| Term | Description |
|------|-------------|
| **Firewall** | A system that filters incoming and outgoing network traffic. |
| **UFW** | A user-friendly interface for managing iptables on Linux. |
| **Inbound Rules** | Control traffic coming *into* your machine. |
| **Port 22 (SSH)** | Secure access port – must be allowed. |
| **Port 23 (Telnet)** | Insecure legacy port – often blocked for safety. |

---

## ✅ Conclusion
This task provided hands-on experience in configuring a Linux-based firewall. I learned how to manage ports securely and apply real-time rules that filter traffic, enhancing my understanding of Linux security fundamentals.
