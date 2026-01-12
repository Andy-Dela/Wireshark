# Wireshark
Analyzing  malicious network traffic using Wireshark.

<h2>Project Overview</h2>
<p>This project involves a deep-dive packet analysis of a network breach at "Bartell Ltd." An employee in the Purchasing Department opened a malicious Word document, triggering an outbound connection to a command-and-control (C2) server.
Using Wireshark, I performed a forensic analysis of the provided .pcap file to identify the malware delivery mechanism, the attacker's infrastructure, and the subsequent "malspam" (malicious spam) activity originating from the compromised host.</p> </br>

<h2>Technical Skills Demonstrated</h2>
<p><b>-Traffic Filtering</b>: Using advanced Wireshark display filters (HTTP, DNS, SMTP, TCP) to isolate malicious streams.

<b>-Malware Triage</b>: Identifying suspicious file downloads (ZIP, DLL, EXE) via unencrypted web traffic.

<b>-Protocol Analysis</b>: Inspecting HTTP headers (User-Agents, Server headers) and SMTP traffic to identify data exfiltration.

<b>-Incident Timeline</b>: Reconstructing the sequence of events from the initial infection to secondary payload delivery. </p> </br>

<h2>Investigation Walktrough</h2>
<p>The investigation began by filtering for HTTP traffic to identify the first connection to a known malicious IP.

Timeline: The first connection occurred on 2021-09-24 16:44:38.
 <img src="https://i.imgur.com/xDp1hu9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Artifact: A file named documents.zip was downloaded from the malicious server.

Secondary Payload: Following the ZIP download, the victim machine requested 623.dll, a common indicator of modular malware like Emotet or Trickbot.</p>
