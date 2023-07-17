## Performed a security Audit 
TO: IT Manager, stakeholders

FROM: Jeffrey Beckett

DATE: 06/29/2023

SUBJECT: Internal IT Audit Findings and Recommendations


Dear Colleagues,

I would like to bring your attention to the findings and recommendations from the recent internal IT audit conducted at Botium Toys. The audit focused on assessing the security posture, compliance alignment, and technology inventory of our organization. Below, you will find a summary of the audit scope, goals, critical findings, and a concise summary of our recommendations.

Audit Summary:

Scope: The audit covered user permissions, controls implementation, procedures and protocols, compliance alignment, and technology inventory at Botium Toys.
Goals: Enhance security posture, achieve compliance, establish a robust cybersecurity framework, implement least privilege, develop comprehensive procedures and protocols, and maintain an updated technology inventory.
Critical Findings:
The audit identified the following critical findings:

User Permissions: Inconsistencies in user permissions across systems, posing a risk of unauthorized access.
Controls Implementation: Gaps in controls related to accounting, endpoint detection, firewalls, intrusion detection systems, and SIEM tools.
Compliance Alignment: Current user permissions, controls, procedures, and protocols do not fully align with necessary compliance requirements.
Control of Least Privilege and Separation of Duties
Disaster recovery plans
Password, access control, and account management policies, including the implementation of a password management system
Encryption (for secure website transactions)
IDS (Intrusion Detection System)
Backups
AV software
CCTV (Closed-Circuit Television)
Locks
Manual monitoring, maintenance, and intervention for legacy systems
Fire detection and prevention systems
Policies need to be developed and implemented to meet PCI DSS and GDPR compliance requirements.
Policies need to be developed and implemented to align to SOC1 and SOC2 guidance related to user access policies and overall data safety.
Other Findings:
In addition to the critical findings, the audit revealed the following areas requiring improvement:

Procedures and Protocols: Existing procedures and protocols for accounting, endpoint detection, firewalls, intrusion detection systems, and SIEM tools.
Technology Inventory: Incomplete documentation of hardware and system access.
Time-controlled safe
Adequate lighting
Locking cabinets
Signage indicating alarm service provider
Summary and Recommendations:
To address these findings and strengthen our IT security, the following actions are recommended:

Implement the principle of least privilege and conduct regular reviews of user permissions.
Enhance controls by adopting industry best practices such as multi-factor authentication, patch management, and network segmentation.
Develop comprehensive procedures and protocols that address specific security requirements, incident response, and change management processes.
Maintain an updated inventory of technology assets to ensure accurate visibility and control.
Develop and implement policies to meet PCI DSS and GDPR compliance requirements.
Develop and implement policies to align with SOC1 and SOC2 guidance related to user access policies and overall data safety.
Address the additional findings by implementing time-controlled safes, ensuring adequate lighting, using locking cabinets, and displaying signage indicating the alarm service provider.
By implementing these recommendations, we will enhance our security posture, achieve compliance, and establish a robust cybersecurity framework to protect our critical assets and ensure business continuity.


## CyberSecurity Incident Reports 


Section 1: Identify the type of attack that may have caused this 
network interruption

After reviewing the logs in my opinion the website is being Dos attacked. The server is being bombarded with SYN requests causing the server to stop responding. This could be what is called a SYN attack.
 

Section 2: Explain how the attack is causing the website to malfunction

When the website visitors try to establish a connection with the web server, a
three-way handshake occurs using the TCP protocol. The handshake consists
of three steps:
1. A SYN packet is sent from the source to the destination, requesting to
connect.
2. The destination replies to the source with a SYN-ACK packet to accept
the connection request. The destination will reserve resources for the
source to connect.
3. A final ACK packet is sent from the source to the destination
acknowledging the permission to connect.

A SYN flood attack simulates a TCP connection and floods the server with SYN packets. The attacker floods the target server with a high volume of SYN requests, overwhelming its resources and causing a disruption in normal operations.
Initially, the attacker’s SYN request is answered normally by the web server (log items 52-54). However, the attacker keeps sending more SYN requests. The log begins to reflect the struggle the web server is having to keep up with the abnormal number of SYN requests coming in at a rapid pace. The attacker is sending several SYN requests every second. Eventually the Server  stopped responding to  legitimate employee visitor traffic.

## CyberSecurity Incident Reports Network Traffic Analysis

Part 1: Provide a summary of the problem found in the DNS and ICMP 
traffic log

The network protocol analyzer shows that when you send UDP packets and receive an ICMP response returned to your host, the results contain an error message: “udp port 53 unreachable.” Port 53 is used for DNS (Domain Name System) services. DNS is responsible for translating human-readable domain names, like yummyrecipesforme.com, into IP addresses that computers use to communicate over a network. This could be intentional to restrict DNS access or unintentional due to misconfigurations using the Firewall. It could also be the result of a DDOS because of the amount of times the error occurred.

 

Part 2: Explain your analysis of the data and provide one solution to implement

The incident occurred between 1:24pm est  and 1:28pm est when several customers contacted us to report that they were not able to access the company website, and saw the error “destination port unreachable” after waiting for the page to load. I loaded my network analyzer tool, tcpdump, and loaded the webpage again.the results contain an error message: “udp port 53 unreachable.” We are continuing to investigate the root cause of the issue to determine how we can restore access to the website. Our next steps are to configure the firewall and block ips with X number of attempts. Contact our  Internet Service Provider (ISP) or hosting provider and inform them about the ongoing DDoS attack to assist with traffic filtering or diverting malicious traffic away from your network.
