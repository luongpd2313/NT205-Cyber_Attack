# Develop Breach Attack Simulation: Web Application Firewall
## Descriptions
- This project simulates various hacker techniques to bypass Web Application Firewall (WAF) and attack web application. By analyzing vulnerability scanner reports, we identify missing WAF rules and propose mitigation strategies to enhance web security.
## Tasks
- Vulnerability scanning: Use tools like Acunetix, ZAP, Qualys, Nessus... to scan applications through WAF, detect unblocked vulnerabilities (SQLi, XSS...).
- Create a report: Describe in detail the remaining vulnerabilities to improve the rules on WAF to prevent.
- Exploit vulnerabilities generated from tools above.
# Instruction

We can use scripts located in script directory to install everything automatically
------

> Important: All the scripts need to run as `root` privileges 

> Tested on Kali Linux 2023.1

## `setup-php8.2-environment.sh` (Optional)

If your PHP version is not support `php-gd`, you may need a latter version. This script will ask you to indicate the **old PHP version** (for removing) and **new PHP version** (for installing), I suggest that the new one should be `8.2` (the latest at this time) and the old one is your choice. 

## `dvwa-full-install.sh`

Fully installing the *DVWA web server*, there would be a phase to prompt you to enter password to **MySQL database** as `root` user. By default, use the same password for `root` user in system. The final result comes up like below:

<p align="center"> <img src="../image/result_final_dvwa.png"> </p>

Also, the status for each phase should be all `OK`

## `modsec-basic-install.sh`

Install the basic configuration for ModSecurity. When finished, try to SQLi the web. For example:

<p align="center"> <img src="../image/test_sqli.png"> </p>

Also, the status for final phase should be all `OK`. 
