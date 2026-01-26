Onimusha | DISCORD-BASED C2 FRAMEWORK
OVERVIEW: Onimusha is a Python-powered Remote Access Tool (RAT) that utilizes Discord as a Command & Control (C2) server. By leveraging the Discord API, the agent bypasses traditional firewall restrictions and eliminates the need for port forwarding or static IP hosting.

DEVELOPER

Main Developer: Felicity

CORE CAPABILITIES
RECONNAISSANCE

!info: Extract hardware specs, IP geolocation, and user privileges.

!tasklist: View all running processes on the target machine.

SYSTEM CONTROL

!shell: Execute background CMD/PowerShell commands with real-time output.

!shutdown / !restart: Power management of the remote endpoint.

DATA EXFILTRATION

!download [path]: Upload files from the target directly to your Discord channel.

!screenshot: High-resolution silent capture of the current desktop.

PERSISTENCE & STEALTH

!startup: Installs the agent into the Windows Startup folder/Registry.

!melt: Self-destructs the agent and cleans up local logs.

TECHNICAL ARCHITECTURE
1. DEPENDENCIES The following Python modules are required for the build:

Bash
pip install discord.py requests mss opencv-python pyinstaller
2. AGENT CONFIGURATION Hardcode your credentials into the config.py or main source file:

BOT_TOKEN: Your Discord Developer Bot Token.

CHANNEL_ID: The specific ID of the Discord channel for C2 traffic.

3. COMPILATION (TO EXE) To convert the script into a standalone Windows binary:

Bash
pyinstaller --onefile --noconsole --icon=NONE agent.py
OPERATIONAL NOTES
TRANSPORT: All traffic is encapsulated within standard HTTPS Discord API calls, making it difficult for Network Intrusion Detection Systems (NIDS) to distinguish from legitimate user activity.

AV EVASION: While the Python runtime is legitimate, the compiled PE (Portable Executable) should be used in conjunction with an obfuscator or crypter to reduce detection rates by signature-based antivirus.

RATE LIMITING: Avoid flooding commands to prevent Discord API rate-limiting or Bot account flagging.

LEGAL & ETHICAL DISCLOSURE
Warning: This tool is for authorized security testing and educational purposes only. Unauthorized use of this software against systems you do not have explicit permission to access is illegal and a violation of Discord’s Terms of Service. The developer assumes no liability for misuse.
