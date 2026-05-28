# Packet-Analysis-Investigations
A beginner-friendly blue-team project repository focused on packet capture analysis using Wireshark. These investigations demonstrate practical SOC analyst skills including network traffic inspection, suspicious activity identification, and incident investigation workflows.
A hands-on blue-team project repository focused on network traffic analysis, protocol investigation, and packet capture analysis using Wireshark. These labs were completed while progressing through the "Wireshark" and packet analysis learning paths on TryHackMe.
This repository demonstrates practical SOC analyst skills including:
Packet inspection and traffic analysis
Identifying suspicious network activity
Analysing protocols and PCAP files
Using Wireshark filters effectively
Investigating DNS, HTTP, TCP, and ICMP traffic
Detecting indicators of compromise within packet captures
Documenting investigation methodology and findings
Overview
This repository contains packet analysis investigations completed using Wireshark and related network analysis techniques. The purpose of these labs is to develop practical SOC analyst skills including:
Network traffic analysis
Threat detection
Packet inspection
DNS analysis
HTTP traffic investigation
Incident investigation workflows
Documentation and reporting
Tools Used
Wireshark
TCP/IP Protocol Analysis
PCAP Files
Sysmon
Windows Event Logs
Splunk 
Skills Demonstrated
Packet filtering
Network troubleshooting
Identifying suspicious traffic
DNS request analysis
HTTP request inspection
Traffic pattern analysis
Basic incident response workflows
Documentation and technical reporting
Investigation Template
Use the following template for each investigation.
Investigation: Suspicious DNS Activity
Objective
Investigate suspicious DNS traffic within a packet capture to identify potentially malicious domains and unusual traffic patterns.
Scenario
A user reported slow network performance and unusual outbound connections. Packet captures were reviewed to determine whether malicious traffic was present.
Tools Used
Wireshark
DNS protocol filters
TCP stream analysis
Investigation Steps
1. Opened PCAP File
Loaded the packet capture into Wireshark for analysis.
2. Applied DNS Filters
Used the following filter:
 dns
This isolated DNS request and response traffic.
3. Identified Suspicious Domains
Reviewed DNS queries for:
Randomized domains
High-frequency requests
Unusual top-level domains
Failed DNS responses
4. Inspected Related Traffic
Followed associated TCP streams to inspect outbound connections.
Findings
Multiple DNS requests were observed to suspicious external domains.
Repeated outbound traffic suggested automated communication.
Traffic patterns were consistent with possible command-and-control behaviour.
Indicators of Compromise (IOCs)
Type	Value
Domain	suspicious-example-domain.com
Protocol	DNS
Destination Port	53
Conclusion
Analysis identified repeated DNS requests to suspicious domains alongside unusual outbound traffic patterns. Further investigation would be recommended to determine whether the host was compromised.
