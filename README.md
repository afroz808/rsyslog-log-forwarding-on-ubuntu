# 📡 System-to-System Log Forwarding using rsyslog on Ubuntu

👨‍💻 **Author:** Afroz Shaikh  
📧 **Email:** afrozshaikh8086@gmail.com  

---

## 🚀 Project Overview

This project demonstrates how to configure **log forwarding** from one Ubuntu machine to another using `rsyslog`. This simulates a real-world SIEM/log pipeline setup, commonly used in **Security Operations Centers (SOC)**, centralized logging, and incident monitoring environments.

---

## 🛠️ Technologies Used

- Ubuntu 20.04 / 22.04  
- rsyslog (default logging service)  
- Nano text editor  
- Basic Linux CLI  

---

## 🧪 Use Case

- Create a **home SOC lab** for log management practice  
- Simulate **real-time log forwarding** between systems  
- Prepare for working with SIEM tools like Splunk, Sentinel, or ELK  
- Understand the flow of logs in enterprise-level architecture  

---

## 🔧 Step-by-Step Configuration

```bash
# 1. Open terminal and go to the /etc directory
cd /etc

# 2. Open the rsyslog.conf file with root privileges
sudo nano /etc/rsyslog.conf

# 3. Add this line at the bottom of the file to forward all logs over UDP
*.* @192.168.1.9:514
# Use @@ instead of @ if you want to use TCP
# Example: *.* @@192.168.1.9:514

# 4. Save and exit the file
# Press Ctrl + X → Y → Enter

# 5. Restart the rsyslog service to apply changes
sudo systemctl restart rsyslog
