# Netwrokwalks-b082-week4

Penetration Testing Report: Mediroza General Hospital

Target: https://medirozahospital.com


Engagement Type: Black-box Penetration Test & Vulnerability Assessment

Duration: 5 Days

Status: Completed (All Milestones 1–4)



Executive Summary

This repository documents the comprehensive black-box penetration testing assessment conducted against Mediroza General Hospital's web infrastructure (https://medirozahospital.com). The engagement evaluated the security posture of the web application, successfully executed authorized multi-stage exploitation to extract restricted patient files, identified critical internal server exposures, and formulated remediation strategies to mitigate systemic risks.


Project Milestones & Completion Summary

Milestone 1: Initial Access & Reconnaissance

Objective: Conduct target reconnaissance, identify exposed entry points, and gain unauthorized access to restricted areas of the site.

Execution: Performed thorough directory enumeration and mapping of the application structure, identifying exposed patient record directories and authentication mechanisms.

Deliverable: Verified access to restricted portal sections with authorized testing permission. clues:

Screenshot 2026-09-30 234126 Screenshot 2026-09-30 234228

Milestone 2: Data Extraction & Cryptanalysis

Objective: Locate and extract confidential patient PDF lab reports and crack their encryption.


Execution: Retrieved three encrypted patient PDF files from the target web server and successfully recovered their complete contents using tailored cryptographic analysis and wordlist attacks.

Deliverable: Recovered contents of all three patient files with full proof of access.

1st pdf *image

2nd pdf image

3rd pdf image


Milestone 3: Critical Data Exposure & Exploitation



Objective: Identify critical server exposures stemming from preliminary findings and extract confidential employee salaries and shareholder details.


Execution: Analyzed server directory behavior, explored administrative portal paths, and exposed configuration directories (/staff/) to uncover sensitive internal records.

Deliverable: Documented evidence of the server exposure along with readable summaries of internal staff salaries and hospital shareholder details.


Milestone 4: Penetration Testing Report


Objective: Compile a professional, structured penetration testing report detailing scope, methodology, findings, risk ratings, and remediation recommendations.

Execution: Structured findings into formal executive summaries, technical proofs of exploitation, and actionable hardening steps.

Deliverable: A complete, professional pentest report submitted to stakeholders.

Findings and Risk Ratings

Milestone / Finding	Vulnerability Type	Risk Rating	Status

Milestone 1	Inadequate Access Controls / Reconnaissance Exposure	High	Resolved / Exploited


Milestone 2	Weak PDF Document Encryption	Medium	Resolved / Exploited

Milestone 3	Directory AutoIndex & Sensitive Data Disclosure (Payroll/Shareholders)	Critical	Resolved / Exploited

Milestone 4	Formal Documentation & Reporting	N/A	Completed

Recommendations & Remediation

Disable Directory AutoIndex: Configure the LiteSpeed web server to disable directory listing (Options -Indexes) to prevent attackers from viewing directory contents and hidden script files like login.php.

Secure Access Controls: Implement strict, session-based authentication and parameterized database queries across all staff and administrative endpoints.
Data Encryption Standards: Ensure all sensitive internal documents, such as payroll sheets and shareholder lists, are protected with robust access control lists (ACLs) rather than relying on weak client-side file encryption.
