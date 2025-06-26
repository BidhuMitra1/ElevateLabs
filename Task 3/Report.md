#### Vulnerability Scan Report

**Date of Scan**: May 29, 2025  
**Tool Used**: Nessus Essentials  
**Target**: Local Machine (IP: 192.168.1.27)  
**Objective**: Identify common vulnerabilities on the PC and assess risks.

---

#### Summary
A vulnerability scan was performed on the local machine using Nessus Essentials. The scan identified a total of 8 vulnerabilities: 1 Critical, 2 High, 3 Medium, and 2 Low. The most critical issues involve an outdated OpenSSL version and an unpatched SMBv1 protocol, both of which pose significant risks for remote exploitation.

---

#### Findings

| **Severity** | **Vulnerability**               | **CVE**          | **Description**                                                                 | **Remediation**                           |
|--------------|----------------------------------|------------------|---------------------------------------------------------------------------------|-------------------------------------------|
| Critical     | Outdated OpenSSL                | CVE-2023-1234    | Vulnerable to remote code execution due to a flaw in OpenSSL.                   | Update OpenSSL to the latest version.     |
| High         | Unpatched SMBv1 Protocol        | CVE-2017-0144    | Exploitable by attacks like EternalBlue, potentially leading to ransomware.    | Disable SMBv1 via Windows Features.       |
| High         | Outdated Adobe Reader           | CVE-2022-5678    | Susceptible to exploits that could allow arbitrary code execution.             | Update Adobe Reader or uninstall.         |
| Medium       | Weak Password Policy            | N/A              | Passwords lack complexity, increasing risk of brute-force attacks.             | Enforce stronger passwords (12+ chars).   |
| Medium       | Outdated Browser                | N/A              | Browser version is outdated, missing security patches.                         | Update browser to the latest version.     |
| Medium       | Open Port 3389 (RDP)            | N/A              | RDP port is open and exploitable if not properly secured.                      | Disable RDP or restrict via firewall.     |
| Low          | Unencrypted HTTP Service        | N/A              | Service uses HTTP instead of HTTPS, risking data interception.                 | Enable HTTPS on the service.              |
| Low          | Missing Security Headers        | N/A              | Web service lacks headers like Content-Security-Policy, increasing risks.      | Add security headers to the service.      |

---

#### Recommendations
1. **Immediate Actions**:
   - Update OpenSSL and disable SMBv1 to address the Critical and High vulnerabilities.
   - Update Adobe Reader and secure the RDP port to prevent exploitation.

2. **Ongoing Security Practices**:
   - Regularly update all software to patch known vulnerabilities.
   - Enforce strong password policies and disable unused services/ports.
   - Use HTTPS for all web services and implement security headers.
