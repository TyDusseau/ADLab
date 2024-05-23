# Active Directory Home Lab

## Objective

In this Active Directory lab project, I aimed to develop a comprehensive understanding of key concepts by building an Active Directory infrastructure, implementing Splunk as a Security Information and Event Management (SIEM) system, and executing simulated attacks using Kali Linux. 

Through hands-on experience, I sought to master the intricacies of AD architecture, user management, and group policies while leveraging Splunk to analyze and respond to security events effectively. Additionally, by orchestrating attacks on a Windows host device via Kali Linux, I aimed to gain insights into common attack vectors and develop robust defensive strategies to fortify network defenses. Ultimately, the objective was to enhance my skills in both offensive and defensive cybersecurity practices within a controlled environment.

### Skills Learned

- Proficiency in building and configuring Active Directory infrastructure.
- Advanced knowledge of Active Directory architecture, including domain controllers, forests, and trusts.
- Experience in analyzing security events and responding to incidents within a SIEM environment.
- Ability to troubleshoot common AD issues, including authentication failures, replication problems, and DNS-related issues.

### Tools Used

- Active Directory Administrative Center (ADAC): Leveraged for advanced management tasks, including managing Active Directory domains, forests, trusts, and schema.
- Splunk Enterprise deployed as the core SIEM platform for ingesting, indexing, and analyzing log data from various sources, including Active Directory logs.
- Kali Linux crowbar tool to perform brute force attacks on Active Directory users.
- VirtualBox to create a network of virtual machines, allowing all attacks and defense to be done in a safe and controlled environment. 

## Steps

![Screenshot 2024-05-23 153743](https://github.com/TyDusseau/ADLab/assets/168771739/6fec9d21-9f9b-4ccf-8425-5db7e3a61212)

_Ref 1: Began installation and configuration of all four necessary VM's_

-----

![Screenshot 2024-05-23 154123](https://github.com/TyDusseau/ADLab/assets/168771739/d950b521-97bc-4818-922c-52b241ac3483)

_Ref 2: Sudo apt get/upgrade for Splunk server_

-----

![Screenshot 2024-05-23 155043](https://github.com/TyDusseau/ADLab/assets/168771739/100b2450-e0c6-4bb4-b930-d8cfa92a6d81)

_Ref 3: Assigned static IP and confirmed connectivity after adjusting network settings in VirtualBox_

-----

![Screenshot 2024-05-23 160233](https://github.com/TyDusseau/ADLab/assets/168771739/7a87d8db-975d-4b6b-9866-b776d0542b6d)

_Ref 4: Installed necessary plugins and configured Splunk to boot with proper user every time on startup_

-----

![Screenshot 2024-05-23 133242](https://github.com/TyDusseau/ADLab/assets/168771739/e5d0df41-8978-42f7-ad74-5d276e42bd86)

_Ref 5: Configured static IP for target system_

-----

![Screenshot 2024-05-23 161947](https://github.com/TyDusseau/ADLab/assets/168771739/9c6c2307-61ae-42a8-999a-291d89b3969a)

_Ref 6: Downloaded sysmon and Splunk Universal Forwarder, complete with all proper config files_ 

-----

![Screenshot 2024-05-23 162545](https://github.com/TyDusseau/ADLab/assets/168771739/054077e5-a4a6-4095-ace1-405d7f1b21f6)

_Ref 7: Restarted Splunk Universal Forwarder to apply new config file with proper endpoint_ 

-----

![Screenshot 2024-05-23 162839](https://github.com/TyDusseau/ADLab/assets/168771739/f33a6844-fb41-4caa-b350-1cd5c309dbee)

_Ref 8: Created Splunk endpoint on admin portal_

-----

![Screenshot 2024-05-23 162902](https://github.com/TyDusseau/ADLab/assets/168771739/6fffecc1-a9d3-4529-b976-311ff91e69f9)

_Ref 9: Configured the correct recieving port of 9997 on admin portal_

-----

![Screenshot 2024-05-23 162942](https://github.com/TyDusseau/ADLab/assets/168771739/1a8792e7-25f7-40f4-9fed-79447519f4c1)

_Ref 10: Verified connectivity of "TARGET-PC" with Splunk server_

-----

![Screenshot 2024-05-23 164433](https://github.com/TyDusseau/ADLab/assets/168771739/928d7626-dd36-43f5-b7c8-afcff524e129)

_Ref 11: Installed and configured ADDS_

-----

![Screenshot 2024-05-23 164943](https://github.com/TyDusseau/ADLab/assets/168771739/83b8ae30-8afb-4529-b2ba-22e05a1c515b)

_Ref 12: Added a new forest_ 

-----

![Screenshot 2024-05-23 165834](https://github.com/TyDusseau/ADLab/assets/168771739/fd1512d4-017d-4408-9f02-d76a0896be55)

_Ref 13: Created new orginizational units and added users_ 

-----

![Screenshot 2024-05-23 170431](https://github.com/TyDusseau/ADLab/assets/168771739/d0205c25-a701-4de2-9f85-a10bcb024ae9)

_Ref 14: Logged on the target pc and connected it to the active directory domain_

-----

![Screenshot 2024-05-23 171527](https://github.com/TyDusseau/ADLab/assets/168771739/ca963946-f8ce-4add-8587-cb5f5c5efda6)

_Ref 15: Began building my brute force attack through Kali Linux via the "crowbar" tool_

-----

![Screenshot 2024-05-23 171829](https://github.com/TyDusseau/ADLab/assets/168771739/1a51b994-42d9-4767-aa57-59d711e1a899)

_Ref 16: Enabled RDP on "TARGET-PC"_

-----

![Screenshot 2024-05-23 172002](https://github.com/TyDusseau/ADLab/assets/168771739/03f8c040-c63a-4031-bab3-5354c2685c51)

_Ref 17: RDP success_

-----

![Screenshot 2024-05-23 172118](https://github.com/TyDusseau/ADLab/assets/168771739/77364260-7124-40ac-931a-4b578b7594cf)

_Ref 18: Reviewed attack telemetry in Splunk_

-----

![Screenshot 2024-05-23 172142](https://github.com/TyDusseau/ADLab/assets/168771739/ac2f2fc4-fb58-4a15-83ba-d3d19cc48bba)

_Ref 19: Verified and "found the evil"_ 

-----

![Screenshot 2024-05-23 172203](https://github.com/TyDusseau/ADLab/assets/168771739/f6acb3f4-5ef8-4f5f-b5dd-068bbfec6f57)

_Ref 20: Found the attacking device_
