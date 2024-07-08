# IncidentHandlingWithSplunk

<p align="center">
<br/>
<img src="https://i.imgur.com/fT0Gi9r.png"/>

<h2>Description</h2>

Learn to use Splunk for incident handling through interactive scenarios.

<h2>Task 1: Introduction: Incident Handling</h2>

This room covers an incident Handling scenario using Splunk. An incident from a security perspective is "Any event or action, that has a negative consequence on the security of a user/computer or an organization is considered a security incident." Below are a few of the events that would negatively affect the environment when they occurred:

 - Crashing the system
 - Execution of an unwanted program
 - Access to sensitive information from an unauthorized user
 - A Website being defaced by the attacker
 - The use of USB devices when there is a restriction in usage is against the company's policy


<h2>Learning Objective and Pre-requisites</h2>

 - Learn how to leverage OSINT sites during an investigation
 - How to map Attacker's activities to Cyber Kill Chain Phases
 - How to utilize effective Splunk searches to investigate logs
 - Understand the importance of host-centric and network-centric log sources

<h2>Task 2: Incident Handling - Life Cycle</h2>

<h2>Task 3: Incident Handling: Scenario</h2>

In this exercise, we will investigate a cyber attack in which the attacker defaced an organization's website. This organization has Splunk as a SIEM solution setup. Our task as a Security Analysis would be to investigate this cyber attack and map the attacker's activities into all 7 of the Cyber Kill Chain Phases. It is important to note that we don't need to follow the sequence of the cyber kill chain during the Investigation. One finding in one phase will lead to another finding that may have mapped into some other phase.

**Scenerio**: A Big corporate organization Wayne Enterprises has recently faced a cyber-attack where the attackers broke into their network, found their way to their web server, and have successfully defaced their website http://www.imreallynotbatman.com. Their website is now showing the trademark of the attackers with the message YOUR SITE HAS BEEN DEFACED.They have requested "US" to join them as a Security Analyst and help them investigate this cyber attack and find the root cause and all the attackers' activities within their network.

The good thing is, that they have Splunk already in place, so we have got all the event logs related to the attacker's activities captured. We need to explore the records and find how the attack got into their network and what actions they performed.
This Investigation comes under the Detection and Analysis phase. 

During our investigation, we will be using Splunk as our SIEM solution. Logs are being ingested from webserver/firewall/Suricata/Sysmon etc. In the data summary tab, we can explore the log sources showing visibility into both network-centric and host-centric activities. To get the complete picture of the hosts and log sources being monitored in Wayne Enterprise, please click on the Data summary and navigate the available tabs to get the information.

<p align="center">
<br/>
<img src="https://i.imgur.com/pa6PhFS.png"/>

