# Project 8 - Pentesting Live Targets

Time spent: **2** hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)

## Blue

Vulnerability #1: Session Hijacking
<img src="blob:https://imgur.com/e807bcfe-b361-4e76-844b-c70539c13939"></img>
By changing the session id I can login from another browser without actually entering in username and password.

Vulnerability #2: SQL Injection
<img src="https://i.imgur.com/of4S5oa.gif"></img>
The salesperson info page is vulernable to SQL injection. I was able to view query another ID using an SQL query.


## Green

Vulnerability #1: Username Enumeration
<img src="https://i.imgur.com/xZbbYdM.gif"></img>
When incorrect password is entered for valid username, the error message is bold.
When the username is invalid, the error message is not bold.

Vulnerability #2: Stored XSS
<img src="https://i.imgur.com/Er3O35x.gif"></img>
The feedback form is vulnerable to an XSS attack that runs when the admin views the feedback page.


## Red

Vulnerability #1: Indirect Object Reference
<img src="https://i.imgur.com/QEC3JjB.gif"></img>
Changing the id parameter in the url to 10 reveals a salesperson's info that should be private or not yet public.

Vulnerability #2: Cross-Site Request Forgery
<img src="https://i.imgur.com/PsVj0Ih.gif"></img>
Using a malicious link in feedback form, admin is tricked into thinking they are logged
out of wifi and click Log Back In while unintentionally submitting an update form.

## Green
Bonus Vulnerability: Cross Site Scripting Redirect
<img src="https://i.imgur.com/yrLQmzi.gif"></img>
Using a window open script for the XSS I am able to redirect admin to Google.com for example (in same window or new window)

## Notes

Describe any challenges encountered while doing the work
