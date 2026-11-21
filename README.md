***🛡️ HYDRA-BASED BRUTE FORCE ATTACK DEMONSTRATION***


**📌 INTRODUCTION**

This project demonstrates an FTP Brute Force Attack using Hydra in a controlled and isolated lab environment.

The practical is performed using Kali Linux as the attacking machine and Metasploitable 2 as the target machine.

The main purpose of this project is to understand how brute force attacks work, how Hydra is used for password testing, and why strong password security is important.

---

**🛠️ TOOLS AND TECHNOLOGIES USED**

- Kali Linux – Attacking Machine
- Hydra – Brute Force Testing Tool
- Nmap – Network Scanning and Service Detection
- Metasploitable 2 – Vulnerable Target Machine
- FTP – File Transfer Protocol
- VMware – Virtualization Platform

---

**🎯 PROJECT OBJECTIVES**

- Understand the concept of Brute Force Attacks.
- Learn how to use the Hydra tool.
- Identify FTP services using Nmap.
- Perform FTP authentication security testing.
- Understand weak password vulnerabilities.
- Learn the importance of strong password security.

---

**🧪 LAB ENVIRONMENT**

Component| Details Attacker Machine| Kali Linux Target Machine| Metasploitable 2 Testing Tool| Hydra Scanning Tool| Nmap Target Service| FTP Default FTP Port| 21 Virtualization| VMware

-----
**📸 Hydra – Brute Force Attack Lab**

**1. Metasploitable 2 Target IP**

Information:

Metasploitable 2 is an intentionally vulnerable virtual machine used as a target system for cybersecurity practical exercises.

<img width="797" height="432" alt="Screenshot 2026-11-20 155646" src="https://github.com/user-attachments/assets/2ad98924-999a-4d72-b11c-800db56d00f6" />

Command:

**ifconfig**

Use:

- To identify the IP address of the target machine.
- To verify network configuration.
- To establish communication between Kali Linux and Metasploitable 2.

---
**2. Kali Linux Desktop**
   
Information:

Kali Linux is a Debian-based Linux distribution designed for penetration testing and security auditing.

<img width="1917" height="1025" alt="Screenshot 2026-11-21 234918" src="https://github.com/user-attachments/assets/fd698778-b522-4cad-bb4c-934ad00736f6" />


Tools Used:

- Kali Linux
- Hydra
- Nmap
- VMware Workstation
  
Use:

Kali Linux is used as the attacker machine to perform authorized security testing in the lab environment.

--- 

**3. Hydra Installation**

Information:

Hydra is a password-testing tool used to check login security by performing authorized login attempts against supported network services.

<img width="1141" height="463" alt="Screenshot 2026-11-22 000016" src="https://github.com/user-attachments/assets/72bbbf27-fb22-4428-8e5d-dac2ab15da5e" />

Command:

**sudo apt update sudo apt install hydra -y**

Verification Command:

**hydra -h**

Use:

- To install THC Hydra in Kali Linux.
- To verify successful installation.
- To view available Hydra options.

-----

**4. Nmap Service Detection**

Information:

Nmap is a network scanning tool used to discover open ports and identify running services on a target machine.

<img width="1046" height="907" alt="Screenshot 2026-11-22 000953" src="https://github.com/user-attachments/assets/b00b0e5e-453d-444e-9fba-9b42966f7127" />


Command:

**nmap -sV -p 21 <TARGET_IP>**

Use:

- To scan FTP port 21.
- To identify the FTP service.
- To detect the service version running on the target machine.

----

**5. Password File Creation**

Information:

A password list is a text file containing multiple password entries used for authorized password security testing.

<img width="915" height="875" alt="image" src="https://github.com/user-attachments/assets/99c9df5b-698c-48e8-a341-106d8b5d9c65" />



Command:

**nano yashpass.txt**

Use:

- To create a custom password list.
- To add password entries for lab testing.
- To prepare a password dictionary for Hydra.

