
# Honeypot Simulation with Wazuh + Cowrie on AWS

This project simulates a real-world SOC simulation environment using:

- **Wazuh SIEM server** on AWS EC2 (Ubuntu)
- **Kali Linux Purple** as a honeypot host
- **Cowrie SSH/Telnet honeypot**
- **Wazuh agent** for log forwarding
- Basic **attack simulations** (SSH brute-force, etc.)

> Emphasis is on simulation and learning, not accurate attacker identification.

---

## 🔧 Setup Overview

### 🖥️ Wazuh Server
- Hosted on **AWS EC2**
- Installed **Wazuh Manager**, **Dashboard**, and **Indexer**
- Security group configured for necessary ports (e.g., 443, 1515, 1514/tcp)

### 🐍 Kali Purple Honeypot
- Installed **Wazuh Agent**
- Deployed **Cowrie** honeypot (SSH emulation)
- Connected agent to Wazuh server via TCP (port 1514)
- Edited `ossec.conf` to forward Cowrie logs

---

## ⚔️ Attack Simulation

Basic attacks performed:
- SSH login attempts (`ssh root@<honeypot-ip> -p 2222`)
- Multiple failed login tries
- Log monitoring through Wazuh dashboard

---

## 📊 Observations

- Wazuh successfully collected system logs, Cowrie logs, and attack traces
- Dashboards showed alerts, file integrity monitoring, and syscollector info
- Focus was more on **log visibility and SIEM simulation**

---

## 📸 Screenshots Included

- EC2 setup (AWS Console)
- Wazuh dashboard (alerts, pie charts)
- Cowrie terminal logs
- Wazuh agent terminal on Kali
- Edited `ossec.conf` configuration
- Sample alerts and JSON logs

---

## 🧠 Key Learnings

- Hands-on Wazuh installation (agent + manager + dashboard)
- AWS EC2 networking, storage, and instance management
- Log forwarding and honeypot simulation
- Realistic SIEM setup and attack emulation basics

---

## 📁 Project Structure


---

## ✅ Status

✔️ Completed as a learning simulation project  
✔️ System teardown completed (AWS instance stopped)

---

## 🙏 Credits
 [Wazuh Documentation](https://documentation.wazuh.com)
- [Cowrie Honeypot](https://github.com/cowrie/cowrie)
- [Wazuh Documentation](https://documentation.wazuh.com)
- [Cowrie Honeypot](https://github.com/cowrie/cowrie)
