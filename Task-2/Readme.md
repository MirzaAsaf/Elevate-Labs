Phishing Email Analysis - Task 2

This repository contains my analysis of a phishing email as part of the Cyber Security Internship Task-2. 
The goal of this task is to identify phishing indicators using header analysis, content analysis, and link inspection.

1. Objective
Analyze a suspicious email and identify:
- Email spoofing techniques
- Phishing indicators in the content
- Suspicious links / attachments
- SPF, DKIM, DMARC authentication results
- Sender server path (Received headers)

2. Sample Phishing Email Used for This Task
- /Screenshots/Phishing Email Screenshot.png

3. Phishing Indicators Identified
  a. Spoofed Sender Email
    - support@paypaI-security.com
    - Not a real PayPal domain
    - Homograph attack (capital “I” instead of “l”)
  b. Suspicious URL
    - Fake link:
        - https://paypal.com.verify-user-security-check.com/login
    - Actual domain is:
        - verify-user-security-check.com
  c. Urgent & Threatening Language
    - “24 hours”
    - “Account suspended”
    - Typical social engineering pressure
  d. Generic Greeting
    - Legitimate services use your real name.
  e. Malicious Attachment
    - PayPal_Verification_Form.zip -> likely malware/trojan.
4. Email Header Used for Analysis
  - /Header-analysis text.txt
5. Header Analysis (SPF, DKIM, DMARC)
  - After pasting the header into Google Admin Toolbox – Message Header Analyzer, the results were: 
  - (/Screenshots/Header Analysis.jpg)
    | Authentication | Status        | Meaning                                    |
    | -------------- | ------------- | ------------------------------------------ |
    | SPF            | Fail          | Sender server is NOT authorized            |
    | DKIM           | None          | Email not digitally signed                 |
    | DMARC          | Fail          | Domain policy rejects the sender           |
    | Source IP      | 185.77.19.62  | Not a PayPal IP, suspicious foreign server |

6. Tools Used
  - Google Admin Toolbox (Header Analyzer)
  - Browser link inspection
  - Manual content analysis

7. Conclusion
  - Based on all findings, this email is confirmed to be a phishing attack using:
    a. Domain spoofing
    b. Homograph attack
    c. Misleading URLs
    d. Threat-based social engineering
    e. Malicious attachments
    f. Failed SPF/DKIM/DMARC authentication
  - This email should NOT be opened, clicked, or trusted.
  - It should be reported and deleted immediately.
