# **Active Directory Security Lab**  

A comprehensive security lab environment designed for security testing, monitoring, and attack simulation. This environment includes an Active Directory domain, Splunk for log analysis, and a dedicated security testing infrastructure.  

## **Network Architecture**  

![Network Infrastructure](./assets/network-diagram.png)  

### **Components**  

- **Domain:** Webcorp  
- **Network Range:** 192.168.1.0/24  
- **Key Systems:**  
  - **Active Directory Domain Controller (Windows Server 2022)**
    - IP Address: 192.168.1.10  
    - Provides authentication, domain management, and centralized user access control.  
  - **Splunk Server (Ubuntu Server)**
    - IP Address: 192.168.1.20  
    - Monitors logs and security events via Universal Forwarder.  
  - **Windows 10 Pro Workstation**
    - IP Address: DHCP Assigned  
    - Simulates an endpoint within the domain for security monitoring and attack simulation.  
  - **Kali Linux (Attacker Machine)**
    - IP Address: 192.168.1.100  
    - Used for security testing, penetration testing, and adversary simulations.  

## **Key Features**  

- **Active Directory Security Testing:** Simulated corporate environment with user roles, departments, and security policies.  
- **Centralized Log Monitoring:** Splunk deployment with Sysmon and Universal Forwarder for real-time log collection.  
- **Red Team/Blue Team Simulations:** Ability to conduct attack simulations using Atomic Red Team and analyze attack detection in Splunk.  
- **Network Segmentation:** Controlled environment for security analysis and incident response exercises.  

## **System Configuration**  

### **Active Directory (Windows Server 2022)**  

- Configured as the domain controller (`Webcorp`).  
- Includes user groups and organizational units (HR, IT).  
- Integrated with Sysmon for enhanced security logging.  
- Supports Windows 10 workstations via domain join.  

### **Splunk Server (Ubuntu Server)**  

- Deployed with Splunk Enterprise.  
- Configured to collect logs from Windows endpoints using Universal Forwarder.  
- Monitors Sysmon, Security, Application, and System logs.  
- Implements event correlation for threat detection.  

### **Windows 10 Pro Workstation**  

- Functions as a domain-joined endpoint.  
- Equipped with Sysmon and Splunk Universal Forwarder.  
- Used for endpoint security monitoring and adversary simulations.  

### **Kali Linux (Attacker Machine)**  

- Configured for penetration testing and adversary simulations.  
- Supports brute-force attacks, lateral movement, and RDP testing.  
- Integrated with Atomic Red Team for controlled attack execution.  

## **Security Monitoring & Attack Simulation**  

- **Sysmon Implementation:**  
  - Provides detailed process monitoring and security event logging.  
  - Logs forwarded to Splunk for centralized analysis.  

- **Splunk Configuration:**  
  - Collects and indexes logs from Windows and Linux endpoints.  
  - Detects anomalous activities and generates security alerts.  

- **Attack Simulations with Atomic Red Team:**  
  - Provides a structured framework for testing detection capabilities.  
  - Generates simulated attack behaviors that can be analyzed in Splunk.  

## **Prerequisites**  

- **Hardware:**  
  - Minimum **16GB RAM** recommended.  
  - **250GB storage** for VM environments.  

- **Software Requirements:**  
  - Windows Server 2022 [Download](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2022)  
  - Ubuntu Server [Download](https://ubuntu.com/download/server)  
  - Windows 10 Pro [Download](https://www.microsoft.com/en-ca/software-download/windows10)  
  - Kali Linux [Download](https://www.kali.org/get-kali/#kali-installer-images)  

## **Relevant Downloads**  

| **Tool**                          | **Download Link** |
|-----------------------------------|------------------|
| **Sysmon (System Monitor)**       | [Sysmon Download](https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon) |
| **Sysmon Config (Modular Ruleset)** | [Sysmon Config](https://raw.githubusercontent.com/olafhartong/sysmon-modular/refs/heads/master/sysmonconfig.xml) |
| **Splunk Enterprise**             | [Splunk Download](https://www.splunk.com/en_us/download/splunk-enterprise.html) |
| **Splunk Universal Forwarder**    | [Universal Forwarder Download](https://www.splunk.com/en_us/download/universal-forwarder.html) |
| **Atomic Red Team (Attack Simulation)** | [Atomic Red Team](https://github.com/redcanaryco/atomic-red-team) |
 
