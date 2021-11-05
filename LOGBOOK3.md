# Trabalho realizado na Semana #3

## Identificação

- Affected the Traffic Management User Interface (TMUI) of multiple BIG-IP products, which allows users to manage their product and its settings.
- Originated from multiple hosts targeting F5 BIG-IP servers, resulting in complete system compromise. 
- Unauthenticated attackers with network access to the Configuration utility able to eventually gain full control over the BIG-IP device.
- Attackers were able to execute arbitrary system commands, create or delete files, disable services, and/or execute arbitrary Java code. 

## Catalogação

- 3,012 in 8,204 unique scanned IPv4 hosts vulnerable in 66 countries. 
- It currently affects: Government agencies, Public universities and schools, Hospitals and healthcare providers, Major financial and banking institutions, among others.
- CVSS score of 9.8/10 - critical.
- The BIG-IP bug was found and privately reported to F5 by Mikhail Klyuchnikov, a security researcher at Positive Technologies.

## Exploit

- It can allow threat actors to gain a foothold inside the targeted networks and conduct malicious activity, such as spreading ransomware.
- CWE (Common Weakness Enumeration) 74 - The software constructs all or part of a command, data structure, or record using externally-influenced input from an upstream component, but it does not neutralize or incorrectly neutralizes special elements that could modify how it is parsed or interpreted when it is sent to a downstream component.
- There is a Metasploit module that exploits a directory traversal in F5's BIG-IP Traffic Management User Interface (TMUI) to upload a shell script and execute it as the root user. 

## Ataques

- NCC Group notes that attackers are leveraging the vulnerability to try to capture “web.xml” or “/etc/hosts” from vulnerable hosts.
- Kevin Beaumont, senior threat intelligence analyst at Microsoft, discovered that attackers had planted a cryptocurrency miner on one of his F5 honeypots.
- Attackers tried to exploit BIG-IP multi-purpose networking devices, to install coin-miners, IoT malware, or to scrape administrator credentials from the hacked devices.
