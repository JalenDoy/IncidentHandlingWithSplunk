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

<h2>Task 4: Reconnaissance Phase </h2>


<p align="center">
Splunk Instance with the logs needed to complete the task<br/>
<img src="https://i.imgur.com/rsFcdvk.png"/>


**Question 1: One suricata alert highlighted the CVE value associated with the attack attempt. What is the CVE value?** CVE-2014-6271

**Hint:** alert.signature = ET WEB_SERVER Possible CVE-2014-6271 Attempt in Headers 

**Question 2: What is the CMS our web server is using?** Joomla

**Question 3: What is the web scanner, the attacker used to perform the scanning attempts?** Acunetix

**Question 4: What is the IP address of the server imreallynotbatman.com?** 192.168.250.70

<h2>Task 5: Exploitation Phase</h2>

The attacker needs to exploit the vulnerability to gain access to the system/server.

In this task, we will look at the potential exploitation attempt from the attacker against our web server and see if the attacker got successful in exploiting or not.

To begin our investigation, let's note the information we have so far:

 - We found two IP addresses from the reconnaissance phase with sending requests to our server.
 - One of the IPs 40.80.148.42 was seen attempting to scan the server with IP 192.168.250.70.
 - The attacker was using the web scanner Acunetix for the scanning attempt.


**Question 1: What was the URI which got multiple brute force attempts?** /joomla/administrator/index.php

**Question 2: Against which username was the brute force attempt made?** Admin

**Question 3: What was the correct password for admin access to the content management system running imreallynotbatman.com?** CVE-2014-6271

**Question 4: How many unique passwords were attempted in the brute force attempt?** CVE-2014-6271

**Question 5: What IP address is likely attempting a brute force password attack against imreallynotbatman.com?** CVE-2014-6271

**Question 6: After finding the correct password, which IP did the attacker use to log in to the admin panel?** CVE-2014-6271



