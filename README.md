# Wireshark Network Protocol Inspection

## Overview
This project involves inspecting various network protocols using Wireshark. The setup includes a Windows VM and a Linux VM running on Azure. The network traffic between these machines is captured and analyzed.

## Table of Contents
- [Setup](#setup)
- [Installing Wireshark](#installing-wireshark)
- [Capturing Network Traffic](#capturing-network-traffic)
- [Filtering Network Protocols](#filtering-network-protocols)
- [Blocking and Allowing Traffic](#blocking-and-allowing-traffic)
- [Observing Various Protocols](#observing-various-protocols)
- [Conclusion](#conclusion)

## Setup
1. **Created two virtual machines on Azure:**
   - **Windows VM**
   - **Linux VM**
     
   ![VM Setup](https://github.com/user-attachments/assets/770b3b68-42e1-42f8-b194-1653ccf684be)

## Installing Wireshark
1. **Downloaded and installed Wireshark** on the Windows VM.
   ![Wireshark Installation](https://github.com/user-attachments/assets/41acc126-196f-463a-9b25-38363b249638)
2. **Opened Wireshark and set up network interfaces** for packet capture.
   ![Network Interfaces](https://github.com/user-attachments/assets/c70621e2-f46e-4d2c-a1b7-499614a6b8c0)

## Capturing Network Traffic
- **Captured backend network traffic** including TCP, TLS, and ICMP packets.
  ![Traffic Capture](https://github.com/user-attachments/assets/ae42ac7e-15d6-4ce1-adff-f8369c18e8ef)

## Filtering Network Protocols
- **Applied filters** to analyze specific types of traffic such as ICMP, SSH, HTTP, and RDP.
  - **ICMP Traffic**: Used `icmp` filter to view ping requests and responses.
    ![ICMP Traffic](https://github.com/user-attachments/assets/5147f190-da46-4a55-9efe-b79d84ad31a8)
    ![Captured ICMP Traffic](https://github.com/user-attachments/assets/3a16536e-94be-445a-97d1-2990ec89b221)
    ![ICMP Filter](https://github.com/user-attachments/assets/60d37498-e2e8-4afb-8325-8431ed4e3c46)

## Blocking and Allowing Traffic
- **Created firewall rules on Azure** to block ICMP traffic to the Linux VM.
  ![Firewall Rules](https://github.com/user-attachments/assets/4cbf9bfd-9ff6-40b6-9475-62bb9f2df9f0)
  ![image](https://github.com/user-attachments/assets/65fa3a3d-9892-465a-89bb-ce63310a4b54)
![image](https://github.com/user-attachments/assets/ad273307-f751-428e-8f64-581514f69ffd)

  - **Verified blocked ICMP traffic.**
    ![Blocked ICMP Traffic](https://github.com/user-attachments/assets/e9bed013-e178-42bf-a0d5-8b51eee26f56)
  - **Deleted the firewall rule** to restore ICMP traffic.
    ![Restored ICMP Traffic](https://github.com/user-attachments/assets/10aa47be-88da-45f1-a67f-04876588e950)
  - **Confirmed that ICMP traffic was restored.**
![image](https://github.com/user-attachments/assets/6f9cfc91-1fc9-4789-b11f-8dcd439e6abb)


  - **SSH Traffic**: Used `ssh` filter to observe encrypted SSH sessions.
    ![SSH Traffic](https://github.com/user-attachments/assets/4e71af7c-d2fc-4197-a416-2b49f236fa09)
    ![Logged into Linux VM](https://github.com/user-attachments/assets/a12ee04d-4c0a-4588-ae64-e8ee3b36c29c)
    ![SSH Session](https://github.com/user-attachments/assets/5bea8ffe-2561-46ff-a8bd-e77ecb1edbc4)
    ![image](https://github.com/user-attachments/assets/8da36aa3-eace-482f-9e46-4b98fd195d83)

  - **HTTP/HTTPS Traffic**: Used `tcp.port == 443` to inspect HTTPS traffic.
    ![HTTPS Traffic](https://github.com/user-attachments/assets/339ba5e2-2313-4321-ae3a-e89324d22a14)
    ![Web Traffic](https://github.com/user-attachments/assets/575b9670-920b-40d1-b7ae-fc789bc5b73d)
  - **DNS Traffic**: Observed domain name resolutions using `dns` filter.
    ![DNS Traffic](https://github.com/user-attachments/assets/8a995d43-c1cc-4add-942c-0865d4278205)
  - **RDP Traffic**: Captured Remote Desktop Protocol sessions using `tcp.port == 3389`.
    ![RDP Traffic](https://github.com/user-attachments/assets/2e8155a2-cb61-48cd-9329-347124e6fa20)



## Conclusion
This project demonstrates how Wireshark can be used to analyze various network protocols, filter specific traffic types, and manage network security rules effectively. By leveraging Wireshark, administrators can:
- Monitor network traffic efficiently.
- Identify security vulnerabilities.
- Troubleshoot connectivity issues.
- Enforce network policies effectively.

This analysis provides a hands-on approach to understanding packet-level network operations and security implications.
