# Microsoft Sentinel Global Threat Mapping (Workbooks)

<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/ea357419-c343-4da3-8bc0-0388d0a721bd" />

This repository contains exported **Microsoft Sentinel Workbook JSON templates** used to create **world map visualizations** based on originating IP address.

These workbooks help visualize authentication activity, Azure resource changes, and malicious inbound traffic to support SOC monitoring and threat hunting.

---

## 📦 Included Workbooks

| Scenario | File |
|---------|------|
| Entra ID (Azure) Authentication Success | [Directory-Login-Successes.json](./Directory-Login-Successes.json) |
| Entra ID (Azure) Authentication Failures | [Directory-Login-Failures.json](./Directory-Login-Failures.json) |
| Azure Resource Creation | [Azure-Resource-Creation.json](./Azure-Resource-Creation.json) |
| VM Authentication Failures | [VM-Authentication-Failures.json](./VM-Authentication-Failures.json) |
| Malicious Traffic Entering the Network | [Allowed-Inbound-Malicious-Flows.json](./Allowed-Inbound-Malicious-Flows.json) |

---

## 🛠️ How to Import These Workbooks into Sentinel

1. Open **Microsoft Sentinel**
2. Go to **Workbooks**
3. Click **+ Add workbook**
4. Click **Edit**
5. Click the **</> (Advanced Editor)** button
6. Replace the existing JSON with the contents of one of the files in this repo
7. Click **Apply**
8. Click **Save** and name the workbook

---

## ✅ Log Sources Used (Varies by Workbook)

- Entra ID Sign-in Logs (**SigninLogs**)
- Azure Activity Logs (**AzureActivity**)
- VM logs (e.g., **SecurityEvent** / **Syslog** depending on configuration)
- Network / NSG flow logs (depending on setup)
- Threat Intelligence (optional enrichment)

---

## 🎯 Use Case

These geographic visualizations help identify:

- Suspicious authentication locations
- Brute force / password spraying clusters
- Unauthorized Azure resource creation regions
- VM access abuse attempts
- Global distribution of inbound malicious traffic
