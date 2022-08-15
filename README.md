# Url-Shorten-By-CF-Worker
A URL Shortener Powered by Cloudflare Worker with password protection feature

This project is based on the work done by xyTom/Url-Shorten-Worker. I added a small javascript to prompt password to verify the user since ideally you do not want this service to be completely public because this kind of url shorten site usually will gett abused usage as the original author faced. Again, this is a simple javascript and no security consideration. Once tested with a better code, it will be replaced right away. 
<br/>
<br/>
Cloudflare works has 100k/day requests limistation, which is enough for a small project to use. 
  
  
# Getting start

## 1. Go to Workers KV and create a namespace.
<img src="https://cdn.jsdelivr.net/npm/imst@0.0.4/20201205232805.png" width = 640>
  
  <br/>
  <br/>
  
## 2. Create a new worker.

  <br/>
  <br/>
  
  
去Worker的Settings选选项卡中绑定KV Namespace  
## 3. Bind an instance of a KV Namespace to access its data in this new created Worker.
<img src="https://cdn.jsdelivr.net/npm/imst@0.0.4/20201205232536.png" width = 640>

  <br/>
  <br/>

## 4.Where Variable name should set as `LINKS` and KV namespace is the namespace you just created in the first step.
<img src="https://cdn.jsdelivr.net/npm/imst@0.0.4/20201205232704.png" width = 640>



  <br/>
  <br/>


## 5. Copy the `index.js` code from this project to Cloudflare Worker. 
<img src="https://photos.51sec.org/file/test1-51sec/2021/09/chrome_EN7fWx3qnx.png" width = 640>



  <br/>
  <br/>

## 6. Click Save and Deploy



  <br/>
  <br/>

# Demo
  
  - https://go.hxbots.worker.dev
  
  <br/>
  <br/>
 
### Note: Because someone abuse this demo website, all the generated link will automatically expired after 24 hours. For long-term use, please deploy your own. To test this demo site, please use code 'cool'. There is a space in the prompt textbox. You might want to delete that space first then enter the password.


# Example Code for Authentication
This code has been put into index.html file. You might want to change it based on your needs.

```
<SCRIPT language="JavaScript">
var password;
var pass1="hxbots";
password=prompt('Please enter your password to view this page!',' ');
if (password!=pass1)
    window.location="https://hxbots.eu.org";
else
   {
    alert('Password Correct! Click OK to enter!');
    }
</SCRIPT>

```
<br/>

<p align="center">
  <a href="https://hxbots.eu.org">
    <img src="https://photos.51sec.org/file/test1-51sec/2021/09/chrome_m3UjIxRh8p.png">
  </a>
  <br />
</p>
<br/>




