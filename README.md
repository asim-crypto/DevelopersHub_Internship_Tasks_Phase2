# DevelopersHub_Internship_Tasks_Phase2
# DevelopersHub Cybersecurity Internship: Phase-2 (Advanced Security)

## Overview
This repository contains the advanced security implementations and penetration testing reports completed during Phase-2 (Weeks 4-6) of the DevelopersHub Corporation cybersecurity internship program. The focus of this phase was to transition from basic vulnerability patching to proactive threat detection, ethical hacking, and secure production deployment.

## Technologies & Tools 
* **Backend:** Node.js, Express.js
* **Security Middleware:** `express-rate-limit`, `csurf`, `helmet`
* **Threat Detection & WAF:** Fail2Ban, OSSEC
* **Penetration Testing:** Kali Linux, SQLMap, Burp Suite, Metasploit
* **Auditing & Deployment:** OWASP ZAP, Nikto, Lynis, Docker

## Project Roadmap

### Week 4: Advanced Threat Detection & API Hardening
* **Intrusion Detection:** Configured Fail2Ban to monitor server logs and automatically ban IP addresses exhibiting malicious behavior (e.g., brute-force login attempts).
* **API Security:** Deployed `express-rate-limit` to strictly control endpoint request volumes.
* **Header Enforcements:** Upgraded security headers to include a strict Content Security Policy (CSP) and HTTP Strict-Transport-Security (HSTS) to force encrypted transmission.

### Week 5: Ethical Hacking & Vulnerability Exploitation
* **SQL Injection (SQLi):** Conducted active reconnaissance and used SQLMap to identify injection vectors. Remediated the vulnerabilities by entirely refactoring database queries to utilize secure, prepared statements.
* **Cross-Site Request Forgery (CSRF):** Simulated CSRF attacks against state-changing endpoints using Burp Suite. Mitigated the flaw by integrating anti-CSRF token validation via the `csurf` middleware.

### Week 6: Security Audits & Secure Deployment
* **Compliance Auditing:** Ran comprehensive scans using OWASP ZAP, Nikto, and Lynis to ensure the application met OWASP Top 10 compliance standards.
* **Container Security:** Deployed the application using Docker, enforcing least-privilege non-root execution and conducting image vulnerability scans.
* **Zero Trust & WAF (Bonus):** Implemented baseline Zero Trust access controls and routed traffic through a Web Application Firewall (WAF) to filter malicious payloads before they hit the application layer.

## Installation and Setup
1. Clone this repository to your local machine.
2. Run `npm install` to install all hardened dependencies.
3. Ensure Docker is installed, and run `docker-compose up --build` to launch the secure containerized environment.
4. Access the application at `http://localhost:3000`.
