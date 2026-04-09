# 🏢 Active Directory Home Lab Project

## 📌 Overview
This project demonstrates the implementation of a **Windows Active Directory environment** using virtual machines. The lab simulates a real-world enterprise setup where a domain controller manages users, groups, policies, and network resources.

This project covers:
- Active Directory Domain Services (AD DS)
- Bulk user creation using PowerShell
- Organizational Units (OUs) and Security Groups
- Group Policy Objects (GPOs)
- Static IP and DNS configuration
- Domain joining (client to server)
- Network drive mapping and file permissions

---

## 🛠️ Technologies Used
- VMware Workstation Pro  
- Windows Server 2022 (Domain Controller)  
- Windows 11 Enterprise (Client Machine)  
- PowerShell  

---

# ⚙️ 1. Active Directory Setup & Bulk User Creation

![User Creation Script](CreateUsers.png)

I configured Active Directory Domain Services and created the domain **Eric.local**.  
To simulate a real enterprise environment, I used a PowerShell script to automate the creation of **500 users**.

Each user was:
- Assigned a unique username  
- Placed into the correct Organizational Unit (Louisville, Detroit, Chicago, Iowa)  
- Added to a department-based security group (IT, HR, Sales, Engineering, Marketing, Accounting)  

---

![Users Created Successfully](userssuccessful.png)

This output confirms that users were successfully created and distributed across multiple OUs and groups, replicating a real-world onboarding process.

---

# 🌐 2. Static IP & DNS Configuration

![Static IP Configuration](staticIP.png)

I configured a **static IP address** on the domain controller to ensure consistent communication within the network.

This step is critical because:
- Domain Controllers must not rely on DHCP  
- DNS must consistently point to the domain controller  

---

![Static IP Verification](staticsuccess.png)

This confirms the static IP was successfully applied and DHCP was disabled.

---

# 🔍 3. Network Connectivity & DNS Validation

![Ping Domain Controller](pingdomain.png)

After configuring networking, I verified connectivity by pinging the domain controller.

This ensured:
- Both virtual machines were on the same network  
- The client could reach the domain controller  

---

# 🖥️ 4. Domain Join (Client Machine)

![Domain Join Successful](domainjoin.png)

After configuring DNS correctly (pointing to the domain controller), I joined the Windows 11 client machine to the **Eric.local domain**.

This step demonstrates:
- Proper DNS dependency for Active Directory  
- Successful communication between client and domain controller  

---

# 🔐 5. Group Policy Configuration

![Group Policy Management](grouppolicies.png)

I created and configured Group Policy Objects (GPOs) to enforce security settings across the domain.

---

![Password Policy](passwordpolicy.png)

A password policy was implemented to require users to change their password at first login.

---

![Password Change Prompt](localdomain.png)

When logging into the client machine, the system enforced the Group Policy by requiring a password update, confirming the policy was successfully applied.

---

# 📂 6. File Sharing & Permissions

![File Permissions](fileprops.png)

I created a shared folder on the server and configured NTFS permissions based on security groups.

This ensures:
- Only authorized users can access specific resources  
- Access is controlled using group-based permissions (RBAC)  

---

# 🔗 7. Network Drive Mapping

![Mapped Drive](filemap.png)

The shared folder was mapped as a network drive on the client machine.

This demonstrates:
- Centralized file access  
- Real-world enterprise file server configuration  

---

# 🧠 Key Skills Demonstrated

- Active Directory administration  
- PowerShell automation  
- Network configuration (IP, DNS)  
- Domain environment setup  
- Group Policy management  
- Access control and file permissions  
- Troubleshooting connectivity and authentication issues  

---

# 🚀 Summary

This project simulates a real-world enterprise environment by combining networking, system administration, and security concepts. It demonstrates how users, devices, and policies interact within an Active Directory domain.

Through this lab, I gained hands-on experience in:
- Managing domain infrastructure  
- Automating administrative tasks  
- Enforcing security policies  
- Configuring enterprise network services  

---
