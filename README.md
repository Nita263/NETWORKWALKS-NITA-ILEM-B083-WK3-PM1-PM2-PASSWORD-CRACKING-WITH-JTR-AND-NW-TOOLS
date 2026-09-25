# Password cracking with Johnny The Ripper(JtR) and Networkwalks Tools (Hash Calculator and Password cracker) 
# Introduction
This report covers cracking passwords of three (3) locked PDF files with multiple password cracking tools. One module covers getting the hashes of these PDF and another covers Using the password cracker tool. Together, it shows how to use these tools to open a PDF without directly inserting their passwords.  All activities were run on Windows PC with. Every step below includes the exact tool used, the result I observed, and a screenshot as evidence.

3. Tools Used
The table below lists each tool used in this report and its purpose.
| Tools | Purpose |
| :---- | :---- |
| Johnny The Ripper(JtR) | open-source password cracking and security auditing tool primarily used by cybersecurity professionals, '<br>' systems administrators and penetration testers |

Tools	Purpose
Kali Linux & Windows	Operating systems used for reconnaissance activities.
WHOIS	Query public domain registration (name, owner, date, server).
Whatweb	Fingerprint technologies running on the website (frameworks, servers CMS, plugins, IP).
nslookup	Resolve domain name to it´s IP address usimg DNS.
curl -I	Read HTTP response headers to see the server banner, status, cookies and redirects.
Wafw00f	Detects if a Web Application Firewall is protecting the site.
dnsrecon	Enumerates all DNS records (Mail servers, SPF, TXT SRV).
Zenmap (Nmap GUI)	Scan the local subnet to find live hosts, IPs and MAC addresses.
Windows CMD	Local IP and MAC address identification
4. Activities Performed
4.1 Footprinting & Reconnaissance

I performed reconnaissance against the networkwalks.com domain using six Kali Linux tools: WHOIS, WhatWeb, Nslookup, Curl, Wafw00f and DNSRecon. Each tool was used to collect a different type of information about the target.

First, I used WHOIS to obtain publicly available domain registration information and identify the domain’s name servers. The results provided information about the domain registration and hosting infrastructure.

I then used WhatWeb to identify technologies used by the website. The results identified WordPress 7.1 and WP Download Manager 3.3.58, along with other information exposed by the website.

Using Nslookup, I resolved the domain name to its IP address. The provided result identified 192.232.216.135.

I used Curl with the -I option to inspect the HTTP response headers. This provided additional information about the web application and exposed the WordPress REST API endpoint /wp-json/.

Next, I used Wafw00f to determine whether a Web Application Firewall was protecting the website. The result showed that the site seemed to be behind a WAF or some sort of security solution.

Finally, I used DNSRecon to enumerate DNS records. The results provided information relating to name servers (Hostgator.com), mail servers, SPF/TXT records, service records and DNS software information.
