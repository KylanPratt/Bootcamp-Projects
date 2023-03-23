# Mock Penetration Report
This project was a simulated penetration test for a fictional company Rekall LLC. An overview of the project is below:  

<h3><b>Overview of Materials </b></h3> <br>
&#x2022; PDF Report <br>
&#x2022; WebAPP YAML File <br>
&#x2022; ReadMe Guide <br>

<h3><b> Main Goal </b> </h3> <br>
&#x2022; Exploit Vulnerabilities in Rekall Corporation's Web Application, Linux Servers, and Windows Servers <br>


<h2><b> Summary of Simulation </b> </h2> <br>
<LI>Rekall Corporation sepcializes in virtual reality experience based on pictures their clients upload.
<LI>Pending their 'Go Live' event in the near future, they are in need of penetration testers to find vulnerabilities in their systems.
<UL>
<UL>
<LI>New Web Application
<LI>Several Windows Servers
<LI>Several Linux Servers
</UL>
<LI>Deliverable
<UL>
<LI>Report of vulnerabilities and mitigations.
<LI>Entire analysis available in PDF Report.
</UL>

  ![Rekall Homepage](https://user-images.githubusercontent.com/110432400/227113443-5136097d-4767-4592-b213-ab48ac3ab0a4.png)



<h2><b> Web App Findings </b> </h2> <br>

<LI> <b> Cross-site Scripting </b> </LI>
<UL>
<LI>Reflected and Stored.
  <LI> bypassed with: <pre>payload=<sscriptcript>alert("XSS")<%2Fsscriptcript> </pre>
</UL>
<LI> <b>Unsecured HTTP Response Headers</b></LI>  
<UL>
<LI>Leveraged with Burp Repeater
</UL>
<LI> <b>Local File Inclusion  </b></LI>
<UL>
<LI>Upload forms allowed for script upload.
<LI>Filter for jpg was bypassed with: <pre>filename.jpg.png </pre>
</UL>
<LI> <b>Basic SQL Injection</b>  </LI>
<UL>
<LI>Passing Boolean True Statement
</UL>
<LI> <b>Exposure of Sensitive Data</b></LI>
<UL>
<LI> Via Robots.txt 
<LI> Via HTML Source Code
</UL>
<LI> <b>Directory Traversal</b></LI>
<UL>
<LI> Via URL Parameters 
<LI> Broken Access Control - Exploited with Burp Intruder
<LI> View access to /etc/passwrd
</UL>

<LI> <b>Overall Weak User Password</b></LI>
<UL>
<LI> Bruteforced with wordlists.
<LI> Password Spraying used.
</UL>
<LI> <b>PHP Injection </b></LI>
<UL>
<LI> Leveraged via script writing
</UL>
<br>
#Complete assessment found in PDF report.
