# PRACTICAL BUG BOUNTY

These are some of the key takeaways from TCM Security's Practical Bug Bounty course. Throughout the course, I learned various web application security testing techniques, common vulnerabilities, and recommended mitigation strategies. The labs provided hands-on experience in identifying, exploiting, and documenting security issues.

| Vulnerability                         | Category       | Description                                                      | Mitigation                                                 |
| ------------------------------------- | -------------- | ---------------------------------------------------------------- | ---------------------------------------------------------- |
| Brute Force                           | Authentication | Automated password guessing against login forms.                 | Account lockout, rate limiting, CAPTCHA, strong passwords. |
| Credential Stuffing                   | Authentication | Using leaked credentials from previous breaches.                 | MFA, breach detection, block known compromised passwords.  |
| Session Hijacking                     | Authentication | Stealing valid session tokens to impersonate users.              | Secure cookies, token rotation, short session lifetimes.   |
| Weak Password Policies                | Authentication | Allowing simple or commonly used passwords.                      | Enforce strong password requirements and MFA.              |
| MFA Bypass                            | Authentication | Exploiting flaws in multi-factor authentication implementations. | Secure backup codes, rate limiting, stronger MFA methods.  |
| IDOR                                  | Authorization  | Accessing another user's data by modifying identifiers.          | Server-side authorization checks on every request.         |
| Privilege Escalation                  | Authorization  | Gaining higher privileges than intended.                         | RBAC, least privilege, deny-by-default policies.           |
| Missing Function-Level Access Control | Authorization  | Accessing restricted functionality without authorization.        | Centralized access control and permission validation.      |
| Forced Browsing                       | Authorization  | Accessing hidden resources by guessing URLs.                     | Authenticate and authorize access to all resources.        |
| Path Traversal                        | Authorization  | Using file path manipulation to access restricted files.         | Validate file paths and restrict directory access.         |
| XXE                                   | Other          | Exploiting XML parsers to read files or perform SSRF.            | Disable external entities and use secure parsers.          |
| XSS                                   | Other          | Injecting malicious scripts into web pages.                      | Output encoding, CSP, and input validation.                |

## Key Skills Practiced

* Web Application Reconnaissance
* Authentication Testing
* Authorization Testing
* Session Management Testing
* Input Validation Testing
* Vulnerability Reporting
* Security Mitigation Analysis
  

  <img width="785" height="604" alt="image" src="https://github.com/user-attachments/assets/0704670b-f6cf-48d3-a309-b00e6977e392" />


## Course Outcome

The course provided practical experience in identifying common web application vulnerabilities, understanding their impact, exploiting them in a controlled environment, and recommending effective remediation strategies.

