# Web Content Accesibility Guidelines Bookmarklet
#### _A Chrome bookmarklet for checking a webpages WCAG compliance

#### By _**Jason Huels**_

## Description
_A Chrome bookmarklet for checking a webpages WCAG compliance

## Setup/Installation Requirements_
* Install XAMPP: https://www.apachefriends.org/index.html
* Clone this repository into C://XAMPP/htdocs directory
* Add a new Chrome Bookmark
* Paste this bit of code into the URL field of the bookmark: 
javascript:(     void(     function() {     var fileRef; var loaded = false;  try { loaded = checkDocumentWCAG; } catch(err) { }  if(!loaded) { fileRef = document.createElement("link"); fileRef.rel = "stylesheet"; fileRef.type = "text/css"; fileRef.href = "https://localhost/wcag/wcag.css"; document.getElementsByTagName("head")[0].appendChild(fileRef);  fileRef = document.createElement("script"); fileRef.src = "https://localhost/wcag/wcag.js"; fileRef.type = "text/javascript"; document.getElementsByTagName("head")[0].appendChild(fileRef); } else { checkDocumentWCAG(); } }() ) )
* Start your Apache server in XAMPP Control Panel
* Navigate to the webpage you would like to check and open the wcag bookmarklet

## Known Bugs
* Since I do not have a valid HTTPS certification this bookmarklet will not work with https enabled (only disable https requirements with sites you trust and be sure to re-enable after using this bookmarklet)

## Support and contact details

_jasonhuels@yahoo.com_

## Technologies Used

_JavaScript, XAMPP_

### License

*open source*

Copyright (c) 2015 **_Jason Huels_**