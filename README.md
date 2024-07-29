# Network-Security
Network Security Comprehension

I wanted to share my experience with the TryHackMe Network Security room. I aimed to deepen my understanding of different attack methods and gain hands-on experience in hacking into a target server in a safe virtual environment.

Brief Introduction:

A computer network consists of interconnected devices, including laptops, desktops, smartphones, and smart home devices such as washers, dryers, thermostats, and security systems.

Network security aims to safeguard data confidentiality, integrity, and availability. To achieve this, a variety of hardware and software solutions can be employed to protect end user data from potential compromises. For instance, antivirus programs and host-based firewalls, like Windows Defender in Microsoft Windows, can effectively block malicious traffic.

Enterprise networks utilize a range of hardware appliances, such as firewall appliances, to control incoming and outgoing connections by enforcing specific rules.

Intrusion Detection Systems are deployed to proactively identify potential attacks, while Intrusion Prevention Systems are implemented to thwart unauthorized access attempts and protect the network from security breaches.


Approach:
In order to carry out a successful operation, it is essential to engage in thorough planning. Gaining control requires in-depth study of the target. Lockheed Martin Cyber Kill Chain outlines a series of crucial steps to be taken before entering a network.

1. Reconnaissance - Learn about your target.
2. Weaponization - Have malicious content ready to gain remote access.
3. Delivery - Phishing email, USB flash drive, links to donation sites.
4. Exploitation - Malicious content is executed.
5. Installation - Install malware on system
6. Command and Control (C2) - Remote control over the system
7. Actions on Objectives - Data exfiltration


Exercise: 
I will briefly list the steps taken gathering information on my target machine using my Linux Box.

- nmap machineIP
- nmap scanned a report providing me confirmation that the host is up.
- Ports open were FTP 21, SSH 22, and HTTP 80
- All other ports were closed.

- I selected the FTP server.
- FTP server is used to transfer files between host.
- I logged into the FTP server with an anonymous login and it worked.
- Used the ls command to list the file contents.
- Located a file name Secret.
- Used the Get Secret.txt to download contents of the file.
- Made note of the password and exit out.

- Logged into the Root account using the password recovered from secret file.
- Used ssh root@IP and password.
- By logging on as root this gave me full control to all files.
- Used pwd which is print working directory to display my location.
- My location shows as root.
- Used ls to display all files and located a flag.

- Navigated to the home directory of root.
- Used cd /home which allowed me to change directories.
- Used ls  while in home and located a librarian folder.
- cd into the librarian folder.
- Used pwd to confirm my location.
- Used the ls to display content within the librarian folder.
- And used cat command to print the contents out.

Conclusion: 
Upon obtaining a printed copy of the contents, I successfully gained access to the librarian account, alongside the FTP server. This enabled me to realize the importance of conducting a thorough reconnaissance of the system. I discovered that identifying open ports and active processes is crucial prior to initiating any attack.
