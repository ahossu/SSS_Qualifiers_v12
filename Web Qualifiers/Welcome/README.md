Link: http://141.85.224.116:8081/.
Inspecting the page the following part of the site is revealed: ```static/css/main.css```.

This page has the following comment: ```/* The first part of the flag is: "FFF{rirel_" */```.

When inspecting the main page appears:
```<p style="margin-top:0;display:inline;float:left">Here is the second part of the flag:</p>```
```<p id="hidden" style="margin-left:5px;display:inline:float:right">svyr_</p>```.

In the following code I found another page:
```
<script type="text/javascript" language="javascript">  
var versionUpdate = (new Date()).getTime();  
var script = document.createElement("script");  
script.type = "text/javascript";  
script.src = "/static/hidden.js?v=" + versionUpdate;  
document.body.appendChild(script);  
</script> 
```

In ```/static/hidden.js?v=``` I found: ```The third part of the flag is: "unf_```

The last part of the flag is in this hidden image: ```<P id="invisible"><img src="static/logo.png") }}"></P>``` and we find: ```srryvatf```.

Combining this parts of the flag it results: ```FFF{rirel_svyr_unf_srryvatf}```.

After this I observed that the letters are shifted and I used [ROT13](https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,false,13)&input=RkZGe3JpcmVsX3N2eXJfdW5mX3Nycnl2YXRmfQ) to find the final flag.

The flag is: ```SSS{every_file_has_feelings}```.