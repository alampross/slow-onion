# Security is everyone's responsibility

Cybersecurity is particularly concerned with the protection of networks, computers, and systems to ensure the confidentiality, integrity, and availability (CIA) of the digital information that they contain.

-Confidentiality - authentication.

-Integrity - Hashing is an example of a technique that can be used to ensure that data has not been tampered with during transit.

-Availability - business continuity plan (BCP) and a disaster recovery plan (DRP).
    - These plans define processes and procedures to maintain or quickly restore the availability of the systems containing the information in the event of failure or disruption.

![Semantic description of image](/images/shared_resp.png)*AWS is responsible for security OF the cloud, and the customer is responsible for the security IN the cloud.*

There are three types of security controls: preventive, detective, and corrective.

| Control Type | Physical | Administrative  | Techinical  |
|:-----------------:|:-------------:|:---------------:|:---------------:|
| Preventative | ID Card Readers  | Corp. Policy must swipe cards      | Monitor data from cards   |
| Detective    | Metal detectors | Control procedures report changes to system | Antivirus software scheduled checks |
| Corrective   | backup generator if power interrupt         | continuity plan in case of... | antivirus software removing malware |


## Security Lifecycle

## Prevention
###  `Identify Assets`: Network Devices, Servers, Applications / Services
#### Refer to Network Topology Diagrams, Architecture Diagrams, System Documentation
    - Ping to discover hosts and IP addresses, use NMAP for more detailed discovery of hosts
    - AWS Systems Manager service provides an inventory function that you can use to list the managed instances in your account. You can view the ID, name, ping status (which reflects the instance’s state), platform type, and IP address.

###  `Assess vulnerabilities`: consider potential threats at the server level, network level, data level (at rest and in transit), code level, see the [CVE-common-vilnerabilities-and-exposures](https://cve.mitre.org/) for much more details
###  `Implement countermeasures`
    – Defense in depth: perimeter (IPS, Security Onion, Suricata), network (ACLs), endpoint (antivirus software), application (app firewall, monitoring and scanning), data (permissions, AWS IAM, encryption)
    - Systems Hardening (OS patches and security updated regularly, remove unused apps, monitor & control config changes) & Network Hardening (discovery: block network exploration protocols, close unused ports, maintain list of devices that have access. architecture: firewalls, IPS, network segmentation, subnets), Data Security Controls (Encryption, digital certificates, shasum, integrity, role-based access control) and Identity Mgmt (principle of least privilege, password policy, Authorization, Authentication, Accounting AAA)

## Detection
- Create and audit logs and check system whenever a change is recognized

## Response
- Containment, Eradication, Recovery, [NIST.SP.800](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-61r2.pdf)

## Analysis
- Root Cause Analysis, 5 why's. Consider any previous or potential issues and encode policy toward prevention.


## CIA Triad: Confidentiality, Integrity, Availability
[Link-CIA](https://www.fortinet.com/resources/cyberglossary/cia-triad#:~:text=The%20three%20letters%20in%20%22CIA,and%20methods%20for%20creating%20solutions)

[Adam'sLink](https://www.csoonline.com/article/3519908/the-cia-triad-definition-components-and-examples.html)
- **Confidentiality**: Encryption, Personal Identifiable Information, 
- **Integrity**: Protect data at rest and in transit, The content of message is not compromised, no alterations, additions or removals, hashes
- **Availability**: for authorized parties, reachable with redundancy, meaning the information can be access when it needs to be accessed. There is high availability and backups in place. This involves properly maintaining hardware and technical infrastructure and systems that hold and display the information. Accuracy, consistency and trustworthiness of data across operations such as capture, storage, retrieval, update and transer. Must remain unaltered by unauthorized entities during all these operations.