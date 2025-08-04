# Cyber-security Task 1 Scan Your Local Network for Open Ports

Objective:
The task was to scan my local network using Nmap and identify which devices are connected and what ports are open on those devices. This helped me understand how exposed my own network is.

tools used -> Nmap

What I Did:
1. First, I found my local IP range using `ipconfig` (I’m using Windows), which gave me something like `192.168.1.x`.
2. I used the command:nmap -sS 192.168.1.0/24
3. This scanned all devices connected to my Wi-Fi to see what ports are open.
4. Saved the scan output as a `.txt` file.
5. Based on the results, I looked up which services usually run on the open ports I found (like 80 for HTTP, 443 for HTTPS, etc.).
6. I also tried to understand what risks can happen if those ports are exposed without protection.


What I Learned:
- How port scanning works using TCP SYN.
- What open ports can reveal about a system.
- Basic use of Nmap and Wireshark.
- How attackers can take advantage of exposed ports.

summary of scan performed of NMAP

Some Devices Found:
- 192.168.1.1 → My router
- 192.168.1.3 → My personal laptop
- 192.168.1.4 → My phone

Open Ports & Their Meaning:
- Port 80 (HTTP): Found on router – this is for the router’s login page. If not secured properly, attackers can try default passwords.
- Port 22 (SSH): Not found in my case, but common on Linux machines. If open, can be brute-forced.
- Port 443 (HTTPS): Also found on router – secure web interface.
- Port 139/445: These are related to file sharing (SMB). If open, it can be risky if someone tries to access shared files.

Risks I Noticed:
- If my router’s admin panel is exposed on port 80 or 443 and not protected with a strong password, anyone on the network can try to access it.
- Devices like phones and laptops can have open ports due to apps or services – good to turn off what’s not needed.
- Open SMB or FTP ports can lead to data leakage.

My Conclusion:
I never realized how much info a simple scan could reveal about my network. After this, I checked my router settings and turned off remote access. Also planning to use a stronger Wi-Fi password.

This small task actually made me feel more aware of my own network’s security. 
Thanks for checking it out! This was fun and very useful for real-world understanding.
