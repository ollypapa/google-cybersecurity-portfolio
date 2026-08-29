# Network Analysis: DNS and ICMP Traffic

## Overview

This activity involved analyzing DNS and ICMP traffic using the tcpdump network protocol analyzer.

The objective was to identify the network protocol and service affected during a cybersecurity incident involving the website:

`www.yummyrecipesforme.com`

## Problem Identified

Users were unable to access the website and received a "destination port unreachable" error.

The tcpdump log showed that DNS requests were sent using UDP to the DNS server. The DNS server responded with ICMP error messages indicating that UDP port 53 was unreachable.

Port 53 is used by DNS services.

## Analysis

The computer sent a DNS request from:

`192.51.100.15`

to the DNS server:

`203.0.113.2`

The request used UDP and was directed to port 53.

The DNS server returned an ICMP error stating:

`udp port 53 unreachable`

The same delivery error occurred multiple times.

## Possible Cause

One possible cause is that the DNS service was unavailable or that no service was listening on UDP port 53.

Because the DNS request could not be completed, the browser could not resolve the website's domain name to an IP address. This prevented the website from loading.

## Tools Used

- tcpdump
- Network protocol analysis
- DNS
- ICMP
- UDP
- TCP/IP model

## Skills Demonstrated

- Network traffic analysis
- DNS troubleshooting
- Protocol identification
- IP address analysis
- Interpreting tcpdump logs
- Identifying potential causes of network incidents
