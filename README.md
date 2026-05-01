# SOC Analyst Lab – Brute Force Attack Investigation

## 📌 Objective
This project simulates a SOC Analyst Level 1 investigation of a suspected brute-force attack using Linux authentication logs. The goal is to detect suspicious activity, analyze logs, identify indicators of compromise (IOCs) and recommend mitigation actions.

---

## 🛠️ Tools Used
- Kali Linux / Ubuntu
- Linux Authentication Logs (/var/log/auth.log)
- Bash / Command Line
- Python (for log analysis)
- GitHub for documentation

---

## 🚨 Scenario
A system administrator reports multiple failed login attempts on a Linux server. As a SOC Analyst, your task is to investigate whether this is a brute-force attack.

---

## 🔍 Steps Performed

### 1. Log Collection
- Accessed authentication logs from `/var/log/auth.log`

### 2. Log Analysis
- Filtered failed login attempts
- Identified repeated login failures from specific IP addresses

### 3. Detection of Suspicious Activity
- Multiple failed login attempts in a short period
- Same IP attempting different usernames

### 4. Indicators of Compromise (IOCs)
- Suspicious IP address (e.g., 192.168.1.100)
- Repeated failed SSH login attempts
- Unauthorized login patterns

### 5. Conclusion
The activity is consistent with a brute-force attack targeting SSH authentication.

---

## 🛡️ Mitigation Actions
- Block malicious IP using firewall (iptables)
- Disable password authentication (use SSH keys)
- Install Fail2Ban
- Enable account lockout policies

---

## 📊 Outcome
Successfully detected and analyzed a brute-force attack scenario, demonstrating SOC L1 skills in log analysis, alert triage and incident documentation.

---

## 📁 Project Structure
logs/ 
analysis/ 
screenshots/

---

## 🔗 Author
Rodgers Rono  
GitHub: https://github.com/Ronoh12
