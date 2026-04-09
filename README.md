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

# ⚙️ 1. Active Directory Domain Setup

![Domain Overview](localdomain.png)

This shows the Active Directory environment after setting up the domain **Eric.local**.  
I configured Organizational Units (OUs) to represent different locations and departments, forming the foundation of the domain structure.

---

# 👥 2. Bulk User Creation (PowerShell)

![User Creation Script](CreateUsers.png)

To simulate a real enterprise environment, I created a PowerShell script that automatically generates **500 users**.

Each user is:
- Assigned a unique username  
- Placed into a specific Organizational Unit  
- Added to a department-based security group (IT, HR, Sales, Engineering, Marketing, Accounting)  

---

![Users Created Successfully](userssuccessful.png)

This output confirms that all users were successfully created and distributed across multiple OUs and groups.

---

# 🔐 3. Group Policy Configuration

![Group Policy Management](grouppolicies.png)

Group Policy Objects (GPOs) were created to enforce security and system configurations across the domain.

This allows centralized control of:
- User behavior  
- System settings  
- Security policies  

---

# 🌐 4. Static IP Configuration (Domain Controller)

![Static IP Configuration](staticIP.png)

A static IP address was configured on the domain controller to ensure consistent communication across the network.

This is critical because:
- Domain Controllers must not rely on DHCP  
- DNS must consistently point to the domain controller  

---

![Static IP Verification](staticsuccess.png)

This confirms that the static IP was successfully applied and DHCP was disabled.

---

# 🔍 5. Network Connectivity Test

![Ping Domain Controller](pingdomain.png)

After configuring networking, I verified connectivity by pinging the domain controller from the client machine.

This ensured:
- Both machines are on the same network  
- Communication between systems is working  

---

# 🖥️ 6. Domain Join (Client Machine)

![Domain Join Successful](domainjoin.png)

After configuring DNS correctly, the Windows 11 client machine was successfully joined to the **Eric.local domain**.

This demonstrates:
- Proper DNS configuration  
- Successful domain communication  
- Integration of client into Active Directory  

---

# 🔑 7. Password Policy Enforcement

![Password Policy](passwordpolicy.png)

A Group Policy was created to enforce password requirements across the domain.

---

![Password Change Prompt](localdomain.png)

When attempting to log in, the system required a password change, confirming that the Group Policy was successfully applied.

---

# 📂 8. File Permissions Configuration

![File Permissions](fileprops.png)

A shared folder was created on the server and configured with NTFS permissions based on security groups.

This ensures:
- Role-based access control (RBAC)  
- Secure access to shared resources  

---

# 🔗 9. Network Drive Mapping

![Mapped Drive](filemap.png)

The shared folder was mapped as a network drive on the client machine.

This demonstrates:
- Centralized file access  
- Real-world enterprise file server setup  

---

# 🧠 Key Skills Demonstrated

- Active Directory administration  
- PowerShell automation  
- Network configuration (IP & DNS)  
- Domain environment setup  
- Group Policy management  
- Access control and file permissions  
- Troubleshooting connectivity and authentication  

---

# 🚀 Summary

This project simulates a real-world enterprise IT environment by combining networking, system administration, and security concepts.

Through this lab, I gained hands-on experience in:
- Managing domain infrastructure  
- Automating administrative tasks  
- Enforcing security policies  
- Configuring enterprise network services  
