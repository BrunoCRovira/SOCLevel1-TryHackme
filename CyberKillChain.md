# Cyber Kill Chain

<p>The Cyber Kill Chain framework is designed for identification and prevention of the network intrusions. You will learn what the adversaries need to do in order to achieve their goals.</p>

<p>he term kill chain is a military concept related to the structure of an attack. It consists of target identification, decision and order to attack the target, and finally the target destruction</p>

**help you undertand end protect against:**
* APT 
* Ransomware Attacks

**Phases Of Kill Chain**

* Reconnaissance
* Weponization
* Delivery 
* Explotation 
* Installation 
* Command & COntrol 
* ACtions on Objectives.

![Cyber Kill Chain ](CyberKill.png)

## Reconnaissance 
**Reconnaisance**: Is discovering and collecting information on the system and the victim. The reconnaisance phase is the planning phase for the adversaries.

**OSINT**
* Email Harvesting
  * theHarvester.
  * Hunter.io.
  * Osint Framework.

## Weaponization 
**Malware: is a program or software that is designed to damage disrupt, or gain unauthorized access to a computer**
**Exploit: is a program or a code that takes advantage ot the vulnerability or flaw in the application or system**
**Payload: is a malicious code that the attacker runs on the system**
**In this phase the attacker can follow next steps**

* Create an infected Microsoft Office document containing a malicious macro or VBA (Visual Basic for Applications) scripts. If you want to learn about macro and VBA, please refer to the article "Intro to Macros and VBA For Script Kiddies" by TrustedSec.
* An attacker can create a malicious payload or a very sophisticated worm, implant it on the USB drives, and then distribute them in public. An example of the virus. 
An attacker would choose Command and Control (C2) techniques for executing the commands on the victim's machine or deliver more payloads. You can read more about the C2 techniques on MITRE ATT&CK.
* An attacker would choose Command and Control (C2) techniques for executing the commands on the victim's machine or deliver more payloads. You can read more about the C2 techniques on MITRE ATT&CK.
* An attacker would select a backdoor implant (the way to access the computer system, which includes bypassing the security mechanisms).

## Delivery 
* Phishing
* Distributing a infected USB
* Watering Hole attack

## Exploitation

<p>After gaining access to the system, the malicious actor could exploit software, system, or server-based vulnerabilities to escalate the privileges or move laterally through the network. According to CrowdStrike, lateral movement refers to the techniques that a malicious actor uses after gaining initial access to the victim's machine to move deeper into a network to obtain sensitive data. </p>
<p>"the zero-day exploit or a zero-day vulnerability is an unknown exploit in the wild that exposes a vulnerability in software or hardware and can create complicated problems well before anyone realizes something is wrong. A zero-day exploit leaves NO opportunity for detection at the beginning."</p>

**EXamples of how an ataccker carries out explotation**
* The victim triggers the exploit by opening the email attachment or clicking on a malicious link.
* Using a zero-day exploit.
* Exploit software, hardware, or even human vulnerabilities. 
* An attacker triggers the exploit for server-based vulnerabilities. 


## Installation 

<p>Once the attacker gets access to the system, he would want to reaccess the system if he loses the connection to it or if he got detected and got the initial access removed, or if the system is later patched. He will no longer have access to it. That is when the attacker needs to install a persistent backdoor. A persistent backdoor will let the attacker access the system he compromised in the past.</p>

**The persistence can be achieved through:**

* Installing a web shell on the webserver. A web shell is a malicious script written in web development programming languages such as ASP, PHP, or JSP used by an attacker to maintain access to the compromised system. Because of the web shell simplicity and file formatting (.php, .asp, .aspx, .jsp, etc.) can be difficult to detect and might be classified as benign. You may check out this great article released by Microsoft on various web shell attacks.
* Installing a backdoor on the victim's machine. For example, the attacker can use Meterpreter to install a backdoor on the victim's machine. Meterpreter is a Metasploit Framework payload that gives an interactive shell from which an attacker can interact with the victim's machine remotely and execute the malicious code.
* Creating or modifying Windows services. This technique is known as T1543.003 on MITRE ATT&CK (MITRE ATT&CK® is a knowledge base of adversary tactics and techniques based on real-world scenarios). An attacker can create or modify the Windows services to execute the malicious scripts or payloads regularly as a part of the persistence. An attacker can use the tools like sc.exe (sc.exe lets you Create, Start, Stop, Query, or Delete any Windows Service) and Reg to modify service configurations. The attacker can also masquerade the malicious payload by using a service name that is known to be related to the Operating System or legitimate software. 
* Adding the entry to the "run keys" for the malicious payload in the Registry or the Startup Folder. By doing that, the payload will execute each time the user logs in on the computer. According to MITRE ATT&CK, there is a startup folder location for individual user accounts and a system-wide startup folder that will be checked no matter what user account logs in.
****************
<p>In this phase, the attacker can also use the Timestomping technique to avoid detection by the forensic investigator and also to make the malware appear as a part of a legitimate program. The Timestomping technique lets an attacker modify the file's timestamps, including the modify, access, create and change times. </p>

************
## Command & Control
<p>The compromised endpoint would communicate with an external server set up by an attacker to establish a command & control channel. After establishing the connection,  the attacker has full control of the victim's machine. Until recently, IRC (Internet Relay Chat) was the traditional C2 channel used by attackers. This is no longer the case, as modern security solutions can easily detect malicious IRC traffic</p>

<p>
  
  **The most common C2 channels used by adversaries nowadays:**

The protocols HTTP on port 80 and HTTPS on port 443 - this type of beaconing blends the malicious traffic with the legitimate traffic and can help the attacker evade firewalls.  
DNS (Domain Name Server). The infected machine makes constant DNS requests to the DNS server that belongs to an attacker, this type of C2 communication is also known as DNS Tunneling.
</p>

## Actions on Objectives

**Goals of the ACtion Objectives**
* Collect the credentials from users.
* Perform privilege escalation (gaining elevated access like domain administrator access from a workstation by exploiting the misconfiguration).
* Internal reconnaissance (for example, an attacker gets to interact with internal software to find its vulnerabilities).
* Lateral movement through the company's environment.
* Collect and exfiltrate sensitive data.
* Deleting the backups and shadow copies. Shadow Copy is a Microsoft technology that can create backup copies, snapshots of computer files, or volumes. 
O* verwrite or corrupt data.









