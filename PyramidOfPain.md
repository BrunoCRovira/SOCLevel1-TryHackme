
# Pyramid of Pain 

**Learn what is the pyramid of Pain and how to utilize it**

### Hash Values (Trivial)
* **MD5 (Message Digiest defined by RFC 1321)**
* **SHA-1(Secure Hash Algorithm 1 defined by RFC 3174)**
* **SHA-2 (Secure Hash Algorithm 2)** - SHA-156

  **Tools online can be used to hash lookups**
  [Virus Total](https://www.virustotal.com/gui/home/upload)
  [Opswat](https://metadefender.opswat.com/)

  ### IP Address (Easy)



**Fast Flux**


<p>Fast flux is a technique used by cybercriminals to increase their infrastructure's resilience by making law enforcement takedown of their servers and denylisting of their IP addresses harder. It is critical for these cybercriminals to maintain their networks' uptime to avoid losses to their revenue streams, including phishing and scam campaigns, botnet rental and illegal gambling operations. </p>

### Domain Names (Simple)
**Punycode Attack**
<p>Used by the attackers to redirect users to a malicious domain that seems legitimate at first glance.</p>

<p>Unicode that converts words that cannot be written in ASCII, like the Greek word for thank you ‘ευχαριστώ’ into an ASCII encoding, like ‘xn--mxahn5algcq2e’ for use as domain names.</p>

<p>To detect the malicious domains, proxy logs or web server logs can be used.</p>

<p>Viewing Connections in Any.run</p>
* HTTP Request
* COnnections
* DNS Requests

### Host Artifacts (Annoying) 
<p>Host artifacts are the traces or observables that attackers leave on the system, such as registry values, suspicious process execution, attack patterns or IOCs (Indicators of Compromise), files dropped by malicious applications, or anything exclusive to the current threat</p>

### Network Artifacts (Annoying)
<p>A network artifact can be a user-agent string, C2 information, or URI patterns followed by the HTTP POST requests.An attacker might use a User-Agent string that hasn’t been observed in your environment before or seems out of the ordinary. The User-Agent is defined by RFC2616 as the request-header field that contains the information about the user agent originating the request.</p>
<p>Network artifacts can be detected in Wireshark PCAPs (file that contains the packet data of a network) by using a network protocol analyzer such as TShark or exploring IDS (Intrusion Detection System) logging from a source such as Snort.</p>

**tshark --Y http.request -T fileds -e http.host -e http.user_agent -r analysis_file.pcap**

<p>If you can detect the custom User-Agent strings that the attacker is using, you might be able to block them, creating more obstacles and making their attempt to compromise the network more annoying.</p>

### Tools Challenging

<p>Antivirus signatures, detection rules, and YARA rules can be great weapons for you to use against attackers at this stage.

MalwareBazaar and Malshare are good resources to provide you with access to the samples, malicious feeds, and YARA results - these all can be very helpful when it comes to threat hunting and incident response. 

For detection rules, SOC Prime Threat Detection Marketplace is a great platform, where security professionals share their detection rules for different kinds of threats including the latest CVE's that are being exploited in the wild by adversaries. 

Fuzzy hashing is also a strong weapon against the attacker's tools. Fuzzy hashing helps you to perform similarity analysis - match two files with minor differences based on the fuzzy hash values. One of the examples of fuzzy hashing is the usage of SSDeep; on the SSDeep official website, you can also find the complete explanation for fuzzy hashing. </p>

<p>Fuzzy hashing is also a strong weapon against the attacker's tools. Fuzzy hashing helps you to perform similarity analysis - match two files with minor differences based on the fuzzy hash values. One of the examples of fuzzy hashing is the usage of SSDeep; on the SSDeep official website, you can also find the complete explanation for fuzzy hashing. </p>

### TTPs (Tough)
<p>TTPs stands for Tactics, Techniques & Procedures. This includes the whole MITRE ATT&CK Matrix, which means all the steps taken by an adversary to achieve his goal, starting from phishing attempts to persistence and data exfiltration. </p>






