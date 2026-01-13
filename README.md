# Wireshark
Analyzing  malicious network traffic using Wireshark.

<h2>Project Overview</h2>
<p>This project involves a deep-dive packet analysis of a network breach at "Bartell Ltd." An employee in the Purchasing Department opened a malicious Word document, triggering an outbound connection to a command-and-control (C2) server.
Using Wireshark, I performed a forensic analysis of the provided .pcap file to identify the malware delivery mechanism, the attacker's infrastructure, and the subsequent "malspam" (malicious spam) activity originating from the compromised host.</p> </br>

<h2>Technical Skills Demonstrated</h2>
<p><b>-Traffic Filtering</b>: Using advanced Wireshark display filters (HTTP, DNS, TCP) to isolate malicious streams.

<b>-Malware Triage</b>: Identifying suspicious file downloads  via unencrypted web traffic.

<b>-Protocol Analysis</b>: Inspecting HTTP headers (User-Agents, Server headers).
 </p> </br>

<h2>Investigation Walktrough</h2>
<p>The investigation began by filtering for HTTP traffic to identify the first connection to a known malicious IP.

   The first connection occurred on 2021-09-24 16:44:38.
 <img src="https://i.imgur.com/rZlE3SG.png" height="80%" width="80%" alt="Investigation Walkthrough"/>

   A file named documents.zip was downloaded from the malicious server.
  <img src="https://i.imgur.com/rZlE3SG.png" height="80%" width="80%" alt="Investigation Walkthrough"/>

   The name of the zipfile is chart-1530076591.txt.
   <img src="https://i.imgur.com/l6R12xG.png" height="80%" width="80%" alt="Investigation Walkthrough"/>

   The three domains involved in the malicious file download activity are: finejewels.com.au,thietbiagt.com, new.americold.com
   <img src="https://i.imgur.com/b17gl7e.png" height="80%" width="80%" alt="Investigation Walkthrough"/>

   The two IP addresses of the Cobalt Strike servers are: 185.106.96.158, 185.125.204.174
   <img src="https://i.imgur.com/IXZjxab.png" height="80%" width="80%" alt="Investigation Walkthrough"/>

   Researched in VirtusTotal and confirmed that it is about Cobalt Strike.
   <img src="https://i.imgur.com/ZlqmFdl.png" height="80%" width="80%" alt="Investigation Walkthrough"/>
   <img src="https://i.imgur.com/SOYtXFX.png" height="80%" width="80%" alt="Investigation Walkthrough"/>
 </p>
