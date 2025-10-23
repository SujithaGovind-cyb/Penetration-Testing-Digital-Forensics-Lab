# Server Penetration Testing & Vulnerability Assessment: From Reconnaissance to Exploitation

This project details a comprehensive penetration test and vulnerability assessment performed on a simulated target server (Metasploitable3). The core objective was to move systematically through the offensive security lifecycle: reconnaissance, vulnerability scanning, exploitation, and post-exploitation. The results demonstrate end-to-end expertise in securing server environments by identifying, exploiting, and providing remediation strategies for critical weaknesses.

### Skills Learned

Vulnerability Assessment
- Systematic identification and classification of security flaws using automated tools and manual verification.

Penetration Testing
- Executing controlled exploitation using the Metasploit Framework.

Reconnaissance & Enumeration
- Detailed host discovery, port scanning, and service enumeration (Nmap).

Post-Exploitation
- Privilege escalation, hash extraction, and local system reconnaissance.

Password Cracking
- Offline hash analysis using high-performance cracking tools (Hashcat).

Risk Reporting
- Documenting findings and delivering prioritized, actionable remediation recommendations.

### Tools Used

- Network Scanning & Enumeration: Nmap
- Vulnerability Analysis: Nessus Professional
- Exploitation & Payload Delivery: Metasploit Framework
- Credential Auditing: Hashcat
- Operating Systems: Kali Linux (Attacker), Metasploitable3 (Target)

## Steps
The project followed a rigorous, multi-stage methodology to ensure full coverage and realistic simulation of an attack:

1. Host Discovery and Enumeration (Nmap)

- Executed comprehensive Nmap scans to identify open ports, running services, and the target operating system (Metasploitable3 - Ubuntu).
- Performed service version enumeration to identify specific, potentially vulnerable software instances (See Figure 3.1 - Nmap Service Version Output).

2. Automated Vulnerability Assessment (Nessus)

- Conducted an in-depth, authenticated Nessus scan against the target, correlating known Common Vulnerabilities and Exposures (CVEs) with the discovered services.
- Prioritized critical risks based on CVSS scores, focusing on exploitable vulnerabilities like the ProFTPD mod_copy flaw and SSL/TLS configuration weaknesses.

3. Controlled Exploitation (Metasploit)

- Selected and deployed an appropriate module within the Metasploit Framework to successfully exploit a high-severity vulnerability identified in the previous step.
- Established a remote command shell on the target server, confirming unauthorized access. (See Figure 5.1 - Metasploit Session Confirmation).

4. Post-Exploitation and Hash Extraction

- Utilized post-exploitation modules to pivot within the compromised environment and escalate privileges to root access.
- Successfully extracted system credentials by locating and combining the local /etc/passwd and /etc/shadow files for offline auditing.

5. Offline Password Auditing (Hashcat)

- Identified the hash types for the extracted credentials and utilized Hashcat with targeted wordlists and rule-sets.
- Successfully cracked several high-value user passwords, demonstrating the critical risk posed by weak credential management on the server. (See Figure 6.2 - Hashcat Password Cracking Success).

6. Risk Analysis and Remediation

- Compiled a comprehensive report detailing all identified vulnerabilities, successful exploits, and the impact of the attack chain.
- Provided specific, actionable remediation recommendations, including patch management strategies and secure configuration baselines (e.g., disabling weak SSL ciphers).

*Ref 1: Network Diagram*
