# Phishing Email Investigation

## Overview
This project analyzes a suspicious phishing email pretending to be from PayPal. The investigation focuses on identifying phishing indicators, analyzing the malicious URL, and verifying infrastructure information using threat intelligence tools.

## Tools Used
- VirusTotal
- MXToolbox
- AbuseIPDB

## Investigation Steps

### 1. Suspicious URL Analysis
The phishing email contained the following URL:

http://security-update@paypai.com/

VirusTotal flagged this URL as malicious and identified it as part of a phishing campaign.

### 2. Email Header Analysis
Email headers were analyzed using MXToolbox.

Findings:
- SPF Authentication: Failed
- DKIM Authentication: Failed
- DMARC Record: Not found

These authentication failures indicate that the email is spoofed.

### 3. IP Address Investigation
The infrastructure IP address was analyzed.

IP Address:
185.231.21.55

VirusTotal showed no direct malicious detections, but infrastructure details revealed hosting in Spain.

### 4. AbuseIPDB Check
The IP was searched in AbuseIPDB.

Result:
- No abuse reports found
- Hosting provider: IUKANET
- Location: Valencia, Spain

Attackers often use newly registered servers that have not yet been reported.

## Conclusion
The investigation confirms this email is a phishing attempt due to:
- Fake PayPal domain
- Email authentication failures
- Malicious URL detection
- Suspicious hosting infrastructure

This investigation demonstrates the workflow used by SOC analysts to analyze phishing emails.
