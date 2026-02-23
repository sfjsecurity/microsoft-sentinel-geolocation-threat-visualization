# Microsoft Sentinel Global Threat Mapping (Workbooks)

<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/ea357419-c343-4da3-8bc0-0388d0a721bd" />

This repository contains exported **Microsoft Sentinel Workbook JSON templates** used to create **world map visualizations** based on originating IP address.

These workbooks help visualize authentication activity, Azure resource changes, and malicious inbound traffic to support SOC monitoring and threat hunting.

---

## 📦 Included Workbooks


### Entra ID (Azure) Authentication Success | [Directory-Login-Successes.json](./Directory-Login-Successes.json)

<img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/402a5c31-80cc-4b3b-b65d-8d12c6d11cd8" />


###  Entra ID (Azure) Authentication Failures | [Directory-Login-Failures.json](./Directory-Login-Failures.json)

<img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/5af11cc7-f7e3-47d2-b6c1-c10c46d28e1a" />

###  Azure Resource Creation | [Azure-Resource-Creation.json](./Azure-Resource-Creation.json)

<img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/b99a800c-a424-42a5-9ce3-7c838f24f592" />

###  VM Authentication Failures | [VM-Authentication-Failures.json](./VM-Authentication-Failures.json)

<img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/94b13d86-c63c-46be-94db-6ea086b4692a" />


###  Malicious Traffic Entering the Network | [Allowed-Inbound-Malicious-Flows.json](./Allowed-Inbound-Malicious-Flows.json) 

<img width="300" height="300" alt="image" src="https://github.com/user-attachments/assets/af6cfd14-fcd1-44b2-8eee-a3a6176e6e06" />


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
