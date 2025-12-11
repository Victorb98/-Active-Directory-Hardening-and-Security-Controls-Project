# 📌 Active Directory Hardening and Security Controls Project

## 🧠 Summary
This project is a hands-on breakdown of how to harden an Active Directory environment using real Windows Server configurations. I walked through password policies, NTLM authentication, LAN Manager hashing, SMB signing, tiered access controls, and domain structure.

The goal was simple: understand how attackers try to move in an AD environment and apply the right defensive controls to block them. Everything here reflects real blue-team and IAM work. Easy to follow and based on real configurations.

---

## ⚙️ Tools and Technologies Used
- Windows Server  
- Group Policy Management Console  
- Local Group Policy Editor  
- Active Directory Domains and Trusts  
- TryHackMe Active Directory Hardening Lab  
- Screenshot evidence from real configurations  

---

## 🗂️ Key Features and Findings

### LAN Manager and NTLM Security  
I inspected policies related to LAN Manager hash storage and NTLM authentication. LM hashes are outdated and weak, so preventing them from being stored is an important hardening step. I also reviewed NTLM fallback behaviour to avoid insecure authentication downgrades.

📸  
LM Hash Policy

<img width="1264" height="749" alt="Active Directory Hardening Answer 2 2" src="https://github.com/user-attachments/assets/05c578e1-aa49-4b9b-a701-c0eb9248c075" />

NTLM and Signing Policies

<img width="1266" height="780" alt="Active Directory Hardening Answer 2 1 " src="https://github.com/user-attachments/assets/6f5332b2-da92-49fb-a3a8-bd46b292c6f5" />


---

### SMB Signing  
I confirmed that both the Microsoft Network Client and Server are configured to digitally sign communications. Enabling SMB signing helps protect against man-in-the-middle attacks such as SMB relay.

📸  
 <img width="1266" height="780" alt="Active Directory Hardening Answer 2 1 " src="https://github.com/user-attachments/assets/ddbdf11c-4145-4e7c-bdd9-17356d895e22" />


---

### Tiered Access Model  
I reviewed the Tier 0, Tier 1, and Tier 2 models used in Active Directory environments.  
Tier 0 contains Domain Controllers and high-privilege admin groups.  
Tier 1 includes servers.  
Tier 2 includes end-user machines.

Printers and regular computers should not be placed in Tier 0, and temporary vendor accounts should not receive high privileges.

📸  
 <img width="1789" height="304" alt="Active Directory Hardening Questions 3-4" src="https://github.com/user-attachments/assets/7f82fe69-9787-4e86-bf82-814d4453dc15" />

 <img width="1781" height="305" alt="Active Directory Hardening Answer 3-4" src="https://github.com/user-attachments/assets/997f1a41-8f2a-42d0-9682-d459b1f5534d" />


---

### Password Policy  
I examined the environment’s password policy settings, which define password length, history, complexity, and maximum age. These help reduce brute-force and credential-based attacks.

📸  
 <img width="1198" height="631" alt="Active Directory Hardening Answer 2" src="https://github.com/user-attachments/assets/6d427621-0390-4113-8fc1-b14e59f098f8" />


---

### Domain Structure  
I identified the root domain of the Active Directory forest and checked trust relationships.  
The root domain for this environment is:

**tryhackme.loc**

📸  
 <img width="1331" height="612" alt="Active Directory Hardening Answer 1 " src="https://github.com/user-attachments/assets/dc8698ed-f186-4ace-8ed6-8cf873ac46c1" />

 <img width="1812" height="167" alt="Active Directory Hardening Question 1 " src="https://github.com/user-attachments/assets/1fa5c14a-f3fa-48d2-86b7-5c41ed6cfa29" />


---

# 🖼️ Image References
All included screenshots are listed below for clarity.
  <img width="1264" height="749" alt="Active Directory Hardening Answer 2 2" src="https://github.com/user-attachments/assets/4e021482-1bdf-40f6-8378-447a9ef5b207" />

  <img width="1266" height="780" alt="Active Directory Hardening Answer 2 1 " src="https://github.com/user-attachments/assets/42945f09-e0ad-4aab-be16-53ac78822ef5" />

  <img width="1789" height="304" alt="Active Directory Hardening Questions 3-4" src="https://github.com/user-attachments/assets/096a0454-b742-45eb-b268-227cd1876b4c" />

  <img width="1781" height="305" alt="Active Directory Hardening Answer 3-4" src="https://github.com/user-attachments/assets/4e5216b7-baea-438d-b7e4-5476b6592663" />
  
<img width="1198" height="631" alt="Active Directory Hardening Answer 2" src="https://github.com/user-attachments/assets/67a35081-a532-4c16-923c-5fcf78660d8e" />

  <img width="1823" height="171" alt="Active Directory Hardening Question 2" src="https://github.com/user-attachments/assets/1ce9519e-a34c-4a90-a9e8-5905456d7edb" />

 <img width="1331" height="612" alt="Active Directory Hardening Answer 1 " src="https://github.com/user-attachments/assets/523efca4-16b0-4d48-bbe4-7b0ef3a5fd7a" />

 <img width="1812" height="167" alt="Active Directory Hardening Question 1 " src="https://github.com/user-attachments/assets/a20dcda0-698a-4974-bb3a-e17b5525f3b9" />


---

# 🚀 What This Project Shows
This project demonstrates that I can  
Evaluate an AD environment  
Identify weak or risky configurations  
Apply Microsoft best practices  
Understand authentication and privilege boundaries  
Document findings clearly and professionally  

These reflect real skills used by SOC analysts, IAM engineers, and blue-team defenders in enterprise environments.

---

# 📚 Resources
Microsoft Tiered Access Model  
Microsoft AD Security Best Practices  
TryHackMe Active Directory Hardening  
MITRE ATT&CK Framework  

---

# 🙌 Acknowledgements
Thanks to TryHackMe for the lab and Microsoft for their documentation.
