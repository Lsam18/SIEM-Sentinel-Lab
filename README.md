# SIEM-Sentinel-Lab
Failed RDP (Remote Desktop Protocol) to IP Geolocation Information

<h2>Description</h2>
<b>The Powershell script in this repository is responsible for parsing out Windows Event Log information for failed RDP attacks and using a third party API to collect geographic information about the attackers location.
</b>
<br />
<br />
The script is used in this demo where I setup Azure Sentinel (SIEM) and connect it to a live virtual machine acting as a honey pot.
We will observe live attacks (RDP Brute Force) from all around the world. I will use a custom PowerShell script to
look up the attackers Geolocation information and plot it on an Azure Sentinel Map!
<br />
<br />

<p align="center">
<img width="1440" alt="Screenshot 2024-05-09 at 21 14 17" src="https://github.com/Lsam18/SIEM-Sentinel-Lab/assets/115799412/8227fb6b-2533-415c-92cd-32a8e4493564">

</p>

<h2>Languages Used</h2>

- <b>PowerShell:</b> Extract RDP failed logon logs from Windows Event Viewer 

<h2>Utilities Used</h2>

- <b>ipgeolocation.io:</b> IP Address to Geolocation API

<h2>Attacks from Pakistan and Sri Lanka coming in; Custom logs being output with geodata</h2>

<p align="center">
<img width="1440" alt="Screenshot 2024-05-09 at 18 26 10" src="https://github.com/Lsam18/SIEM-Sentinel-Lab/assets/115799412/dd2d03e0-6e9b-4bc2-9f3d-c594a92a9421">

</p>

<h2>World map of incoming attacks after 24 hours (built custom logs including geodata)</h2>
<img width="1440" alt="Screenshot 2024-05-09 at 21 00 44" src="https://github.com/Lsam18/SIEM-Sentinel-Lab/assets/115799412/6800b776-e3ae-4d20-bbb4-7d42186d51d5">

<p align="center">

</p>


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
