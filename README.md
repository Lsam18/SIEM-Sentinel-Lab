# Security Information and Event Management (SIEM) - Sentinel-Lab

## Overview
This repository contains a PowerShell script designed to sift through Windows Event Logs, pinpointing failed Remote Desktop Protocol (RDP) attacks and utilizing a third-party API to gather geographical data about the attackers' locations.

The script powers a demonstration where Azure Sentinel (SIEM) is set up, connected to a live virtual machine acting as a honeypot. By monitoring live attacks, particularly RDP brute force attempts, the script dynamically fetches and visualizes the attackers' geolocation information on an Azure Sentinel Map.

## Project Components
1. **PowerShell Script**: The project utilizes a PowerShell script to extract RDP failed logon events from Windows Event Viewer. These events are crucial indicators of potential brute force attacks on systems.
   
2. **Azure Sentinel**: Azure Sentinel is a cloud-native SIEM and Security Orchestration, Automation, and Response (SOAR) solution provided by Microsoft. It collects and analyzes security data across an organization's entire hybrid environment, including devices, users, applications, and infrastructure. Azure Sentinel employs advanced analytics and machine learning to detect and respond to threats effectively.

3. **ipgeolocation.io API**: The project integrates with the ipgeolocation.io API to enrich the extracted IP addresses from RDP failed logon events with geolocation data. This information helps in identifying the geographical origin of the attackers, enabling better threat analysis and response.


<p align="center">
<img src="https://github.com/Lsam18/SIEM-Sentinel-Lab/assets/115799412/b202929d-e920-4467-b6d3-464646239b0a"/>
</p>



## Technologies Used
- **PowerShell**: For scripting and automating the extraction of RDP failed logon events.
- **Microsoft Azure**: Azure Sentinel is utilized as the SIEM platform.
- **ipgeolocation.io**: Provides geolocation data for IP addresses.
- **GitHub**: Hosting the project repository and documentation.
- **Visual Studio Code**: For script development and testing.

## Demonstration
In the provided demonstration, Azure Sentinel is configured to receive telemetry from the honeypot VM, detecting and logging failed RDP login attempts. The PowerShell script continuously monitors these logs, extracting relevant information and querying the ipgeolocation.io API to determine the geographic origin of the attackers.

## Languages Utilized
- **PowerShell:** The core functionality of the script involves extracting RDP failed logon logs from Windows Event Viewer.

## External Utilities
- **ipgeolocation.io:** Utilized for the IP Address to Geolocation API, enriching the logs with geographical data.

## Screenshots
### Attacks from Pakistan and Sri Lanka 

<p align="center">
<img src="https://github.com/Lsam18/SIEM-Sentinel-Lab/assets/115799412/dd2d03e0-6e9b-4bc2-9f3d-c594a92a9421"/>
</p>

### Attacks from Sri Lanka (My own Attempts - for testing purposes) 

<p align="center">
<img width="1440" alt="Screenshot 2024-05-09 at 18 39 31" src="https://github.com/Lsam18/SIEM-Sentinel-Lab/assets/115799412/91de6079-7f28-4569-8ef9-6afdeb7bb54a">
</p>

### World Map of Attacks After 24 Hours

<p align="center">
<img src="https://github.com/Lsam18/SIEM-Sentinel-Lab/assets/115799412/6800b776-e3ae-4d20-bbb4-7d42186d51d5"/>
</p>

## Future Enhancements
1. Implementing real-time alerts for anomalous activity.
2. Integrating with other threat intelligence sources for deeper analysis.
3. Enhancing visualization capabilities for better insights into attack patterns.
4. Developing automated response mechanisms to mitigate detected threats.


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>