---



**6. Password File Verification**


Information:

After creating the password file, it is important to verify its contents before using it in the testing process.


<img width="847" height="387" alt="image" src="https://github.com/user-attachments/assets/7511ae6d-db66-4b79-a61d-1038c5ca3da1" />


Command:

**cat yashpass.txt**

Use:

- To display the password list.
- To verify the file contents.
- To check the password list before testing.

  ----

  
 **7. FTP Service Result**

  
  Information:

FTP (File Transfer Protocol) is a network protocol used to transfer files between a client and a server.

Port 21 is the standard control port used by FTP.

<img width="1115" height="842" alt="image" src="https://github.com/user-attachments/assets/ecaf672c-4130-4df4-9446-8e9f46a9964c" />


Command:

**nmap -sV -p 21 <TARGET_IP>**

Use:

- To identify whether FTP service is running.
- To check the FTP service version.
- To confirm the target service before Hydra testing.


-----


**8. Hydra Final Testing**

Information:


Hydra is used to perform authorized password testing against the FTP service using a username and a custom password list.


<img width="1111" height="441" alt="image" src="https://github.com/user-attachments/assets/d1a7ac21-928c-4a88-9da6-9ee11a8b7a31" />



Command:

**hydra -l -P yashpass.txt ftp://<TARGET_IP> -t 4 -V**

Command Explanation:

"-l" : Specifies a single username.
"-P" : Specifies the password list file.
"ftp://" : Specifies the FTP service.
"-t 4" : Uses four parallel tasks.
"-V" : Displays each login attempt.

Use:

- To test FTP login security.
- To identify weak passwords in the authorized lab.
- To understand how brute-force attacks work.

----




**9. FTP Final Connection**

Information:

After identifying valid login credentials during authorized testing, an FTP connection can be established to verify the login.

<img width="777" height="416" alt="image" src="https://github.com/user-attachments/assets/4758dea6-d9e1-4ece-9191-8a1573b29be4" />



Command:

ftp <TARGET_IP>

Use:

- To connect to the FTP server.
- To verify the discovered credentials.
- To understand FTP authentication.

  ---

  
  **Security Recommendations**

- Use strong and complex passwords.
- Enable Multi-Factor Authentication (MFA).
- Implement login rate limiting.
- Monitor failed login attempts.
- Disable unused services.
- Use secure file transfer protocols such as SFTP.
- Regularly update systems and applications.

  ----

  
**Conclusion**


This project demonstrates how Hydra can be used for authorized FTP password security testing in a controlled lab environment.

It provides practical knowledge of Nmap scanning, FTP service detection, password list creation, and brute-force testing.

Project Environment: Kali Linux, Metasploitable 2, VMware Workstation

Tools Used: Hydra, Nmap, FTP 
🔐 SECURITY RECOMMENDATIONS

- Use Strong Passwords: Create long and complex passwords.
- Enable Multi-Factor Authentication: Add an extra layer of account security.
- Implement Login Rate Limiting: Restrict repeated login attempts.
- Monitor Failed Login Attempts: Regularly check authentication logs.
- Disable Unused Services: Reduce unnecessary network exposure.
- Use Secure Protocols: Prefer SFTP instead of FTP.


  ----


  
**📚 LEARNING OUTCOMES**

Through this project, I learned:

- Basic concepts of Brute Force Attacks.
- Installation and usage of Hydra.
- Network scanning using Nmap.
- FTP service identification and testing.
- Password security and authentication risks.
- Basic security measures against brute force attacks.

----



**⚠️ DISCLAIMER**

This project is created strictly for educational and cybersecurity learning purposes.

All testing was performed in an isolated lab environment using Metasploitable 2.

Unauthorized access or testing against systems without permission is strictly prohibited.


**👨‍💻 AUTHOR**

Yash Ganorkar

Cyber Security Enthusiast | Aspiring SOC Analyst













