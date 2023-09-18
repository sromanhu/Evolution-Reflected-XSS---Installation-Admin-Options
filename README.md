# Evolution CMS Reflected XSS v3.2.3

## Author: (Sergio)

**Description:** Multiple Cross-site scripting (XSS) reflected vulnerabilities in the evolution v.3.2.3 installation process Admin options allows a local attacker to execute arbitrary web scripts via a crafted payload injected into the cmsadmin, cmsadminemail, cmspassword and cmspasswordconfim parameters.

**Attack Vectors:** A vulnerability in the sanitization of the cmsadmin, cmsadminemail, cmspassword and cmspasswordconfim parameters of the Database installation Admin options process allows JavaScript code to be injected.

---

### POC:


During the installation process we enter the XSS payload in the cmsadmin, cmsadminemail, cmspassword and cmspasswordconfim parameters and when we click on next, we will obtain the XSS pop-up.

### XSS Payload:

```js
'"><svg/onload=alert('admin_name')>
```


In the following image you can see the embedded code that executes the payload in the instalaltion process.

![XSS Payload Name](https://github.com/sromanhu/Evolution-Reflected-XSS---Installation-Admin-Options/assets/87250597/30cde2e8-fa76-4f22-ac5c-2d4906cea5c3)


![XSS Payload email](https://github.com/sromanhu/Evolution-Reflected-XSS---Installation-Admin-Options/assets/87250597/c10cd7e2-8237-4beb-ad8e-10bc25679eca)


![XSS Payload password y password confirm](https://github.com/sromanhu/Evolution-Reflected-XSS---Installation-Admin-Options/assets/87250597/1db7bf83-27de-42e0-9ee8-8257a8f1ce1e)


And the result will be reflected with the pop-up of the following evidence:

![XSS result Name](https://github.com/sromanhu/Evolution-Reflected-XSS---Installation-Admin-Options/assets/87250597/27da2910-aa79-4efd-ad43-017bfd8986cd)


![XSS result emailpng](https://github.com/sromanhu/Evolution-Reflected-XSS---Installation-Admin-Options/assets/87250597/842fc005-29c2-4b8c-bfd7-344e0e685172)


![XSS result password](https://github.com/sromanhu/Evolution-Reflected-XSS---Installation-Admin-Options/assets/87250597/7cc0e05e-4c47-4136-8bb5-a3d3a59ec520)


![XSS result password confirm](https://github.com/sromanhu/Evolution-Reflected-XSS---Installation-Admin-Options/assets/87250597/3f2f5cf0-1457-4ab3-bb8b-782ed0bd5ffd)


</br>

### Additional Information:

https://evo.im/

