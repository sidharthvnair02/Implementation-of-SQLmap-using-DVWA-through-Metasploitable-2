#                                 Implementation-of-SQLmap-using-DVWA-through-Metasploitable-2
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------
                                                   Information Security IA_2
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Group members: Rahi Patil - 16010120038 Sidharth Nair - 16010120032
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Introduction:

Kali Linux: A Linux distribution with Debian roots called Kali Linux is made for penetration testing and digital forensics. Offensive Security oversees and provides maintenance for it.Kali Linux offers 600 penetration-testing applications, including Armitage, Nmap, Wireshark, John the Ripper, sqlmap, Aircrack-ing, Burp, and OWASP ZAP. It was created by Offensive Security employees Mati Aharoni and Devon Kearns through the rewriting of BackTrack, a Linux distribution they had previously used for information security testing and which was based on Knoppix. The Hindu deity Kali served as the name's inspiration.

SQLmap: SQLmap is an open-source penetration testing tool that automates the process of detecting and exploiting SQL injection vulnerabilities in web applications. It can automatically detect the type of database management system (DBMS) used by a web application, and can use various techniques to enumerate and extract data from the database. It also supports a wide range of DBMSs, including MySQL, Oracle, Microsoft SQL Server, PostgreSQL, and more. SQLmap can be used by security professionals and penetration testers to assess the security of web applications and identify SQL injection vulnerabilities that could be exploited by attackers. It can also be used by developers to test their own applications for SQL injection vulnerabilities.

DVWA: DVWA is a PHP/MySQL web application designed to be vulnerable to various types of web attacks, such as SQL injection, cross-site scripting (XSS), and command injection. It is designed for educational purposes to help people learn about web application security and how to defend against common web attacks. DVWA can be downloaded and installed on a local machine or hosted on a web server and includes various security levels, ranging from low to high. It also includes a number of challenges and exercises to help users develop their skills in identifying and exploiting vulnerabilities in web applications. Overall, DVWA is a useful tool for anyone interested in learning about Web application security and penetration testing.

Metasploitable2: Metasploitable2 is a virtual machine designed to be vulnerable to various types of attacks, making it a useful tool for testing and practicing penetration testing techniques. It is based on Ubuntu and includes vulnerable services and applications that can be exploited by attackers. It is available for free download and can be run on a virtual machine platform such as VMware or VirtualBox. Users can use various tools and techniques, such as Metasploit, to exploit the vulnerabilities and gain access to the system. It is designed to be used for educational and training purposes only, and should not be used for any illegal or malicious activities.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Stepwise Demonstration:

First we need to download SQLmap using the following command: sudo apt install sqlmap
![image](https://user-images.githubusercontent.com/82643868/227793227-301bc794-2bf8-4c7a-925d-640b78160cca.png)

To setup dvwa for SQLmap we are using metasploitable 2. Here is the demonstration of the same.
![image](https://user-images.githubusercontent.com/82643868/227793253-6e2152e1-960c-4b5a-8977-5d932ce286e5.png)

Click on DVWA.
We get the access to dvwa.
![image](https://user-images.githubusercontent.com/82643868/227793302-a2a8d75c-cdbc-435c-9f6d-c47b9522a9b9.png)

Click on DVWA Security and set the security level to low.
![image](https://user-images.githubusercontent.com/82643868/227793395-25c13265-cab9-44c9-9d1d-4acc88ec81c6.png)

After setting security to low , we click on SQL injection and set the ID as 1.
![image](https://user-images.githubusercontent.com/82643868/227793479-5d09a115-956a-4ec4-a829-56d0fd32fc8c.png)

Click on inspect to view the php session id
![image](https://user-images.githubusercontent.com/82643868/227793639-f8bd430e-b2cd-4ac8-9b65-1096a4b142e5.png)

We run the following command in the terminal : sqlmap -u "url" --cookie "php session id and security"
the output is as follows:
![image](https://user-images.githubusercontent.com/82643868/227793856-aa2929b6-f708-4e83-8275-10d267b308eb.png)

dbs is used to enumerate database :
run the command: sqlmap -u "url" --cookie "php session id and security"--dbs






