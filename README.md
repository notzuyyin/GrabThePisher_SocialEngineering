# GrabThePisher_SocialEngineering
GrabThePisher Blue Team Challenge

## Student Information

**Name:** Nurul Iman Zuyyin Binti Mohd Zanizam

**Group:** L01-B05

**Platform:** CyberDefenders



## Room Information
**Room Name:** GrabThePisher Lab
 
 **Difficulty:** Easy 
 
 **URL:** https://cyberdefenders.org/blueteam-ctf-challenges/grabthephisher/
 
 **Tools Used:** Sublime Text Editor


## Objective
This lab focuses on analysing a cryptocurrency phishing kit to identify exfiltration methods, 
extract critical IOCs, 
and gather threat actor intelligence using local logs and Telegram APIs.


### Question 1: Which wallet is used for asking the seed phrase? 
As for this question,each file was checked using "grep -R wallet" to search for any
file that contains "wallet" information.

**Answer**: 'Metamask'

![Q1 Correct] (found metamask.png)

### Question 2: What is the file name that has the code for the phishing kit?
From the "grep -R wallet" command, the file that contains "wallet" information is  "metamask.php". 

**Answer**: 'metamask.php'

![Q2 Correct] (qs 2 , grep Ri wallet.png) 

### Question 3: In which language was the kit written?
The file extension indicate the kit written language. 

**Answer**: 'PHP'

![Q3 Correct] (qs 2, grep Ri wallet.png)


### Question 4: What service does the kit use to retrieve the victim's machine information?

When opening the metamask.php file, the following code was noticed : 

$request = file_get_contents("http://api.sypexgeo.net/json/" . $_SERVER['REMOTE_ADDR']);

Sypexgeo.net service is the database used to find geographical information that is based on the IP address. 


**Answer**: 'Spex Geo'

![Q4 Correct] (geo smtg.png)


### Question 5: How many seed phrases were already collected?

Review log.txt, which is contains in the metamask.php file.While reviewing the content, three seed phrases can be seen. 

**Answer**: '3'

![Q5 Correct] (3 seed phrases.png) 



### Question 6: Could you please provide the seed phrase associated with the most recent phishing incident?

**Answer**: 'father also recycle embody balance concert mechanic believe owner pair muffin hockey'

![Q6 Correct] (3 seed phrases.png) 


### Question 7: Which medium was used for credential dumping?

From Question 5 , the image shows the usage of $filename in order to dump the credentials on Telegram 

**Answer**: 'Telegram'

![Q7 Correct] (token.png)



### Question 8: What is the token for accessing the channel?

The token can be seen in the metamask.php file when it is being reviewed. 

**Answer**: '5457463144:AAG8t4k7e2ew3tTi0IBShcWbSia0Irvxm10'

![Q8 Correct] (token.png) 



### Question 9: What is the Chat ID for the phisher's channel?

**Answer**: '5442785564'

![Q9 Correct] (token.png)


### Question 10: What are the allies of the phish kit developer?

In the metamask.php file it contains multi-line comments, where the name is mentioned. 

**Answer**: 'j1j1b1s@m3r0'

![Q10 Correct] (geo smtg.png)




### Investigation Performed
- The email header was analysed
- The malicious URLs and sender domains was identified 
- Correlated indicators of compromise (IoCs)


### Conclusion : 
The phising attempt was identified successfully. It is mitigated through 
recognising social engineering indicators like malicious links and spoofed
sender adresses. 
