# unrestricted-file-upload-leads-to-stored-XSS-cross-site-scripting-stored-xss

Summary:

When I was testing the domain, I came across the subdomain https://static.gc.apple.com/  Which showed me an Access denied error. So I tried typing random words in the URL and I saw that it was redirecting me to this page "This static.gc.apple.com page can’t be found No webpage was found for the web address". 

Then I injected ";" this symbol to the end of the URL, it is reflected on the page.

Using this bypass method I was able to inject content to the page after the ";" symbol.

So that means it is vulnerable to Text injection or content spoofing.

 Content spoofing, also referred to as content injection, "arbitrary text injection" or virtual defacement, is an attack targeting a user made possible by an injection vulnerability in a web application. When an application does not properly handle user-supplied data, an attacker can supply content to a web application, typically via a parameter value, that is reflected back to the user. This presents the user with a modified page under the context of the trusted domain.


Like other domains of apple with the same issue, stopped me from doing it, but this didn't. For ex: " https://streamingaudio.itunes.apple.com/ --> this domain too has the same issue, access denied error. But when you inject any text it will stop me and throw an error.

Browser used:
chrome

Affected Resource(URL):
https://static.gc.apple.com/

Steps to reproduce
1. Go to https://static.gc.apple.com/ you will see an Access Denied error on the page.
2. In the URL type anything after the slash, and it will be redirected to the page(No webpage was found for the web address)
3. Now using ; this symbol at the end of the URL. These can be bypassed.
4. Text after ; will be reflected on the page.

Expected results
Access Denied
You don't have permission to access this content.


Actual results
Access Denied
You don't have permission to access "http://static.gc.apple.com/;Contentspoofingby_sharan" on this server.


Payload
WeareundermaintenacesorryfortheinconveniencehappenYoucanaccesstheresourcehereiewww.attacker.com


POC IMAGE :
https://drive.google.com/file/d/1ijf922qVKOL4DmyEknEAiRdMZL7DTS76/view?usp=share_link

PLEASE VIEW THE POC IMAGE ATTACHED FOR A DETAILED VIEW

