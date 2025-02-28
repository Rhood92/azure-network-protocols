# Wireshark Network Protocol Inspection

**Author:** [Your Name]  
**Date:** [Date]  
**Category:** Network Security & Threat Analysis  

---

## 🛠️ Scenario Overview
This project involves inspecting various network protocols using Wireshark. The setup includes a **Windows VM** and a **Linux VM** running on Azure. The network traffic between these machines is captured and analyzed to observe protocol behaviors and security implications.

### 🔍 **Hypothesis**
- Analyzing network traffic with Wireshark will reveal insights into various communication protocols.
- Applying filters will allow targeted inspection of traffic, including ICMP, SSH, HTTP, DNS, and RDP.
- Firewall rules can be modified to control network behavior effectively.

---

## 📊 Data Collection

### 📝 **Setup: Creating Virtual Machines**
- **Windows VM** and **Linux VM** created on Azure.
  
  ![VM Setup](https://github.com/user-attachments/assets/770b3b68-42e1-42f8-b194-1653ccf684be)

### 📝 **Installing Wireshark**
- **Downloaded and installed Wireshark** on the Windows VM.
  
  ![Wireshark Installation](https://github.com/user-attachments/assets/41acc126-196f-463a-9b25-38363b249638)
- **Configured network interfaces** for packet capture.
  
  ![Network Interfaces](https://github.com/user-attachments/assets/c70621e2-f46e-4d2c-a1b7-499614a6b8c0)

---

## 🚀 Data Analysis

### 📝 **Capturing Network Traffic**
- Captured **backend network traffic**, including **TCP, TLS, and ICMP packets**.
  
  ![Traffic Capture](https://github.com/user-attachments/assets/ae42ac7e-15d6-4ce1-adff-f8369c18e8ef)

### 📝 **Filtering Network Protocols**

#### 🔹 **ICMP Traffic**
- Applied `icmp` filter to view ping requests and responses.
  
  ![ICMP Traffic](https://github.com/user-attachments/assets/5147f190-da46-4a55-9efe-b79d84ad31a8)
  ![image](https://github.com/user-attachments/assets/a0449cac-a28d-47cd-8eaa-03bece931d9c)
  ![image](https://github.com/user-attachments/assets/9d00d673-6473-4e6c-97f2-b2e456684d95)


  
#### 🔹 **SSH Traffic**
- Used `ssh` filter to observe encrypted SSH sessions.
  
  ![SSH Traffic](https://github.com/user-attachments/assets/4e71af7c-d2fc-4197-a416-2b49f236fa09)
  ![image](https://github.com/user-attachments/assets/1f53c45b-c0e4-4274-8a03-654b2072e51e)
  ![image](https://github.com/user-attachments/assets/2d5caaaf-e34c-4020-b159-fdedce77afe1)
  ![image](https://github.com/user-attachments/assets/fa60351a-9f44-4c3d-9755-af120d3b781f)

#### 🔹 **HTTP/HTTPS Traffic**
- Applied `tcp.port == 443` filter to analyze secure web traffic.
  
  ![HTTPS Traffic](https://github.com/user-attachments/assets/339ba5e2-2313-4321-ae3a-e89324d22a14)
  ![image](https://github.com/user-attachments/assets/193cfd26-b8c9-466d-a004-5a1f0ebdd834)

#### 🔹 **DNS Traffic**
- Used `dns` filter to analyze domain name resolution.
  
  ![DNS Traffic](https://github.com/user-attachments/assets/8a995d43-c1cc-4add-942c-0865d4278205)

#### 🔹 **RDP Traffic**
- Captured Remote Desktop Protocol (RDP) sessions using `tcp.port == 3389`.
  
  ![RDP Traffic](https://github.com/user-attachments/assets/2e8155a2-cb61-48cd-9329-347124e6fa20)

---

## 🛡️ Blocking and Allowing Traffic

### 📝 **Firewall Rule Implementation**

#### 🔹 **Blocking ICMP Traffic**
- **Created firewall rules** on Azure to block ICMP traffic to the Linux VM.
  
  ![Firewall Rules](https://github.com/user-attachments/assets/4cbf9bfd-9ff6-40b6-9475-62bb9f2df9f0)
  ![image](https://github.com/user-attachments/assets/80ce5bfd-0615-4c64-b033-fb645222f23f)
  ![image](https://github.com/user-attachments/assets/7a56f7e1-e2cc-4f0c-b45d-388091b61396)

- **Verified that ICMP traffic was blocked.**
  
  ![Blocked ICMP Traffic](https://github.com/user-attachments/assets/e9bed013-e178-42bf-a0d5-8b51eee26f56)
  ![image](https://github.com/user-attachments/assets/f38ab521-eeda-4496-aa62-68d37cce7443)
  ![image](https://github.com/user-attachments/assets/b8f38a48-ce94-480a-a5a9-adfbef4e167b)


#### 🔹 **Restoring ICMP Traffic**
- **Deleted firewall rule** to allow ICMP traffic again.
  
  ![Restored ICMP Traffic](https://github.com/user-attachments/assets/10aa47be-88da-45f1-a67f-04876588e950)
- **Confirmed successful ICMP traffic restoration.**

---

## 📚 Areas for Improvement

### 🔹 **Network Security Enhancements**
- Implement **Network Security Groups (NSGs)** for more granular traffic control.
- Apply **Just-In-Time (JIT) access** for sensitive management ports.
- Strengthen firewall policies to prevent unauthorized access.

### 🔹 **Threat Analysis Enhancements**
- Use **Wireshark custom rules** to detect anomalies.
- Automate traffic logging for real-time network monitoring.

---

## 📖 Final Summary
✅ Successfully captured and analyzed **multiple network protocols** using Wireshark.  
✅ Applied **protocol-specific filters** to inspect targeted traffic types.  
✅ Implemented **firewall rules** to block and allow traffic dynamically.  
✅ Demonstrated **network security monitoring** using real-world scenarios.  

🔐 **Next Steps:** Enhance **Wireshark capabilities**, strengthen **network security policies**, and integrate **automated alerts** for suspicious traffic.  

---

### 📌 **Repository Information**

💡 This project is designed for **educational & security research purposes**. If you're interested in **network security, protocol analysis, or Wireshark**, feel free to explore and contribute!  

📁 _Repo: [GitHub Link]_  
📬 _Contact: [Your Contact]_
