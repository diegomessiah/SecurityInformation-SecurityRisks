# Chapter: Logs and SIEM tools

## 1. Introduction

As a security analyst, a critical responsibility is analyzing log data to mitigate and manage threats, risks, and vulnerabilities. Logs are records of events that occur within an organization's systems and networks. Security analysts access logs from various sources, which help in identifying potential threats.

Three common log sources are:

- Firewall Logs
- Network Logs
- Server Logs

Let’s explore each of these in more detail.

---

## 2. Common Log Sources

### 2.1 Firewall Logs

A **firewall log** is a record of attempted or established connections for incoming traffic from the internet. It also includes outbound requests from the network to external sources.

Example of a firewall log:

```plaintext
[2024-10-21 15:32:12] INBOUND TCP connection from 192.168.0.101:443 to 10.0.0.5:80
[2024-10-21 15:33:45] OUTBOUND TCP connection from 10.0.0.5:80 to 172.16.1.50:443
```

Firewall logs help track:

- Unusual or unauthorized access attempts
- Blocked or allowed connections

---

### 2.2 Network Logs

A **network log** is a record of all devices entering and leaving the network. It captures connections between devices and services.

Example of a network log:

```plaintext
[2024-10-21 15:35:22] DEVICE connected: MAC=00:1B:44:11:3A:B7, IP=10.0.0.5
[2024-10-21 15:37:58] DEVICE disconnected: MAC=00:1B:44:11:3A:B7, IP=10.0.0.5
```

Network logs help monitor:

- Device entry and exit
- Suspicious traffic patterns

---

### 2.3 Server Logs

A **server log** records events related to services such as websites, emails, or file shares. This includes actions like login attempts, password resets, and file requests.

Example of a server log:

```plaintext
[2024-10-21 15:40:01] LOGIN attempt: Username=admin, Status=Success
[2024-10-21 15:41:23] FILE accessed: File=/var/www/html/index.html, User=admin
```

Server logs help track:

- Successful and failed logins
- File or service access patterns

---

## 3. Monitoring and Analysis

By analyzing logs, security teams can detect vulnerabilities and potential data breaches. Logs are essential because **Security Information and Event Management (SIEM)** tools rely on them to monitor systems and detect threats in real-time.

---

## 4. SIEM Tools Overview

A **Security Information and Event Management (SIEM)** tool collects and analyzes log data to monitor critical activities across the organization. It provides:

- Real-time visibility
- Event monitoring and analysis
- Automated alerts for suspicious activities

### Example of SIEM Alert:

```json
{
  "timestamp": "2024-10-21T15:45:30Z",
  "alert": {
    "source": "Firewall",
    "message": "Unauthorized access attempt from IP 203.0.113.7",
    "severity": "High"
  }
}
```

SIEM tools centralize and streamline log analysis, making it easier to detect and address threats quickly.

---

## 5. Customization of SIEM Tools

While SIEM tools offer efficiency, they must be **configured** and **customized** to meet the unique security needs of an organization. As new threats emerge, security teams must continuously adapt and fine-tune SIEM rules to detect and mitigate new risks effectively.

---
