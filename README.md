# Project 8 - Pentesting Live Targets

Time spent: **5** hours spent in total

> Objective: Identify vulnerabilities in six different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)

## Blue

Vulnerability #1: SQL Injection-  In this vulnerability, I changed the end of the url of the site from id=1 to id=1' OR '1=1" --.  The next window that appears from that url displays "DATABASE QUERY NOT FOUND" suggestion that other SQL injections can be used to hack the site.

Gif: week8_3.gif


Vulnerability #2: Session Hijacking/fixation- In this vulnerability, I again changed the url.  I injected the malicious php string public/hacktools/change_session_id.php.  When reloading the page, I can now change the session id of the site.

Gif: week8_6.gif


## Green

Vulnerability #1: Username Enumeration- This vulnerability allows the hacker to see if a username already exists or not.  When loging in with a username that's already in use, the words "log-in attempt failed" will appear in bold letters.  However, when using a username that does not exist, the same message appears, but is not bolded.

Gif: week8_1.gif


Vulnerability #2: Cross-Site Scripting- In this vulnerability, a hacker is able to insert malicious scripts into the Contact Us page.  After entering an email and name, a hacker can insert code, such as <script>alert=('hello'), into the body of the supposed email they sent out.  In veiwing the Feeback page on that site, the alert message will appear.

Gif: week8_4.gif


## Red

Vulnerability #1: Insecure Direct Object Reference- Just as in the vulnerabilities in blue, I changed the url of the site.  When changing the end of te url on a salesperson's page to id=10, I am able to access the information of a salesperson that is no public.

Gif: week8_2.gif


Vulnerability #2: Cross-Site Request Forgery-  With this vulnerability in place, a hacker is able to change the CSRF token of any user on the site.  On the edit users page, a hacker can inspect the elements of that site and change the CSRF token.

Gif: week8_5.gif


## Notes

Figuring out what vulnerability we needed to use for what website was challenging.  However, after figuring that out, everything went smoothly.


