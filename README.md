# Home Network Risk Assessment

![assasment](https://github.com/user-attachments/assets/c9e0ed7e-8ef2-44e6-a165-e4a5a2a926d4)

## Overview
This project involves performing a risk assessment on a home network. The goal is to identify potential vulnerabilities and offer actionable recommendations to enhance network security.

## Objectives
- **Identify Network Devices:** Discover devices connected to the network.
- **Scan for Vulnerabilities:** Assess the network for potential security issues.
- **Analyze Risks:** Evaluate the potential impact of identified vulnerabilities.
- **Provide Recommendations:** Suggest measures to mitigate identified risks.

## Methodology
   **Network Mapping:**
   - **Tool Used:** Nmap
   - **Command:** `nmap -sP 192.168.1.0/24`
   - **Description:** This step involves discovering devices on the local network by scanning the IP range

   **Home Network Description:**
   
     This risk assessment evaluates the security posture of a typical suburban home network with various connected devices, including laptops, smartphones, a smart TV, a gaming console, smart home devices, and a Wi-Fi-enabled home security system, all connected through a router.
   
| Quantity | Device  | Manufacturer  |
| ------------- | ------------- | ------------- |
| 2 | Air purifier | Hangzhou BroadLink Technology |
| 2 | Iphone 13  | Apple Inc. |
| 1 | Router | Sagemcom Broadband SAS |
| 2 | Smart lamp | Tuya Smart |
| 1 | 55" OLED 4K UHD Smart TV | Samsung |
| 1 | XBOX One Console | Microsoft |
| 1 | TV box | Telia |
| 2 | Lenovo Idealpad laptop | Lenovo | 

   **Vulnerability Scanning:**
   - **Tool Used:** OpenVAS
   - **Description:** Perform vulnerability scans on identified devices to uncover security issues.  
   
   **Identify Potential Risks:**

| **Risk Category**          | **Description**                                                                                                          |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------|
| **Unauthorized Access**     | Risk of unauthorized individuals gaining access to the network due to weak or misconfigured security settings.           |
| **Malware and Viruses**     | Devices on the network becoming infected with malware, leading to data theft, loss, or system compromise.                |
| **Phishing Attacks**        | Network users might unintentionally disclose sensitive information due to phishing attempts.                             |
| **Weak Passwords**          | The use of default or weak passwords across network devices, increasing the chance of unauthorized access.               |
| **Outdated Software**       | Devices and services running unpatched or outdated software, exposing known vulnerabilities to exploitation.             |
| **Data Interception**       | Unencrypted or weakly encrypted data could be intercepted over the network.                                               |
| **Device Theft or Loss**    | Loss or theft of mobile or smart devices, posing a risk of data breaches.                                                |
| **Network Overload/Failure**| Network performance degradation or service disruption due to overload or configuration issues.                           |
 
   **Analyze Risks:**
   
| **Risk**                   | **Likelihood** | **Impact** |
|----------------------------|----------------|------------|
| **Unauthorized Access**     | High           | High       |
| **Malware and Viruses**     | Medium         | High       |
| **Phishing Attacks**        | Low            | Medium     |
| **Weak Passwords**          | High           | High       |
| **Outdated Software**       | Medium         | High       |
| **Data Interception**       | Medium         | High       |
| **Device Theft or Loss**    | Low            | Medium     |
| **Network Overload/Failure**| Low            | Low        |

## Findings and Recommendations
1. **Weak Encryption Algorithms**:
   - Several services on the network were found to use weak SSL/TLS encryption algorithms, which could allow attackers to intercept and decrypt data.
   - **Recommendation**: Update configurations to enforce stronger encryption standards (e.g., TLS 1.2 or 1.3).

2. **Open Ports and Unrestricted Services**:
   - Some services on the network were found to have open ports, increasing the attack surface for unauthorized access.
   - **Recommendation**: Disable or restrict access to unnecessary services, and close any open ports not required for regular use.

3. **Use of Weak or Default Passwords**:
   - Certain devices or services are using default or weak passwords, which could be easily guessed by attackers.
   - **Recommendation**: Change all default passwords and enforce strong password policies across the network.

4. **Unpatched Software and Firmware**:
   - Some devices and services are running outdated software or firmware, exposing known vulnerabilities.
   - **Recommendation**: Regularly update software and firmware to the latest versions to mitigate these risks.

5. **Potential Data Interception**:
   - Lack of encryption for some network traffic could allow data interception.
   - **Recommendation**: Ensure all sensitive data transmission is encrypted using secure protocols.

6. **TCP and ICMP Information Leakage**:
   - Devices on the network were found to leak information (e.g., uptime) through TCP timestamps and ICMP replies, which could be used in targeted attacks.
   - **Recommendation**: Disable unnecessary network protocols, such as TCP timestamps and ICMP replies, if they are not required.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details. 
