# Cyber-Security-Task
VULNERABILITY SCAN RESULT
Starting Nmap 7.80 ( https://nmap.org ) at 2026-03-15 22:26 UTC
Nmap scan report for testphp.vulnweb.com (44.228.249.3)
Host is up.
rDNS record for 44.228.249.3: ec2-44-228-249-3.us-west-2.compute.amazonaws.com

PORT     STATE    SERVICE       VERSION
21/tcp   filtered ftp
22/tcp   filtered ssh
23/tcp   filtered telnet
80/tcp   filtered http
110/tcp  filtered pop3
143/tcp  filtered imap
443/tcp  filtered https
3389/tcp filtered ms-wbt-server

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 3.93 seconds
I scanned testphp.vulnweb.com using an online scanner.
i found open Port 80 (HTTP) and Port 443(HTTPS). 
The server is running an old version og Nginx.
Analysis:
​Port 80 (HTTP): This port is open and unencrypted. Traffic sent over this port can be intercepted by attackers.
​Port 3306 (MySQL): Having a database port open to the public internet is a major security risk. It could lead to unauthorized access to user data or SQL injection attacks.
​Recommendation: Close all unnecessary ports and ensure Port 80 redirects to Port 443 (HTTPS) for encrypted communication.

PHISHING ANALYSIS
Subject: URGENT: Security Breach Detected on Your Account!
From: IT Security Desk <security-alert@service-verification-portal.net>
Message: Dear Valued User, Our system has detected an unauthorized login attempt on your account. To restore your access, you must verify your identity immediately by clicking the button below: [ VERIFY ACCOUNT NOW ] (Link: http://login-check-secure.xyz/update-credentials) Note: If you do not complete this verification within 2 hours, your account will be permanently deactivated.
​Key Red Flags (Indicators of Compromise):
​Suspicious Sender Address: The email address service-verification-portal.net is not an official company domain.
​Hidden URL: The button link points to a .xyz website instead of a secure, official portal.
​Artificial Urgency: The "2-hour deadline" is a psychological trick to force the user to act quickly without checking the facts.
​Generic Greeting: Using "Valued User" instead of my specific name is a sign of a mass-distributed scam.
I found there to be fake sender address, hiddenlink URL and extreme sense of urgency(panic and pressure).
