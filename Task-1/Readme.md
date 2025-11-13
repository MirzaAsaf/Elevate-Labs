Task 1 – Local Network Port Scanning (Cybersecurity Internship)

Objective
Perform a TCP SYN scan on my local network using Nmap and analyze open ports, services, and potential security risks.

Tools Used
- Nmap
- Wireshark (optional)

Steps Performed
1. Installed Nmap from the official website.
2. Found my local IP using `ipconfig`.
3. Identified network range: 192.168.x.0/24.
4. Ran a TCP SYN scan: nmap -sS 192.168.x.0/24
5. Ran service/version detection: nmap -sS -sV 192.168.x.0/24
6. Saved scan output to `Scan Results.txt`.
7. Identified open ports on devices in the network.
8. Analyzed risks associated with ports like 135, 139, 445, etc.

Findings
->Example open ports found:
- 135 (RPC) – Windows remote communication service  
- 139 (NetBIOS) – Legacy Windows file-sharing  
- 445 (SMB) – Windows file-sharing protocol  
- 443 (HTTPS) – Secure web service  
- 80 (HTTP) – Web server  

Security Risks:
- RPC (135) can be used for remote exploitation if unpatched.
- SMB (445) is commonly targeted by ransomware.
- NetBIOS (139) can leak device information.
- HTTP (80) can expose outdated web services.
- Any unnecessary open port increases attack surface.

Screenshots Included
- Nmap scan output
- Device-specific port scan results

All screenshots are stored in the `/Screenshots` folder.

Output Files
Stored in the `/Scans` folder:
- Scan Results.txt

Conclusion
This task helped me understand:
- How network reconnaissance works
- How open ports reveal active services
- The importance of securing unnecessary ports
- How tools like Nmap and Wireshark complement each other

Author
Mirza Asaf
