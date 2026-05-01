# 🔍 Incident Investigation Report – Brute Force Attack

## 📅 Date of Analysis
10 January 2026

---

## 🚨 Incident Summary
Multiple failed SSH login attempts were detected on a Linux server from a single IP address, indicating a potential brute-force attack.

---

## 📂 Log Source
- File: `/var/log/auth.log`
- Service: SSH (sshd)

---

## 🔎 Findings

### 1. Repeated Failed Login Attempts
Several failed login attempts were observed from the IP address:

- **192.168.1.100**

Targeted usernames included:
- admin
- root
- test
- guest
- user

---

### 2. Pattern Identified
- Rapid login attempts within seconds
- Multiple usernames targeted
- Same IP address used

👉 This behavior is consistent with a brute-force attack.
Accepted password for validuser from 192.168.1.100


- Indicates attacker may have gained access
- Elevates incident severity to **HIGH**

---

## 🚩 Indicators of Compromise (IOCs)

- Malicious IP: **192.168.1.100**
- Attack Type: SSH Brute Force
- Target: Linux Authentication System

---

## ⚠️ Risk Level
**HIGH**

Reason:
- Successful login after multiple failed attempts

---

## 🛡️ Recommended Actions

1. Block IP address:
   ```bash
   sudo iptables -A INPUT -s 192.168.1.100 -j DROP
   Enable Fail2Ban to prevent brute-force attacks
2. Disable password authentication:
3. Use SSH key-based authentication
4. Review user account:
5. Investigate "validuser" activity
6. Reset compromised credentials immediately

📊 Conclusion

The investigation confirms a brute-force attack originating from a single IP address. The presence of a successful login suggests a possible compromise, requiring immediate response and containment.

👨‍💻 Analyst
Rodgers Rono


---
