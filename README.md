Social Engineering Exercises (Phishing Analysis 2)
# Phishing Analysis 2
1. Overview

       The analyzed email claims to originate from Amazon Support and informs the recipient that their account has been locked due to suspicious activity.
       The message urges the user to take immediate action by clicking a “Review Account” button within 72 hours, creating sense of urgency commonly used in phishing attacks
2. Header Analysis
   2.1. Sender Information

       Sender Name: Amazn
       Sender Address: amazon@zyevantoby.cn
   
   2.2. Recipient Information

       Recipient Email Address: saintington73@outlook.com
       The email is directly addressed to the victim’s email address and victims is using outlook email

   2.3. Subject Line

       Subject : Your Account has been locked
       The subject is used to cause alertness and pressure tp the victim to click the phishing link without a proper verification
   
   2.4. Date and Time Sent

       Date header : Wed, 14 July 2021 01:40:32 +0900
       Timestamp show the sender-declared send time and can be used for reference for phishing investigations process later

4. Email Body Analysis
   3.1. Email Content

       The body of the email contains several common phishing traits :
           - General greeting : “Hello Dear Customer”
           - Claims the account restriction due to suspicious activity
           - Threats the victim with the account limitation effects
           - Used time-based urgency “within 72 hours” to pressure victims to click the malicious link

   3.2. Social Engineering Techniques Used

       Urgency : Threat of losing account access
       Fear : Suggestion of suspicious activity
       Authority Impersonation : Pretending to be Amazon Support
       Action Pressure : Directing the user to click a button

6. Call-to-Action (CTA) Analysis
   4.1. Used CTA Button

       The attacker choose to use a CTA button to make the victim click the malicious link without caution
       Button Text : Review Account
       The primary mechanism used to redirect the victim to a malicious website to steal victim sensitive information
   
   4.2. CTA URL Extraction
   
        When the button is clicked, Microsoft Outlook rewrites the original phishing URL using Safe Links protection : 
        Link : https://emea01.safelinks.protection.outlook.com/?url=https%3A%2F%2Famaozn.zzyuchengzhika.cn%2F%3Fmailtoken%3Dsaintington73%40outlook.com&data= 
        The Safe Links URL encapsulates the original attacker-controlled destination

   4.3. Original Phishing Destination

       Decode the “url=” parameter within the Safe Links wrapper, to reveal the the real malicious destination
       Link : https://amaozn.zzyuchengzhika.cn/?mailtoken=saintington73@outlook.com 

8. Conclusion

       This email is a clear phishing attempt designed to impersonate Amazon and trick the recipient into clicking a malicious link.
       Multiple indicators such as including a spoofed sender domain, typosquatted URL, social engineering language, and malicious call-to-action can confirm the fraudulent nature of the message.
       If a user had interacted with the phishing site, their credentials or personal information could have been compromised.
