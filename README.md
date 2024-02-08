<h1>  SIEM home lab: geographic data for unsuccessful RDP connections to an IP address.</h1>


<h2>Description</h2>
<b>The Powershell script in this repository is responsible for parsing out Windows Event Log information for failed RDP attacks and using a third party API to collect geographic information about the attackers location.
</b>
<br />
<br />
The script is used in this demo where I setup Azure Sentinel (SIEM) and connect it to a live virtual machine acting as a honey pot. We will observe live attacks (RDP Brute Force) from all around the world. I will use a custom PowerShell script to look up the attackers Geolocation information and plot it on an Azure Sentinel Map!
<br />
<br />

<p align="center">
<img src="https://i.imgur.com/cpTECWR.png" height="85%" width="85%" alt="RDP event fail logs"/>
</p>
<h2>Languages Used</h2>

- <b>PowerShell:</b> Extract RDP failed logon logs from Windows Event Viewer 

<h2>Utilities Used</h2>

- <b>ipgeolocation.io:</b> IP Address to Geolocation API

<h2>Attacks coming in; Custom logs being output with geodata</h2>

<p align="center">
<img src="https://i.imgur.com/QmGjLnw.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>


<h2>World map of incoming attacks after 24 hours (built custom logs including geodata)</h2>

<p align="center">
<img src="https://i.imgur.com/mEbWMlo.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>

## Key Components

1. **RDP Event Fail Logs**: PowerShell script extracts failed RDP logon events from the Windows Event Viewer.
2. **Languages Used**:
   - PowerShell: Used to extract RDP failed logon logs from the Windows Event Viewer.
3. **Utilities Used**:
    - ipgeolocation.io: Utilized for the IP Address to Geolocation API functionality.
