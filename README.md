# future_cs_01
vulnerability Assesment Report
# 🔐 Vulnerability Assessment Report (Passive Reconnaissance)

## 📄 Overview
This repository contains a **Vulnerability Assessment Report** conducted using a **read-only, passive reconnaissance approach**.  
The assessment evaluates the security posture of a deliberately vulnerable web application without performing any active exploitation.

- **Assessment Type:** Passive / Read-only  
- **Scope:** Ethical & non-intrusive  
- **Overall Risk Rating:** **HIGH**

> ⚠️ No attacks, exploitation, or intrusive testing were performed at any stage.

---

## 🎯 Target Application
- **URL:** http://testphp.vulnweb.com  
- **Purpose:** Intentionally vulnerable web application maintained by **Acunetix** for security training and research.

---

## 🧪 Methodology
The assessment was carried out using **publicly observable information only**, focusing on:
- HTTP response headers
- SSL/TLS configuration
- Cookie attributes
- Directory exposure
- Open network services

### ❌ Explicitly Excluded
- SQL Injection
- Authentication bypass
- Brute-force attacks
- Denial-of-Service (DoS)
- Any form of active exploitation

---

## 🛠️ Tools Used
- **OWASP ZAP** (Passive Scan Mode)
- **Nmap** (Safe scan with `-Pn` and version detection)
- **Browser Developer Tools**
- **SSL Labs**
- **SecurityHeaders.com**
- **BuiltWith / Wappalyzer**

---

## 📊 Findings Summary
A total of **8 security findings** were identified:

| Severity | Count |
|--------|-------|
| High   | 1 |
| Medium| 4 |
| Low / Info | 3 |

### Key Issues Identified
- Missing critical HTTP security headers
- No HTTPS enforcement or HSTS
- Insecure session cookie configuration
- Server information disclosure
- Directory listing enabled
- Public exposure of SSH service

---

## 🛡️ Sample Vulnerabilities
- Missing **Content-Security-Policy**
- Missing **X-Frame-Options** (Clickjacking risk)
- Missing **X-Content-Type-Options**
- No HTTPS redirect and missing **HSTS**
- Session cookies without **Secure** and **HttpOnly** flags

---

## 🚀 Remediation Highlights
Most findings are **configuration-level issues** and can be fixed quickly:

- Enforce HTTPS and enable HSTS
- Add standard HTTP security headers
- Harden cookie attributes
- Disable directory listing
- Restrict SSH access using firewall or VPN

Many fixes are **quick wins** requiring minimal effort.

---

## 📁 Repository Contents
- `Vulnerability_Assessment_Report_2026.pdf` – Full detailed assessment report

---

## ⚖️ Disclaimer
This assessment was conducted strictly within a **passive, ethical, and legal scope**.  
The target application is intentionally vulnerable and used solely for educational purposes.

> Results do not guarantee the discovery of all vulnerabilities and should not be treated as a complete security audit.

---

## 👩‍💻 Author
**Nishalini M**  
Security Assessment & Academic Project  
April 2026

---

## 📌 Note
This repository is intended for:
- Academic reference
- Learning and training
- Demonstrating vulnerability assessment methodology

**Not intended for malicious use.**
