# 🔍 Basic Vulnerability Scan Using Nessus Essentials

## 📌 Task Overview

This project was completed as part of **Task 3: Perform a Basic Vulnerability Scan on Your PC**. The objective was to identify common security vulnerabilities using a free vulnerability scanning tool.

---

## 🛠 Tools Used

- **Nessus Essentials (Free Version)**
  - Website: [https://www.tenable.com/products/nessus/nessus-essentials](https://www.tenable.com/products/nessus/nessus-essentials)

---

## 🧪 Scan Configuration

- **Scan Tool**: Nessus Essentials
- **Scan Target**: 192.168.29.41
- **Scan Type**: Basic Network Scan
- **Scan Duration**: Approx. 15 minutes
- **Environment**: Windows 11

---

## 📊 Results Summary

| Severity | Count |
|----------|-------|
| Critical | X     |
| High     | X     |
| Medium   | 2     |
| Low      | X     |
| Info     | 60     |

## 🚨 Notable Vulnerabilities

### 1. [SSL Certificate Cannot Be Trusted]
- **Severity**: Medium
- **Description**: The server's X.509 certificate cannot be trusted. This situation can occur in three different ways, in which the chain of trust can be broken, as stated below :

- First, the top of the certificate chain sent by the server might not be descended from a known public certificate authority. This can occur either when the top of the chain is an unrecognized, self-signed certificate, or when intermediate certificates are missing that would connect the top of the certificate chain to a known public certificate authority.

- Second, the certificate chain may contain a certificate that is not valid at the time of the scan. This can occur either when the scan occurs before one of the certificate's 'notBefore' dates, or after one of the certificate's 'notAfter' dates.

- Third, the certificate chain may contain a signature that either didn't match the certificate's information or could not be verified. Bad signatures can be fixed by getting the certificate with the bad signature to be re-signed by its issuer. Signatures that could not be verified are the result of the certificate's issuer using a signing algorithm that Nessus either does not support or does not recognize.

If the remote host is a public host in production, any break in the chain makes it more difficult for users to verify the authenticity and identity of the web server. This could make it easier to carry out man-in-the-middle attacks against the remote host.

### 2. [SMB Signing not required]
- **Severity**: Medium
- **Description**: Signing is not required on the remote SMB server. An unauthenticated, remote attacker can exploit this to conduct man-in-the-middle attacks against the SMB server.
## 🛡️ Mitigation Steps Taken

- Updated vulnerable software
- Disabled unused ports and services
- Applied system updates and patches
- Configured firewall rules to restrict access

---

## 🖼️ Screenshots

Screenshots of the scan results are available in the `screenshots/` folder:
- `dashboard.png`
- `critical_issue.png`
- `scan_summary.png`

---

## 📁 Project Structure

