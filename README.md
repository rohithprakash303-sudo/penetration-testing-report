Overview

This project presents a penetration testing assessment conducted in a controlled academic environment, focusing on identifying vulnerabilities across network services, web applications, and administrative interfaces.
The objective was to evaluate the security posture of a simulated IT infrastructure by analysing exposed services, outdated technologies, and misconfigurations, and demonstrating how these weaknesses could be exploited through a structured attack chain.

Objectives

Identify vulnerabilities in network and web services
Analyse misconfigurations and outdated technologies
Assess potential real-world security impact
Construct a multi-stage attack chain

Tools & Techniques

Nmap (Port & service enumeration)
Wireshark (Network traffic analysis)
Burp Suite (Web vulnerability analysis)
ike-scan (VPN configuration analysis)
Manual enumeration techniques

Key Findings

The assessment identified several critical vulnerabilities, including:
Outdated OpenSSH (v5.3) vulnerable to known exploits
VPN using IKEv1 Aggressive Mode, exposing credentials to offline attacks
Unencrypted GlobalProtect portal (HTTP) vulnerable to MITM attacks
Exposed Webmin administrative interface with weak security controls
Outdated MySQL (v5.1.73) with critical vulnerabilities
Vulnerable jQuery (v3.4.1) enabling XSS attacks
IIS server allowing TRACE method, enabling Cross-Site Tracing (XST)
Outdated DD-WRT firmware, enabling network pivoting

Security Impact

The environment was classified as CRITICAL risk due to:
Weak encryption protocols (SHA1, DH Group 2)
Public exposure of administrative interfaces
Lack of HTTPS and secure headers
Use of unsupported and outdated software

Attack Chain Summary

A realistic attack path was constructed:
Exploitation of VPN (IKEv1 Aggressive Mode)
Credential compromise via brute-force attack
Access to internal network
Exploitation of exposed Webmin interface
Privilege escalation to administrative control
Lateral movement via vulnerable router (DD-WRT)
Data access through exposed MySQL database
This demonstrates how multiple low-level vulnerabilities can combine into a full system compromise.


Project Structure

Full penetration testing report (PDF)
Supporting screenshots and evidence
Analysis of vulnerabilities and attack chain

⚠️ Disclaimer
This project was conducted in a controlled academic environment for educational purposes only. No real systems were targeted or exploited.
