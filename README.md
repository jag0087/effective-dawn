# effective-dawn

Title:
Building a NIST SP 800-53 Cybersecurity Framework Laboratory Environment

Author:
John Gardner - jag0087

**Independent Cybersecurity Research Lab**

Date:
3 October 2025

__Abstract__  
This project establishes a virtualized cybersecurity laboratory built to align with the National Institute of Standards and Technology (NIST) Special Publication 800-53 Rev. 5 security controls and the Risk Management Framework (RMF). The goal of the lab is to simulate a small but realistic enterprise environment to demonstrate the implementation and documentation of key NIST control families, including Access Control (AC), Identification and Authentication (IA), Configuration Management (CM), Audit and Accountability (AU), and Incident Response (IR).  
The environment consists of both Windows and Linux systems deployed within VMware Workstation on a local workstation. Each component will serve as evidence of security control implementation, supported by documentation artifacts such as a System Security Plan (SSP), a Plan of Action and Milestones (POA&M), and Request for Information (RFI) response examples. The project aims to provide practical experience with control documentation, system hardening, and audit evidence collection.
<br><br>

**Introduction**  
The National Institute of Standards and Technology (NIST) provides a series of frameworks and publications that form the foundation for information security governance within both public and private sector organizations. Among these, NIST SP 800-53 Rev. 5 outlines a comprehensive catalog of security and privacy controls used to protect information systems.  
The objective of this project is to design and deploy a controlled virtual environment that allows for the practical implementation and documentation of selected NIST SP 800-53 controls. This laboratory will replicate common enterprise infrastructure components. Components such as a domain controller, client systems, servers, and logging mechanisms, while maintaining manageability on a single workstation.

By the end of this project, the environment will enable the user to:  
Understand the intent and application of NIST SP 800-53 controls.  
Implement technical measures that satisfy control requirements.  
Collect verifiable evidence to support compliance documentation.  
Produce professional artifacts (SSP, POA&M, and RFI) that demonstrate applied cybersecurity governance.
<br><br>

**Materials and Methods**  
Hardware  
Component	Specification
Host CPU	AMD Ryzen 7 9800X3D (8 Core / 16 Thread)  
Host Memory	64 GB DDR5 RAM  
Host Storage,	4 TB, SSD WD Blue SN5000, Internal (VMware and OS); 1 TB, SSD SanDisk Extreme 55AE SCSI, External (VMware virtual OS)  
Virtualization Platform	VMware Workstation Pro [Version #17.5.2]  
Total Allocated Lab Resources	10 vCPUs, ~24 GB RAM, ~300 GB Disk  

Software  
System,	Operating System,	Purpose  
WIN-DC,	Windows Server 2022 Datacenter (Evaluation),	Domain Controller / DNS  
WIN-CL,	Windows 10 Pro (Evaluation),	Domain-Joined Workstation  
UBU-APP,	Ubuntu Server 22.04, LTS	Application Server (SSH MFA + SFTP Chroot)  
UBU-SECOPS,	Ubuntu Server 22.04, LTS	Log Aggregation / rsyslog / future Wazuh SIEM  
Optional Device,	Android-x86 or OpenWRT,	Simulated IoT Device or Mobile Node
