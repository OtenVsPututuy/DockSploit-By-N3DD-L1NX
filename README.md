🐳 DockSploit – Docker Remote API Exploitation Framework
BY: N3DD X L1NX

![image](https://github.com/user-attachments/assets/64cd474b-103a-4e92-a746-80a12d04d58f)

🔥 Overview
DockSploit is a post-exploitation and red team tool tailored for penetration testers, bug bounty hunters, and security researchers to exploit Docker daemons that are exposed over TCP port 2375 — a common misconfiguration that can lead to full system compromise.

Port 2375 is often unintentionally left open by developers or administrators during testing or when deploying containerized environments without proper TLS authentication. When exposed, it grants unauthenticated root-level access to the host via Docker commands. DockSploit leverages this vulnerability with a sleek, user-friendly terminal interface, giving the attacker remote access to containers, live shell interaction, and the ability to dump MySQL databases directly from compromised containers.

🛠️ Features
📡 Auto-detect exposed Docker API on port 2375

🔍 Enumerate all running and stopped containers

🐚 Gain interactive shell access inside any container

💾 Dump all MySQL databases if the container is running a MySQL service

🔒 Does not require installing on target — all remote via Docker API

📚 What Makes This Vulnerability Dangerous?
The Docker Remote API on port 2375 is unauthenticated by default unless secured with TLS. If exposed publicly, anyone can:

List and inspect containers

Read environment variables (which may contain credentials)

Execute commands as root in containers

Mount host volumes or escape the container

Replace legitimate images with backdoored ones

Deploy persistent reverse shells or crypto miners

DockSploit automates the initial foothold by enabling fast container inspection and command execution, which can escalate to full host compromise depending on how the container is configured.

⚠️ Legal Disclaimer
This tool is intended for educational and authorized penetration testing purposes only. Unauthorized access to systems that you do not own or have explicit permission to test is illegal and punishable by law. The developer is not responsible for any misuse or damage caused by this tool.
