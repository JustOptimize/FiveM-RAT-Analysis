# FiveM RAT Analysis

## Overview

This repository contains an in-depth analysis of a Remote Access Trojan (RAT) found in various FiveM server resources. The analysis focuses on the second stage of the RAT, which is part of a larger, multi-stage infection process aimed at compromising FiveM servers.

> **Warning:** The code in this repository is malicious and should not be used under any circumstances. This analysis is provided solely for educational purposes.

## Features

### [Remote Code Execution (RCE)](./RCE/)

The RAT operates through a series of stages, each designed to further the infection:

- **Stage 1:** Downloads the second stage of the RAT from a remote server.
- **Stage 2:** Retrieves the third stage from the server.
- **Stage 3:** Continues by downloading the fourth stage.
- **Stage 4:** Establishes a persistent connection with the remote server, allowing for command execution.

### [Between Script Communication (BSC)](./BSC/)

This RAT also employs Between Script Communication (BSC), registering handlers for events triggered by other RAT instances. This method helps the RAT avoid detection by communicating between scripts.

## Additional Findings

During further investigation on an infected VPS, it was discovered that the hosts file had been altered to block access to common antivirus websites. This modification was likely made to prevent the server from being scanned by antivirus software.

## Prevention and Mitigation

### Prevention

To avoid similar infections on your FiveM server, consider the following precautions:

- **Avoid Downloading Leaked Resources:** Use only trusted sources for server resources.
- **Keep Your Server Updated:** Regular updates can prevent exploitation of vulnerabilities.
- **Use a Firewall:** Protect your server by blocking unauthorized access.
- **Implement a Web Application Firewall (WAF):** Add an extra layer of security for web applications.
- **Install Reliable Antivirus Software:** Ensure your server is protected by strong antivirus software.
- **Monitor Server Activity:** Regularly check for suspicious activity on your server.
- **Inspect Resource Code:** Periodically review your resources for any suspicious code.

### Mitigation

If you suspect your server has been compromised by this RAT, consider the following mitigation steps:

1. **Block the IP Address:** Add the IP address of the malicious server to your firewall's blacklist.
2. **Block the RAT Domain:** Modify the hosts file to block communication with the RAT's domain.
3. **Remove Malicious Code:** Delete the RAT code from your resources and restart the server to halt further execution.

## Timeline of Discoveries

- **March 28, 2024:** The first instance of this RAT was discovered.
- **March 29, 2024:** A second instance was found using a different domain for its backdoor (thedreamoffivem[.]com)

## Disclaimer

This repository is for educational purposes only. The information provided here should be used to improve security practices and protect servers from similar threats. Do not attempt to use the code for malicious purposes.
