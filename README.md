# unrestricted-file-upload-leads-to-stored-XSS-cross-site-scripting-stored-xss

A file upload is a serious opportunity to find cross-site scripting (XSS) to a web application.

As we know many web applications allow clients or their users to upload files for many different purposes and this is only the opportunity to find loopholes on them. so let’s see how to attack these entry points which allows files to upload there, for the purpose of finding XSS

Steps to reproduce:

1. Go to the dashboard/profile page

2. scroll down you will find the skipper license field , which contains file upload functions.

3. when I tried to upload html file it doesn't throwed an error message.

4. so i uploaded a xss file and opened that , yes it is stored and reflecting back.


![image](https://user-images.githubusercontent.com/84071887/234311684-ca7f5bb8-f17f-4fc0-a7ab-cab63d86e64b.png)

![image](https://user-images.githubusercontent.com/84071887/234311744-b8cfee20-cde2-4a29-b068-eb12f3469e92.png)

Impact :

Successful exploitation of cross-site scripting vulnerabilities allows an attacker to run arbitrary script code in the context of the affected user. This can be used to compromise the integrity of content returned by the webserver to take over a user's session, and redirect the user to a malicious website.

References:
1. https://portswigger.net/web-security/cross-site-scripting/stored
2. https://owasp.org/www-community/vulnerabilities/Unrestricted_File_Upload.
3. https://hackerone.com/reports/831703


Thank You

Have a great day!

