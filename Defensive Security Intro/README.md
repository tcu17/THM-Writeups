![image](https://github.com/user-attachments/assets/89f08a4a-15d1-4e46-acc2-72ef20ccc216)# Defensive Security Intro
## Thomas Urbain - April 7, 2025

![image](https://github.com/user-attachments/assets/839539a9-d63c-448a-810f-3ca67e8a7d0e)

### Overview

### Task 1 - Introduction to Defensive Security
In the previous room, we learned about offensive security, which aims to identify and exploit system vulnerabilities to enhance security measures. This includes exploiting software bugs, leveraging insecure setups, and taking advantage of unenforced access control policies, among other strategies. Red teams and penetration testers specialize in these offensive techniques.

In this room, we will examine its counterpart, defensive security. It is concerned with two main tasks:

1. Preventing intrusions from occurring
2. Detecting intrusions when they occur and responding properly

Blue teams are part of the defensive security landscape.

Some of the tasks that are related to defensive security include:

- User cyber security awareness: Training users about cyber security helps protect against attacks targeting their systems.
- Documenting and managing assets: We need to know the systems and devices we must manage and protect adequately.
- Updating and patching systems: Ensuring that computers, servers, and network devices are correctly updated and patched against any known vulnerability (weakness).
- Setting up preventative security devices: firewall and intrusion prevention systems (IPS) are critical components of preventative security. Firewalls control what network traffic can go inside and what can leave the system or network. IPS blocks any network traffic that matches present rules and attack signatures.
- Setting up logging and monitoring devices: Proper network logging and monitoring are essential for detecting malicious activities and intrusions. If a new unauthorized device appears on our network, we should be able to detect it.

There is much more to defensive security. Aside from the above, we will also cover the following related topics:

- Security Operations Center (SOC)
- Threat Intelligence
- Digital Forensics and Incident Response (DFIR)
- Malware Analysis

###### Question 1:
![image](https://github.com/user-attachments/assets/4902e1b3-ec66-4966-9819-4b12f0903373)

###### Answer:
![image](https://github.com/user-attachments/assets/d34cf9c7-8111-43b6-8e6f-b42711e632f3)

Explanation: In the section above, blue teams are mentioned as part of the defensive security landscape. 

### Task 2 - Areas of Defensive Security

In this task, we will cover two main topics related to defensive security:

- Security Operations Center (SOC), where we cover Threat Intelligence
- Digital Forensics and Incident Response (DFIR), where we also cover Malware Analysis

#### Security Operations Center (SOC)
A <i>Security Operations Center</i> (SOC) is a team of cyber security professionals that monitors the network and its systems to detect malicious cyber security events. Some of the main areas of interest for a SOC are:

- Vulnerabilities: Whenever a system vulnerability (weakness) is discovered, it is essential to fix it by installing a proper update or patch. When a fix is unavailable, the necessary measures should be taken to prevent an attacker from exploiting it. Although remediating vulnerabilities is vital to a SOC, it is not necessarily assigned to them.
- Policy violations: A security policy is a set of rules required to protect the network and systems. For example, it might be a policy violation if users upload confidential company data to an online storage service.
- Unauthorized activity: Consider the case where a user’s login name and password are stolen, and the attacker uses them to log into the network. A SOC must detect and block such an event as soon as possible before further damage is done.
- Network intrusions: No matter how good your security is, there is always a chance for an intrusion. An intrusion can occur when a user clicks on a malicious link or when an attacker exploits a public server. Either way, when an intrusion occurs, we must detect it as soon as possible to prevent further damage.
- Security operations cover various tasks to ensure protection; one such task is threat intelligence.

![image](https://github.com/user-attachments/assets/0c9c4058-3d63-48f8-9e26-829333aa1ccf)

#### Threat Intelligence
In this context, <i>intelligence</i> refers to information you gather about actual and potential enemies. A <i>threat</i> is any action that can disrupt or adversely affect a system. Threat intelligence collects information to help the company better prepare against potential adversaries. The purpose would be to achieve a <i>threat-informed defence</i>. Different companies have different adversaries. Some adversaries might seek to steal customer data from a mobile operator; however, other adversaries are interested in halting the production in a petroleum refinery. Example adversaries include a nation-state cyber army working for political reasons and a ransomware group acting for financial purposes. Based on the company (target), we can expect adversaries.

![image](https://github.com/user-attachments/assets/d1ef89d8-d4ae-4d7c-b7d2-8c8978980ff5)

Intelligence needs data. Data has to be collected, processed, and analyzed. Data is collected from local sources such as network logs and public sources such as forums. Data processing arranges it into a format suitable for analysis. The analysis phase seeks to find more information about the attackers and their motives; moreover, it aims to create a list of recommendations and actionable steps.

Learning about your adversaries lets you know their tactics, techniques, and procedures. As a result of threat intelligence, we identify the threat actor (adversary) and predict their activity. Consequently, we can mitigate their attacks and prepare a response strategy.

#### Digital Forensics and Incident Response (DFIR)
This section is about Digital Forensics and Incident Response (DFIR), and we will cover:
- Digital Forensics
- Incident Response
- Malware Analysis

##### Digital Forensics
Forensics is the application of science to investigate crimes and establish facts. With the use and spread of digital systems, such as computers and smartphones, a new branch of forensics was born to investigate related crimes: computer forensics, which later evolved into <i>digital forensics</i>.

In defensive security, the focus of digital forensics shifts to analyzing evidence of an attack and its perpetrators and other areas such as intellectual property theft, cyber espionage, and possession of unauthorized content. Consequently, digital forensics will focus on different areas, such as:
- File System: Analyzing a digital forensics image (low-level copy) of a system’s storage reveals much information, such as installed programs, created files, partially overwritten files, and deleted files.
- System memory: If the attacker runs their malicious program in memory without saving it to the disk, taking a forensic image (low-level copy) of the system memory is the best way to analyze its contents and learn about the attack.
- System logs: Each client and server computer maintains different log files about what is happening. Log files provide plenty of information about what happened on a system. Even if the attacker tries to clear their traces, some traces will remain.
- Network logs: Logs of the network packets that have traversed a network would help answer more questions about whether an attack is occurring and what it entails.

##### Incident Response
An <i>incident</i> usually refers to a data breach or cyber attack; however, in some cases, it can be something less critical, such as a misconfiguration, an intrusion attempt, or a policy violation. Examples of a cyber attack include an attacker making our network or systems inaccessible, defacing (changing) the public website, and data breach (stealing company data). How would you <i>respond</i> to a cyber attack? Incident response specifies the methodology that should be followed to handle such a case. The aim is to reduce damage and recover in the shortest time possible. Ideally, you would develop a plan that is ready for incident response.

The four major phases of the incident response process are:
1. Preparation: This requires a team trained and ready to handle incidents. Ideally, various measures are put in place to prevent incidents from happening in the first place.
2. Detection and Analysis: The team has the necessary resources to detect any incident; moreover, it is essential to analyze any detected incident further to learn about its severity.
3. Containment, Eradication, and Recovery: Once an incident is detected, it is crucial to stop it from affecting other systems, eliminate it, and recover the affected systems. For instance, when we notice that a system is infected with a computer virus, we would like to stop (contain) the virus from spreading to other systems, clean (eradicate) the virus, and ensure proper system recovery.
4. Post-Incident Activity: After a successful recovery, a report is produced, and the lesson learned is shared to prevent similar future incidents.

![image](https://github.com/user-attachments/assets/545f9be7-f03f-45fa-8278-54601a6e4a6c)
##### Malware Analysis
Malware stands for malicious software. <i>Software</i> refers to programs, documents, and files you can save on a disk or send over the network. Malware includes many types, such as:
- A virus is a piece of code (part of a program) that attaches itself to a program. It is designed to spread from one computer to another and works by altering, overwriting, and deleting files once it infects a computer. The result ranges from the computer becoming slow to unusable.
- Trojan Horse is a program that shows one desirable function but hides a malicious function underneath. For example, a victim might download a video player from a shady website that gives the attacker complete control over their system.
- Ransomware is a malicious program that encrypts the user’s files. Encryption makes the files unreadable without knowing the encryption password. The attacker offers the user the encryption password if the user is willing to pay a “ransom.”

![image](https://github.com/user-attachments/assets/544a7faa-b3e1-4494-83dd-04f1f7b74ca7)

Malware analysis aims to learn about such malicious programs using various means:
1. Static analysis works by inspecting the malicious program without running it. This usually requires solid knowledge of assembly language (the processor’s instruction set, i.e., the computer’s fundamental instructions).
2. Dynamic analysis works by running the malware in a controlled environment and monitoring its activities. It lets you observe how the malware behaves when running.

###### Question 2:
![image](https://github.com/user-attachments/assets/d4e6a7c5-bedc-4631-809b-68bbc90efb84)

###### Answer:
![image](https://github.com/user-attachments/assets/c56361a0-e905-4c0f-b001-8b0dd4105e06)

Explanation: A Security Operations Center, as mentioned above, is a team of cyber security professionals that monitors the network and its systems to detect malicious cyber security events.

###### Question 3:
![image](https://github.com/user-attachments/assets/ccc2f704-871a-4b5c-867d-48c504679b5e)

###### Answer:
![image](https://github.com/user-attachments/assets/374e7263-abf2-4dc1-bebe-8dea7f6c7256)

Explanation: The only option that contains two pillars of Defensive Security is Digital Forensics and Incident Response. Digital Forensics and Incident Response was also discussed in detail above.

###### Question 4:
![image](https://github.com/user-attachments/assets/72220d8f-3637-4143-93da-f1ad2f3afded)

###### Answer:
![image](https://github.com/user-attachments/assets/79f0cbc0-2629-4fc2-8cc6-557dc43ece63)

Explanation: Ransomware is classified as a malicious program that encrypts the user's files. The attacker often asks the victim to pay a "ransom" in order to get their files back.

### Task 3 - Practical Example of Defensive Security

#### The Scenario
Let us pretend you are a <i>Security Operations Center</i> (SOC) analyst responsible for protecting a bank. This bank's SOC uses a <i>Security Information and Event Management</i> (SIEM) tool, which gathers security-related information and events from various sources and presents them in one dashboard. If the SIEM finds something suspicious, an alert will be generated.

![image](https://github.com/user-attachments/assets/3c79f208-287a-4f5a-81fe-1c6c6734cc1e)

Not all alerts are malicious, however. It is up to the analyst to use their expertise in cyber security to investigate which ones are harmful.

For example, you may encounter an alert where a user has failed multiple login attempts. While suspicious, this kind of thing happens, especially if the user has forgotten their password and continues to try to log in. 

Additionally, there might be alerts related to connections from unknown IP addresses. An IP address is like a home address for your computer on the Internet—it tells other computers where to send the information you request. When these addresses are unknown, it could mean that someone new is trying to connect or someone is attempting unauthorized access.

#### Simulating a SIEM
We have prepared a simplified, interactive simulation of a SIEM system to provide you with a hands-on experience similar to what cyber security analysts encounter.

To start this simulation, please click the "View Site" button below.
![image](https://github.com/user-attachments/assets/17d040b2-c432-4863-afad-ec88d45fa805)

This action will open a "static site" on the right side of your screen. Follow the step-by-step instructions provided within the simulation to navigate through the events and locate the "flag." A flag is a series of characters with a format like this: "THM{RANDOM_WORDS}". Use this flag to answer questions from rooms here in TryHackMe, like the one below.

#### What's next?
In this room, we've discussed the different subfields (SOC, Threat Intelligence, Malware Analysis, and DFIR) and experienced firsthand how to deal with alerts in a simulated SIEM environment. While we've covered a lot, the depth and complexity of this field mean there's more to learn and explore. The lessons learned here will serve as your foundation as cyber threats evolve, demanding continuous learning, vigilance, and adaptation.

Continue learning by checking out the next room in this series, "Search Skills." This room will teach you valuable techniques for searching for information online to aid your investigations and learning.

If you want to skip ahead and learn more about the topics discussed in this room, the following rooms are recommended:
- <a href="https://tryhackme.com/r/room/introtosiem">Introduction to SIEM</a> - An Introduction to Security Information and Event Management
- <a href="https://tryhackme.com/r/room/securityoperations">Security Operations</a> - Learn about the Security Operations Center (SOC): its responsibilities, services, and data sources
- <a href="https://tryhackme.com/r/room/introductoryroomdfirmodule">DFIR : An Introduction</a> - Introductory room for the DFIR module
- <a href="https://tryhackme.com/r/room/intromalwareanalysis">Intro to Malware Analysis</a> - What to do when you run into a suspected malware

###### Question 5:
![image](https://github.com/user-attachments/assets/b29f6dba-10b2-4d4e-bde5-c89ec7749a5d)

###### Answer:

![image](https://github.com/user-attachments/assets/b890701f-e25b-4036-959e-9f2483ddf61d)

Explanation: To get the answer, we must first activate the static site by clicking the 'view site' button in this task. After doing so, you are greeted with this web page denoting a SIEM.
![image](https://github.com/user-attachments/assets/a3245fb8-165b-4a71-8881-2b0e90652341)

After making note of the suspicious IP address (143.110.250.149) by clicking on its failed logon attempt, we move onto the next page, where we can enter the IP address to scan.
![image](https://github.com/user-attachments/assets/b52e976a-2985-4d90-8480-87e632ee7eae)

After clicking the scan button, we are presented with the next page, showing where the suspicious IP address originates from.
![image](https://github.com/user-attachments/assets/ebf6ef9b-3b65-40a3-a4ab-75b8e5e87ac4)

Upon clicking 'Next', we are brought to the next page, in which we are given a choice of who to report this suspicious activity to. Knowing that we are already a part of the SOC Team, we should present our findings to the SOC Team Lead.
![image](https://github.com/user-attachments/assets/eb95e86c-2a32-4150-9a52-5c050046ed9f)

After presenting our findings to the SOC Team Lead, we are brought to a web page in order to block specific IP addresses. We can enter the suspicious IP into the text field and press the button to block it.
![image](https://github.com/user-attachments/assets/ef11875f-2f93-4668-b654-5136b5f80ff9)

After blocking the IP address, we are given our flag, <i>THM{THREAT-BLOCKED}</i>.
![image](https://github.com/user-attachments/assets/5170e104-a95a-421b-adc2-db9520b79248)

We can then close the static site and insert our flag into the answer field.
