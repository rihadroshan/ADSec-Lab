# **Active Directory security, monitoring, and attack simulation**  

A comprehensive security lab environment designed for security testing, monitoring, and attack simulation. This environment includes an Active Directory domain, Splunk for log analysis, and a dedicated security testing infrastructure.  

## **Network Architecture**  

![Network Infrastructure](./assets/network-diagram.png)  

### **Components**

- **Domain:** Webcorp
- **Network Range:** 192.168.1.0/24
- **Key Systems:**
  - **Active Directory Domain Controller** (Windows Server 2025)
    - IP: 192.168.1.10
    - Role: Authentication, GPO management, DNS services
  - **Splunk (SIEM)** (Ubuntu Server)
    - IP: 192.168.1.20
    - Role: Log aggregation, event correlation, threat detection
  - **Domain Workstation** (Windows 10 Pro)
    - IP: DHCP Assigned
    - Role: End-user simulation, security control testing
  - **Attack Platform** (Kali Linux)
    - IP: 192.168.1.100
    - Role: Penetration testing, threat simulation

## **Key Features**

- **Realistic Enterprise Environment:** Simulated corporate infrastructure with proper user hierarchy, group policies, and security controls
- **End-to-End Visibility:** Centralized logging with Sysmon and Splunk for comprehensive detection capabilities
- **Red/Blue Team Training:** Dedicated platform for attack simulation and defensive response exercises
- **Isolated Test Environment:** Self-contained network for safe security experimentation

## **System Configurations**

### **Domain Controller (Windows Server 2022)**
- Domain: webcorp.local
- Active Directory structure with realistic OUs (HR, IT, Finance, etc.)
- Group Policy Objects for security baselines
- DNS and DHCP services
- Sysmon with enhanced logging configuration

### **Splunk SIEM (Ubuntu Server)**
- Splunk Enterprise deployment
- Custom dashboards for security monitoring
- Saved searches for common attack techniques
- Alert configurations for suspicious activities
- Universal Forwarder management

### **Client Workstation (Windows 10 Pro)**
- Domain-joined endpoint with simulated user profiles
- Microsoft Office and common productivity tools
- Sysmon and Universal Forwarder deployment
- Vulnerable software for testing (configurable)

### **Attack Platform (Kali Linux)**
- Preinstalled penetration testing tools
- Atomic Red Team framework for attack automation
- Custom scripts for common AD attacks
- Metasploit Framework and other exploitation tools

## **Security Monitoring & Attack Simulation**  

- **Detection & Analysis:**
  - Real-time correlation rules in Splunk
  - MITRE ATT&CK mapping for detected techniques
  - Historical search capabilities for forensic analysis
  - Automated alerting for critical security events

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

## **Downloads & Resources**

| **Component** | **Download Link** | **Purpose** |
|---------------|-------------------|-------------|
| Windows Server 2022 | [Microsoft Evaluation Center](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2025) | Domain Controller |
| Ubuntu Server | [Ubuntu](https://ubuntu.com/download/server) | Splunk SIEM Platform |
| Windows 10 Pro | [Windows 10 Pro](https://www.microsoft.com/en-ca/software-download/windows10) | Domain Workstation |
| Kali Linux | [Kali Images](https://www.kali.org/get-kali/#kali-installer-images) | Attack Platform |
| Splunk Enterprise | [Splunk Enterprise](https://www.splunk.com/en_us/download/splunk-enterprise.html) | Security Monitoring |
| Splunk Universal Forwarder    | [Splunk Universal Forwarder](https://www.splunk.com/en_us/download/universal-forwarder.html) | Log Forwarding to Splunk           |
| Sysmon | [Microsoft Sysinternals](https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon) | Advanced Endpoint Logging |
| Atomic Red Team | [GitHub Repository](https://github.com/redcanaryco/atomic-red-team) | Attack Simulation Framework |

 
