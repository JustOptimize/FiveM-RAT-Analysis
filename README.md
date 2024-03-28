# FiveM RAT Analysis

This repository contains the analysis of a RAT (Remote Access Trojan) that was found in multiple resources.
This piece of code (stage 2) is a part of a bigger RAT that is used to infect FiveM servers and gets injected into various resources.

WARNING: This code is malicious and should not be used in any way. This repository is for educational purposes only.

## Stage 2

First stage of the RAT that is used to download the second stage of the RAT from a remote server.

## Stage 3

Second stage of the RAT that is used to download the third stage of the RAT from a remote server.

## Stage 3b

Third stage of the RAT that is used to download the fourth stage of the RAT from a remote server.

## Stage 4

Finally with stage 4 RAT keeps the connection with the remote server and waits for commands.

# What is missing?

Digging deeper into the VPS that was infected, I found that the hosts file was modified to block many common antivirus websites. This was done to prevent the server from being scanned by antivirus software.

# How to prevent this?

-   Do NOT download leaked resources
-   Keep your server up to date
-   Use a firewall
-   Use a WAF (Web Application Firewall)
-   Use a good antivirus software
-   Monitor your server for any suspicious activity
-   Keep an eye on your resources for any suspicious code

# Mitigations

-   The first mitigation I put in place was to block the IP address of the server that was hosting the malicious code. This was done by adding the IP address to the firewall blacklist on the VPS. This would prevent any further communication with the server and stop the RAT from being able to download additional stages.
-   The second mitigation was to block the RAT domain in the hosts file. This would prevent the RAT from being able to communicate with the remote server and download additional stages (if the IP address was changed).
-   The third mitigation was to remove the RAT code from the resources. This was done by removing the code from the resources and restarting the server. This would prevent the RAT from being able to execute any further code on the server.
