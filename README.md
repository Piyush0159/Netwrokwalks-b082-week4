
    **Penetration Testing Report: Mediroza General Hospital**

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



<img width="925" height="578" alt="662428601-23e02b5b-2497-4fba-9179-905013cbe6cf" src="https://github.com/user-attachments/assets/359abe2a-5e70-4a6e-b20b-613072fdf669" />



<img width="1622" height="636" alt="662428985-f8f856f4-0cc5-4386-ad8d-47fdd6128530" src="https://github.com/user-attachments/assets/8fe53b4a-23e7-4b87-9621-e45e889070d1" />


Milestone 2: Data Extraction & Cryptanalysis

Objective: Locate and extract confidential patient PDF lab reports and crack their encryption.


Execution: Retrieved three encrypted patient PDF files from the target web server and successfully recovered their complete contents using tailored cryptographic analysis and wordlist attacks.

Deliverable: Recovered contents of all three patient files with full proof of access.

1st pdf 


<img width="1091" height="770" alt="662431425-2a997ce4-3808-495c-b148-b18c078cacdd" src="https://github.com/user-attachments/assets/bf70b010-2b9b-479e-9e2a-07272ae55155" />



2nd pdf 


<img width="1196" height="672" alt="662432178-80a2d2fb-3024-48dd-965f-ddfdfcee7771" src="https://github.com/user-attachments/assets/bd010ae4-a00d-4c72-a35a-934bfb4669ee" />




3rd pdf 


<img width="1920" height="922" alt="662433093-7d2994d3-f22a-4306-b5a7-9f307e465018" src="https://github.com/user-attachments/assets/42e8b760-00cc-45c2-b111-c1f4f70afb20" />



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
