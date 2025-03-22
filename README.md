# Identifying and Remediating Vulnerabilities using Greenbone Enterprise Appliance

![Vulnerability Analysis](https://img.shields.io/badge/Analysis-Vulnerability%20Assessment-blue)
![Tools](https://img.shields.io/badge/Tools-Greenbone%20GVM%20%7C%20Metasploitable%202%20%7C%20VirtualBox-green)
![Platform](https://img.shields.io/badge/Platform-Kali%20Linux%20%7C%20Linux-orange)

## 📌 Project Overview
This project demonstrates the process of identifying and remediating vulnerabilities using **Greenbone Enterprise Appliance** to scan a vulnerable system, **Metasploitable 2 VM**, in a safe and controlled environment.

---

## 📁 Table of Contents
- [Tools and Technologies](#tools-and-technologies)
- [Objectives](#objectives)
- [Network Setup](#network-setup)
- [Scanning Process](#scanning-process)
- [Scan Results Summary](#scan-results-summary)
- [Remediation Recommendations](#remediation-recommendations)
- [Lessons Learned](#lessons-learned)
- [References](#references)
- [Author](#author)

---

## 🛠️ Tools and Technologies
- **Greenbone Enterprise Appliance (GVM/Greenbone Vulnerability Management)**
- **Metasploitable 2 VM** (Vulnerable target system)
- **VirtualBox** (VM Management)
- **Internal Network Configuration**

---

## 🎯 Objectives
- Configure a Greenbone Enterprise Appliance to scan a vulnerable target system.
- Identify vulnerabilities present on the Metasploitable 2 VM.
- Remediate the identified vulnerabilities by providing recommendations.

---

## 🌐 Network Setup
- Both VMs (Kali Linux and Metasploitable 2) are configured on an **Internal Network**.
<img src = https://github.com/elliotjonah/Identifying-and-Remediating-Vulnerabilities/blob/0e639d84a1d35e464068874b8929afc170fe98a0/Screenshot%202025-03-02%20233521.png>
<img src = https://github.com/elliotjonah/Identifying-and-Remediating-Vulnerabilities/blob/0e639d84a1d35e464068874b8929afc170fe98a0/Screenshot%202025-03-02%20233401.png>
- The Greenbone VM is accessible via its web interface.
- The Metasploitable 2 VM acts as the target for vulnerability scanning.


---

## 🔍 Scanning Process
1. **Install and configure OpenVas.**
sudo apt update && sudo apt upgrade -y
<img src = https://github.com/elliotjonah/Identifying-and-Remediating-Vulnerabilities/blob/0e639d84a1d35e464068874b8929afc170fe98a0/Screenshot%202025-03-19%20132336.png>
Install OpenVAS; apt-get install openvas
<img src = https://github.com/elliotjonah/Identifying-and-Remediating-Vulnerabilities/blob/0e639d84a1d35e464068874b8929afc170fe98a0/Screenshot%202025-03-19%20132650.png>
Start OpenVAS services; gvm-setup
<img src = https://github.com/elliotjonah/Identifying-and-Remediating-Vulnerabilities/blob/0e639d84a1d35e464068874b8929afc170fe98a0/Screenshot%202025-03-19%20132827.png>
<img src = https://github.com/elliotjonah/Identifying-and-Remediating-Vulnerabilities/blob/0e639d84a1d35e464068874b8929afc170fe98a0/Screenshot%202025-03-19%20132850.png>
Now that the setup is complete we have to check if everything is running correctly
gvm-check-setup
<img src = https://github.com/elliotjonah/Identifying-and-Remediating-Vulnerabilities/blob/0e639d84a1d35e464068874b8929afc170fe98a0/Screenshot%202025-03-19%20132939.png>
<img src = https://github.com/elliotjonah/Identifying-and-Remediating-Vulnerabilities/blob/0e639d84a1d35e464068874b8929afc170fe98a0/Screenshot%202025-03-19%20133009.png>
Access OpenVAS via web interface at https://127.0.0.1:9392/.
<img src = https://github.com/elliotjonah/Identifying-and-Remediating-Vulnerabilities/blob/0e639d84a1d35e464068874b8929afc170fe98a0/Screenshot%20(37).png>
<img src = https://github.com/elliotjonah/Identifying-and-Remediating-Vulnerabilities/blob/0e639d84a1d35e464068874b8929afc170fe98a0/Screenshot%20(39).png>
Click on advanced to continue and click on Accept the Risk and Continue
<img src = https://github.com/elliotjonah/Identifying-and-Remediating-Vulnerabilities/blob/0e639d84a1d35e464068874b8929afc170fe98a0/Screenshot%20(40).png>
 **Set up the target (Metasploitable 2 VM) for scanning.**
<img src = https://github.com/elliotjonah/Identifying-and-Remediating-Vulnerabilities/blob/0e639d84a1d35e464068874b8929afc170fe98a0/WhatsApp%20Image%202025-03-19%20at%2015.12.51_22252129.jpg>
 **Run a vulnerability scan on the target.**
<img src = https://github.com/elliotjonah/Identifying-and-Remediating-Vulnerabilities/blob/0e639d84a1d35e464068874b8929afc170fe98a0/WhatsApp%20Image%202025-03-19%20at%2015.12.51_8d891e7c.jpg>
7. **Review scan results to identify vulnerabilities.**

![Greenbone Scan Configuration](./images/scan-configuration.png)

---

## 📊 Scan Results Summary
The scan identified various vulnerabilities on the Metasploitable 2 VM, including:
- Outdated software versions.
- Open and vulnerable ports.
- Weak credentials.
- Vulnerable services (e.g., FTP, SSH, etc.).

![Scan Report Overview](./images/scan-report-overview.png)

For a detailed list of findings, refer to the attached [Scan Report](./scan-report.pdf).

---

## 🛡️ Remediation Recommendations
- **Update outdated software:** Ensure all services are running the latest stable versions.
- **Use strong credentials:** Replace weak passwords with strong, complex passwords.
- **Restrict unnecessary services:** Disable or restrict access to services that are not required.
- **Apply patches:** Regularly update systems with the latest security patches.

---

## 📖 Lessons Learned
- Proper network segmentation enhances security by limiting exposure to vulnerabilities.
- Regular vulnerability scans are essential to maintain a secure environment.
- Effective remediation involves not only patching but also improving configurations.

---

## 🔗 References
- [Greenbone Enterprise Appliance Documentation](https://www.greenbone.net)
- [Metasploitable 2 Vulnerabilities](https://github.com/rapid7/metasploitable)

---

## 👤 Author
Elliot Jonah

---
