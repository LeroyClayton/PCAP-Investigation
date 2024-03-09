# PCAP Investigation

## Objective

  The objective of this GitHub project is to document and share the findings of a Packet Capture (PCAP) investigation conducted on network traffic. Through meticulous analysis of captured network packets, the project aims to uncover potential security vulnerabilities, anomalous activities, or performance issues within the network infrastructure. By providing detailed insights into network communication patterns, protocols, and potential threats, this project seeks to contribute to the enhancement of network security practices and aid in the understanding of network behavior for researchers, cybersecurity professionals, and network administrators.

### Skills Learned

- Packet Analysis
- Traffic Pattern Recognition
- Traffic Visualization
- Network Forensics
- Data Filtering and Extraction


### Tools Used

- Network Protocol Analyzer (WireShark)

### Scenario

![PCAP Scenario](https://github.com/LeroyClayton/PCAP-Investigation/assets/118240301/395dbdaf-cb4d-418c-b0c6-a242fc09be33)

 TIP! If you're having difficulties seeing the image, right-click it and open it in another tab to get a clearer view.
## Steps
**Step 1:** installing Wireshark


![Wireshark Install](https://github.com/LeroyClayton/PCAP-Investigation/assets/118240301/a640ecc7-8231-4b3a-9ed3-b6051c36c1c7)

**Step 2:** Opening malicious file in Wireshark


![Opening File In Wireshark](https://github.com/LeroyClayton/PCAP-Investigation/assets/118240301/9412a0a1-2bea-44d1-9067-281463bd01e0)


**Step 3:** SSH, DNS, HTTP, and SMB present ample avenues for lateral movement opportunities.



![SSH, DNS, HTTP, SMB Later Movement Oppertunity](https://github.com/LeroyClayton/PCAP-Investigation/assets/118240301/cf5f477f-ea47-485d-8478-c57849614a62)


**Step 4:** Port 4422 suggests potential utilization by an active program

![A program may be inuse ](https://github.com/LeroyClayton/PCAP-Investigation/assets/118240301/72a8621a-c1fd-449e-87ae-ba3b996e0413)


**Step 5:** An unusual byte size observed on port 80 indicates potential anomalies or irregularities. 

![Unsual Byte Size For Port 80](https://github.com/LeroyClayton/PCAP-Investigation/assets/118240301/0cf21936-c1c6-44a8-bf6d-1c710980cfb4)



**Step 6:** A user gained access using username:admin Password:Password
![User login with admin password](https://github.com/LeroyClayton/PCAP-Investigation/assets/118240301/22e526bb-655b-4466-a6b0-251fc0a2bad7)



**Step 7:** Adding a source and destination port column for organization.
![Adding Source And Destination Port For Organization](https://github.com/LeroyClayton/PCAP-Investigation/assets/118240301/a166b18c-7b27-471f-8e34-be762226d25a)



**Step 8:** Ports 22 and 80 are most likely open.

![Port 22 Is Open](https://github.com/LeroyClayton/PCAP-Investigation/assets/118240301/217d2c2f-a7fe-40e8-adff-e467d812c4b2)

![Port 80 Is Open](https://github.com/LeroyClayton/PCAP-Investigation/assets/118240301/232e7e1a-4044-489f-a696-4e44d4d560ad)


**Step 9:** Scan ends at 2165


![Scan Ends 2165](https://github.com/LeroyClayton/PCAP-Investigation/assets/118240301/6a47e0db-4115-4063-8f44-ec36ff92f665)


**Step 10:** Take note of the user agent.

![User Agent Mozilla ](https://github.com/LeroyClayton/PCAP-Investigation/assets/118240301/43a589bc-320e-4eae-af0a-6f69f6bdacbd)



**Step 11:** Take notice of the user agent. Gobuster is a software program for brute-forcing directories on web servers. It is not preloaded with Kali Linux.

![Gobuster Used Not Good ](https://github.com/LeroyClayton/PCAP-Investigation/assets/118240301/4de4bf6d-3353-4065-a07d-302fe6a99ef7)


**Step 12:** Crafting display filters to find good stuff.

![Crafting Display Filters To Find The Good Stuff](https://github.com/LeroyClayton/PCAP-Investigation/assets/118240301/2fa7be49-d548-4e28-bb68-a5f9ba2e2d66)


**Step 13:** Gobuster finished at 16:34:06.

![Gobuster Finished At Time 16'34'06](https://github.com/LeroyClayton/PCAP-Investigation/assets/118240301/5d019c76-f464-4c27-ab50-0539855b11d6)

**Step 14:** A upload was found to the directory.

![Upload Directory was found](https://github.com/LeroyClayton/PCAP-Investigation/assets/118240301/b03331d6-2c21-4776-ab5b-8065faa0e883)

**Step 15:** A SQL map was used (Sqlmap is a software utility for automated discovering of SQL injection vulnerabilities in web applicatons.)

![SQL Map Was Used Not Good 16'36'17](https://github.com/LeroyClayton/PCAP-Investigation/assets/118240301/7808fe61-d03b-4264-a39a-966e9cd0a586)


**Step 16:** Making Use of a URL Decoder I discovered that there had been an attempt to access a passwords folder.

![Using A Decoder Found This](https://github.com/LeroyClayton/PCAP-Investigation/assets/118240301/859c0457-b00e-48b1-b693-6210088e1593)


**Step 17:** The attacker used the edit profile button to upload a file.

![Attacker Uploaded File Through Edit Profile](https://github.com/LeroyClayton/PCAP-Investigation/assets/118240301/f0ae9e8a-3114-4e39-b4e3-df7b208ca369)

**Step 18:** The upload shows submitted.


![Upload was sumbitted](https://github.com/LeroyClayton/PCAP-Investigation/assets/118240301/33fbfb26-fbfa-435b-bb82-b2b8f9a7ea7e)

### Summary

It's clear from looking at a PCAP file that the attacker used SQL injection techniques to get around security and read a password file without authorization. The infected file was then uploaded by the intruder, so endangering the system's sensitive data's confidentiality and integrity.

