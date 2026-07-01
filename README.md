# FUTURE_CS_03
API Security Risk Analysis Report conducting a structured, non-intrusive security evaluation of the JSONPlaceholder public REST API using Postman and Browser DevTools. Completed for the Future Interns Cyber Security track.

# Task 3: API Security Risk Analysis Report

📌 Project Overview
This repository contains a professional API Security Risk Analysis Report evaluating the free and publicly accessible JSONPlaceholder REST API against the OWASP API Security Top 10 framework. The assessment was performed using a strictly non-intrusive, observational approach to analyze systemic vulnerabilities in authentication, access control, data exposure, and server configuration, providing actionable remediation strategies to establish a secure development baseline.

🛠️ Tools Used

* Postman: Used to issue structured HTTP GET and POST requests and inspect raw data payloads.
* Browser Developer Tools: Utilized to inspect HTTP response headers and check for infrastructure misconfigurations.
* OWASP API Security Top 10 Framework: Leveraged to categorize, map, and contextually assess industry-standard API risks.
* Microsoft Word: Used for professional layout design, formatting, and report compilation.

🔍 Key Findings Summary
The analysis successfully uncovered 8 distinct security vulnerabilities across 4 core risk areas, resulting in an overall Critical risk rating if replicated in a production environment:

1. No Authentication Required (Critical): Lack of API key, token, or session verification across all endpoints, enabling unauthenticated access to sensitive resources.
2. Broken Object Level Authorization / BOLA (Critical): Flawed authorization logic permitting unrestricted access to full user profiles by simply manipulating the integer ID in the request URI.
3. Unauthorized Data Modification (Critical): Absence of write-operation constraints allowing unauthenticated users to successfully create or inject data via POST requests.
4. Insecure Direct Object Reference / IDOR (Critical): Predictable, sequential resource identifiers that allow malicious actors to seamlessly enumerate and expose post data across different user boundaries.
5. Excessive Data Exposure (High): API payloads returning complete user data structures, including sensitive corporate and relationship information, without field filtering.
6. Sensitive Data Exposure (High): Exposure of highly critical data fields—specifically precise GPS coordinates and physical street addresses—to unauthenticated requests.
7. No Rate Limiting (High): Complete absence of request throttling or throttling blocks, opening the infrastructure to automated abuse, brute-force enumeration, and denial-of-service (DoS) conditions.
8. Missing Security Headers (Medium): Omission of foundational HTTP response security headers, including Content-Security-Policy, X-Frame-Options, X-Content-Type-Options, and Strict-Transport-Security.

📂 Deliverables Included

* `API_Security_Risk_Analysis_Report.pdf: The complete, client-ready analytical report outlining findings, impacts, and remediation priorities.
* `/screenshots: Directory containing Postman request/response captures, missing HTTP header proofs from DevTools, and data exposure logs.

*This project was completed as part of the Cyber Security Track (CS) Internship under Future Interns.*
