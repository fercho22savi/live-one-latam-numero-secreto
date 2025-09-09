# Security Policy
Deployment and Operations Policy
Data Management Policy

Data Minimization: Since the application only handles names, no sensitive information is involved. 
However, if in the future it is planned to add email addresses or other personal data, the policy should be to collect only the data strictly necessary for the game’s functionality.

Transience: The names entered by the user should exist only during the game session. They must not be stored persistently in a database or in the browser’s local storage, unless strictly 
required for functionality. This reduces the risk of data leakage to zero.

Anonymization: If names could be considered sensitive (full names, addresses), the policy would be to anonymize or pseudonymize them in any considered storage. 
For your project, this is not necessary.

Code and Application Security Policy

Input Validation: Although the logic is simple, it is crucial to validate the data users enter into forms.
Ensure that names do not contain malicious code (such as scripts) that could be executed. While client-side JavaScript can perform some sanitization, applying proper validation is a good 
security practice.

Cross-Site Scripting (XSS) Protection: Since the application manipulates and displays user-generated content, all data must be sanitized before being rendered in the interface.
Use methods to escape special characters (such as < and >) to prevent malicious script injection. This is essential even for small-scale projects.

Dependency Management: If the project uses external libraries (even though this one is “vanilla”), the policy would be to review known vulnerabilities in those dependencies. 
Use tools like npm audit if Node.js is ever introduced for a similar project.

Deployment and Operations Policy

HTTPS: Even for an educational project, it should be deployed on a server using HTTPS to encrypt communication between the user’s browser and the server. 
This ensures that no one can intercept the names while they are being transmitted. Many free hosting services like Netlify or Vercel provide HTTPS by default.

Security Headers: Configure security-related HTTP headers in the web server. Start with essentials such as Content-Security-Policy (CSP),
which prevents XSS attacks and restricts loading of resources from untrusted sources, and X-Content-Type-Options, which prevents MIME sniffing.



## Supported Versions

Use this section to tell people about which versions of your project are
currently being supported with security updates.

| Version | Supported          |
| ------- | ------------------ |
| 5.1.x   | :white_check_mark: |
| 5.0.x   | :x:                |
| 4.0.x   | :white_check_mark: |
| < 4.0   | :x:                |

## Reporting a Vulnerability

Use this section to tell people how to report a vulnerability.

Tell them where to go, how often they can expect to get an update on a
reported vulnerability, what to expect if the vulnerability is accepted or
declined, etc.
