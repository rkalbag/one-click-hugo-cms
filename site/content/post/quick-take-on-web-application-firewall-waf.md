---
title: Quick Take On Web Application Firewall (WAF)
date: 2020-12-26T19:24:09.228Z
description: A quick take on the what, why, and how of Web Application Firewalls
image: img/locked-2143493_640-272x182.jpg
---
##### Definition:

OWASP defines a Web Application Firewall (WAF) as a security solution on the web application level which – from a technical point of view – does not depend on the application itself.

##### What is it?

It is a software or hardware security solution that is meant to do the following:

1. Front-end your web application infrastructure and protect it from attacks targeted at known vulnerabilities such as Cross-site scripting, SQL injection, etc.
2. Provide an easier means of patching a known vulnerability, or new vulnerability discovered by penetration testing or other means without making changes to the application.
3. Use a ruleset based on the expected pattern of behavior of the web app to detect and prevent abnormal application requests. Typically, a WAF can learn the ruleset from profiling the application during the training stage.
4. Offload some of the functions that are common across all web applications instead of carrying them out on each individual web server. For example, session management, error logging, etc.

##### Why is it needed?

Web apps are increasingly complex and rely on different frameworks, middleware, and external APIs. Sometimes the code is not properly documented or is a wrapper around a legacy application. When security exploits are found in any of the many things that the web app builds on, it may be time-consuming or impractical to fix the app due to a variety of reasons. Even when newer more secure versions of middleware are available, there is a risk that an upgrade may break the app or need code alteration. This is when a WAF can be used to blacklist the known attack pattern that exploits the vulnerability instead of fixing the app or in the interim while the app is being fixed.

One of the criteria for meeting the security standard of the credit card industry currently in force (PCI DSS – Payment Card Industry Data Security Standard v.1.1) for example, is either a regular source code review or the use of a WAF.

##### How to make the best use of one?

1. Any security measure is effective only if properly configured and monitored. Subscribe to the WAF supplier’s service that keeps the blacklist of known attack signatures current.
2. Train and test the WAF on each new release of the app so that the WAF can create a ruleset (whitelist)
3. Check that the app can gracefully handle circumstances that can be the result of using a WAF. For example, abrupt session disconnects.
4. Integrate the WAF logs in company-wide SIEM tool
5. Monitor for false-positive closely on updates to the black or whitelists.

##### What are the key features to look for in a product?

During the product evaluation period, pay special attention to the following:

1. The ease of applying rules to patch one of the latest known exploits for one of the web frameworks you are using
2. The efficiency with which the WAF can create a whitelist by learning your application’s behavior
3. Check the product’s facility for figuring out the reason for and mitigating the occurrence of false positives by surgically altering the ruleset without disabling everything

##### Which products are the market leaders?

According to Gartner’s Magic Quadrant for August of 2017, the top 3 product leaders are:

* [Imperva](https://web.archive.org/web/20190812030727/https://www.imperva.com/)
* [F5 Networks](https://web.archive.org/web/20190812030727/https://f5.com/)
* [Akamai Technologies](https://web.archive.org/web/20190812030727/https://www.akamai.com/)

##### Additional Reading:

[https://www.owasp.org/index.php/Category:OWASP_Best_Practices:_Use_of_Web_Application_Firewalls](https://web.archive.org/web/20190812030727/https://www.owasp.org/index.php/Category:OWASP_Best_Practices:_Use_of_Web_Application_Firewalls)