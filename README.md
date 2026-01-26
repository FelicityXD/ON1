# Project Name: Onimusha

### **Discord-Based Remote Access Trojan or C2 Framework**

---

## Project Description

**Onimusha** is an experimental Remote Access Trojan (RAT) that leverages the **Discord API** as a communication backbone. By utilizing a Discord Bot token and a dedicated server (Guild), administrators can issue commands and receive data exfiltration directly through a Discord channel.

This project is designed to demonstrate how legitimate cloud services can be used for asynchronous Command and Control (C2).

---
## Architecture

* **Controller:** A Discord Server where you interact with the Bot.
* **Transport:** HTTPS (Discord API).
* **Agent:** A Python-based client compiled into a standalone `.exe` for deployment on Windows endpoints.

---

## Features
* **Real-time Interaction:** Interact with your agent and gain the machine.
* **Secure Token Integration:** Communication is tied to a specific **Bot Token** and **Channel ID**.
* **File Exfiltration:** Download files from the target machine directly into your Discord chat.





---

## Setup & Deployment

## 1. Discord Configuration

1. Create a new application on the [Discord Developer Portal](https://www.google.com/search?q=https://discord.com/developers/applications).
2. Create a **Bot**, enable the **Message Content Intent**, and copy the **Bot Token**.
3. Create a private Discord Server and copy the **Channel ID** where you want the logs to appear.

## 2. Configuration

Edit the `EXE` to include your credentials:

```python
TOKEN = "YOUR DISCORD BOT TOKEN"
SERVER = "YOUR SERVER ID"
OWNER = "YOUR OWNER ID"

```
## Command Overview

| Command | Action |
| --- | --- |
| `.man` | Displays all available administrative commands. |
| `.cmd <command>` | Executes a command in the background CMD/PowerShell. |
| `.ss` | Captures the current active display. |
| `.fuckoff` | Terminates the agent session on the target. |
| `.arise` | Makes the agent to connect to the server. |

---

## Ethical Disclosure

**Disclaimer:** This tool is strictly for authorized red-teaming. The use of this tool for accessing systems without explicit permission is a violation of international law and the Discord Terms of Service.

---

