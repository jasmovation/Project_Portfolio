# 🧠 Windows Server 2022 Active Directory Lab (VirtualBox)

### 📁 Project Overview
This project demonstrates a **fully functional on-prem Active Directory domain** built in Oracle VirtualBox, featuring a Windows Server 2022 Domain Controller and a Windows 10 Pro client joined to the domain.

The lab showcases fundamental **systems-integration and network-administration** skills, including DHCP, DNS, and Group Policy configuration.

---

### ⚙️ Environment Architecture

| Component | Role | OS | IP Address | Notes |
|------------|------|----|-------------|-------|
| **DC01** | Domain Controller / DNS / DHCP | Windows Server 2022 Standard | `192.168.10.10` | Hosts the domain **jasmovation.local** |
| **CLIENT01** | Domain Workstation | Windows 10 Pro 22H2 | `192.168.10.11` | Joined to **jasmovation.local** |
| **LABNET** | Internal VirtualBox Network | — | `192.168.10.0/24` | Isolated internal LAN |

---

### 🧩 Configuration Highlights
- **Active Directory Domain Services (AD DS)** promoted on DC01  
- **DHCP Scope:** `192.168.10.20 – 192.168.10.200`  
- **DNS:** Forward lookup zone `jasmovation.local` with dynamic updates  
- **Domain Join:** CLIENT01 → `jasmovation.local`  
- **Domain User:** `JASMOVATION\LabUser` (`[YourSecurePassword]`)  
- **Shared Folder:** `\\dc01\CompanyShare` (Domain Users granted Full Control)  
- **Group Policy Test:** Custom logon-message policy pushed to CLIENT01  

---

### 🧱 Skills Demonstrated
- Windows Server deployment and configuration  
- Active Directory user, computer, and policy management  
- DHCP/DNS role installation and troubleshooting  
- Domain join, authentication, and profile creation  
- VirtualBox network design (NAT vs Internal Network)  
- Snapshot management and environment backup  

---

### 🧰 Tools & Resources
- **Oracle VirtualBox 7.x**  
- **Windows Server 2022 ISO**  
- **Windows 10 22H2 ISO**  
- **PowerShell / CMD**  
- **Server Manager + DHCP / DNS / ADUC MMC tools**

---

### 🖼️ Suggested Screenshots
*(Replace with your actual images)*

1. Server Manager showing AD DS, DNS, DHCP roles  
2. DHCP scope `192.168.10.0/24` active  
3. CLIENT01 System → About → `client01.jasmovation.local`  
4. Successful “Welcome to jasmovation.local” domain-join message  
5. Shared folder `\\dc01\CompanyShare` opened from CLIENT01  

---

### 🧩 Future Enhancements
- Add Windows 11 client  
- Implement WSUS or a file server (FILE01)  
- Explore GPOs for security baselines  
- Automate setup with PowerShell scripts  

---

### 📜 Credits
Created by **Jasmine Lopez (Jasmovation)**  
Documentation & network build authored during the **2025 VirtualBox AD Lab series.**

---

### 🔒 Security & Data Notice
All IP addresses (e.g., `192.168.10.x`) and domain names (`jasmovation.local`) shown in this documentation are **private, non-routable network addresses** used exclusively for local lab demonstration.

No production systems, credentials, or personally identifiable information (PII) are included in this project.  
This environment was built and tested in an isolated **Oracle VirtualBox** network (LABNET) for educational and portfolio purposes only.
