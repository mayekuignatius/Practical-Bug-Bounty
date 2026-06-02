# WebApp-Attacks-Vulnerabilities-with-Mitigations

Here are some of the take aways from TCM's Security Practical Bug bounty course. As i learnt various Web app security testing TTPs on how to exploit and improve webapp security and do a report writing.
This is a brief outlook on what i learnt and did on the practical hands on labs.

| Attack/Vulnerability          | Group          | Brief Explanation                                                                 | Mitigation                                                                 |
|-------------------------------|----------------|--------------------------------------------------------------------------------|-------|-----------------------------------------------------------------------------|
| Brute Force                   | Authentication | Trying many passwords/userIDs automatically                                    | 💪    | Account lockout, CAPTCHA, rate limiting, strong passwords                   |
| Credential Stuffing           | Authentication | Using leaked credentials from other sites                                      | 🧦    | MFA, passwordless login, breach detection, block known leaked passwords     |
| Session Hijacking             | Authentication | Stealing a valid session cookie/token                                          | 🎭    | HTTP-only + Secure + SameSite cookies, short session expiry, rotate tokens  |
| Weak Password Policies        | Authentication | Allowing easily guessable passwords (e.g., "1234")                             | 1234  | Enforce complexity, length (>12), block common passwords, MFA               |
| MFA Bypass                    | Authentication | Exploiting flaws in multi-factor authentication                                | 📲    | Rate-limit MFA attempts, secure backup codes, avoid SMS if possible         |
| IDOR                          | Authorization  | Changing an ID in URL/param to access another user's data                      | 🆔    | Use indirect reference maps, server-side access control, verify user owner  |
| Privilege Escalation          | Authorization  | Vertical (user→admin) or horizontal (user→another user)                        | ⬆️    | Role-based access control (RBAC), deny by default, revalidate per request   |
| Missing Function‑Level Access | Authorization  | Directly calling admin endpoints without checks                                | 🚪    | Centralized access control middleware, annotation-based security            |
| Forced Browsing               | Authorization  | Guessing hidden URLs/resources that should be protected                        | 🧭    | Disable directory listing, use allowlists, authentication on every resource |
| Path Traversal                | Authorization  | Using `../../` to read arbitrary files                                         | 📁    | Sanitize file paths, use a safe base directory, avoid user-supplied paths   |
| XXE (XML External Entity)     | Other          | Injection attack reading local files / doing SSRF via malicious XML            | 🌐    | Disable external entities (e.g., `setFeature`, `XMLConstants`), use JSON    |
| XSS (Cross‑Site Scripting)    | Other          | Injecting malicious scripts into a trusted website (client‑side)               | 💬    | Output encoding, Content Security Policy (CSP), input validation (`<` → `&lt;`) |