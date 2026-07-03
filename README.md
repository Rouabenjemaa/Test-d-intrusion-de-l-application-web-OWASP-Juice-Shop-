# OWASP Juice Shop Penetration Testing Report

## 📌 Project Overview

This project presents a comprehensive penetration testing assessment of the **OWASP Juice Shop** vulnerable web application. The objective was to identify, exploit, and document common web security vulnerabilities following industry best practices and the OWASP Top 10.

The report covers the complete penetration testing process, including reconnaissance, vulnerability discovery, exploitation, risk assessment, and remediation recommendations.

---

## 👥 Authors

* **Roua Ben Jemaa**
* **Mohamed Mahdi Dkhil**

Academic Year: **2025–2026**

---

## 🎯 Objectives

* Perform reconnaissance on the target application.
* Identify exposed services and technologies.
* Discover security vulnerabilities.
* Exploit identified weaknesses in a controlled environment.
* Assess risks according to severity.
* Provide practical remediation recommendations.

---

## 🛠️ Technologies & Tools

* OWASP Juice Shop
* Nmap
* WhatWeb
* cURL
* Wafw00f
* Web Browser Developer Tools
* Manual Security Testing

---

## 📂 Project Structure

```text
.
├── Report.pdf / Report.docx
├── Screenshots
├── README.md
```

---

## 🔍 Information Gathering

The reconnaissance phase identified:

* Target: localhost
* Web Application: OWASP Juice Shop
* Open Port: 3000/tcp
* HTTP Service
* HTML5
* jQuery 2.2.4
* Accessible robots.txt
* Exposed `/ftp` directory
* No Web Application Firewall (WAF) detected
* Permissive CORS configuration

---

## 🚨 Identified Vulnerabilities

| ID        | Vulnerability                      | Severity    |
| --------- | ---------------------------------- | ----------- |
| JUICY-001 | SQL Injection (Login)              | 🔴 Critical |
| JUICY-002 | SQL Injection (Search)             | 🔴 Critical |
| JUICY-003 | Weak Administrator Password        | 🔴 Critical |
| JUICY-004 | Sensitive Data Exposure (/ftp)     | 🟠 High     |
| JUICY-005 | Broken Access Control (Basket)     | 🟠 High     |
| JUICY-006 | Broken Access Control (Admin Page) | 🟠 High     |
| JUICY-007 | Public Score Board                 | 🟡 Medium   |
| JUICY-008 | Exposed API Documentation          | 🟡 Medium   |
| JUICY-009 | Cross-Site Scripting (XSS)         | 🟡 Medium   |
| JUICY-010 | Cross-Site Request Forgery (CSRF)  | 🟡 Medium   |

---

## 🔐 Security Recommendations

* Use parameterized SQL queries.
* Validate and sanitize all user inputs.
* Enforce strong password policies.
* Enable Multi-Factor Authentication (MFA).
* Restrict access to sensitive directories.
* Implement Role-Based Access Control (RBAC).
* Protect API documentation.
* Deploy a strict Content Security Policy (CSP).
* Implement anti-CSRF tokens.
* Apply the Principle of Least Privilege.
* Deploy a Web Application Firewall (WAF).

---

## 📖 Learning Outcomes

This project demonstrates practical experience in:

* Web Application Penetration Testing
* Information Gathering
* Vulnerability Assessment
* SQL Injection
* Cross-Site Scripting (XSS)
* Broken Access Control
* Sensitive Data Exposure
* Security Reporting
* Risk Analysis
* Secure Development Best Practices

---

## ⚠️ Disclaimer

This project was conducted **strictly for educational purposes** using the intentionally vulnerable **OWASP Juice Shop** application. No unauthorized systems were targeted.

---

## 📚 References

* OWASP Top 10
* OWASP Juice Shop Documentation
* NIST SP 800-53
* OWASP Testing Guide
