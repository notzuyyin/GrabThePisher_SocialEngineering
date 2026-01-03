# GrabThePisher_SocialEngineering
GrabThePisher Blue Team Challenge

## Student Information
**Name:** Nurul Iman Zuyyin Binti Mohd Zanizam

**Course:** [BCSS]

 **Institution:** UniKL MIIT
 
 **Platform:** CyberDefenders



## Room Information
 **Room Name:** GrabThePisher Lab
 
 **Difficulty:** Easy 
 
 **URL:** https://cyberdefenders.org/blueteam-ctf-challenges/grabthephisher/
 
## Tools Used
 Sublime Text Editor


---
## Objective
This lab focuses on analysing a cryptocurrency phishing kit to identify exfiltration methods, 
extract critical IOCs, 
and gather threat actor intelligence using local logs and Telegram APIs.

**Question 1:** 
Which wallet is used for asking the seed phrase? 

As for this question,each file was checked using "grep -R wallet" to search for any
file that contains "wallet" information.

**Answer**: 'Metamask'
![Q1 Correct]



### Investigation Performed
- Analyzed phishing email headers
- Identified malicious URLs and sender domains
- Correlated indicators of compromise (IoCs)

### Evidence


### Outcome
The phishing attempt was successfully identified and mitigated by
recognizing social engineering indicators such as spoofed sender addresses
and malicious links.
