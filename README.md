<div align="center">

## Creating StyleSheets dynamically using javascript


</div>

### Description

Creates StyleSheets Dynamically
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Sanjeev Kaushik](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/sanjeev-kaushik.md)
**Level**          |Advanced
**User Rating**    |3.6 (25 globes from 7 users)
**Compatibility**  |
**Category**       |[\.JS files](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/js-files__2-77.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/sanjeev-kaushik-creating-stylesheets-dynamically-using-javascript__2-2979/archive/master.zip)

### API Declarations

<html>
<head>
<meta author="Sanjeev" content="creating dynamic style sheets">
<meta name="ProgId" content="FrontPage.Editor.Document">
<title>Creating StyleSheets Dynamically</title>
&lt;script language=javascript>
var mysheets = new Array();
var i = 0, x = 230, y = 150
var n = 1
function addit(){
	mysheets[i] = document.createElement("div")
	with(mysheets[i].style)	{
		width = 100
		position = "absolute"
		cursor = "hand"
		height = 30
		backgroundColor = "maroon"
		left = x
		top = y
	}
	mysheets[i].innerHTML = "<font color=ivory>&lt;marquee> Sanjeev Kaushik</marquee></font>"
	document.body.appendChild(mysheets[i])
	mysheets[i].onclick = addit
	i++
	y += 50
}
function removeit(){
	if(mysheets.length == 0)
		return;
	lastItem = mysheets[mysheets.length -1]
	document.body.removeChild(lastItem)
	mysheets[mysheets.length -1] = null
	tempArr = new Array()
	for(i=0;i<mysheets.length;i++) {
		if(mysheets[i] != null)
			tempArr[i] = mysheets[i]
	}
	mysheets = tempArr
	y -= 50
}
var mytimer
function init() {
	if(n < 5) {
		mytimer = setTimeout("init()",1000)
		addit()
	}else if (n < 9) {
		mytimer = setTimeout("init()",1000)
		removeit()
	}else {
		clearTimeout(mytimer)
		n = 0
		return false
	}
	n++
}
</script>
</head>
&lt;body onload="init()">
<b>Hi Friends,</b>
<br>
<font color=maroon>
Here is the way, how you can create style sheets dynamically. By this you can do make tree structure, directory structure or animation game. This is mere an idea.
</font>
<div align=center id=mya1 title="Add an element" style="position:absolute;left:200;top:100;width:80;background-color:red;cursor:hand" onClick="addit()">
Add
</div>
<div id=mya2 align=center title="Remove an element" style="position:absolute;left:300;top:100;width:80;background-color:green;cursor:hand" onClick="removeit()">
Remove
</div>
</body>
</html>


### Source Code

```
<html>
<head>
<meta author="Sanjeev" content="creating dynamic style sheets">
<meta name="ProgId" content="FrontPage.Editor.Document">
<title>Creating StyleSheets Dynamically</title>
<script language=javascript>
var mysheets = new Array();
var i = 0, x = 230, y = 150
var n = 1
function addit(){
	mysheets[i] = document.createElement("div")
	with(mysheets[i].style)	{
		width = 100
		position = "absolute"
		cursor = "hand"
		height = 30
		backgroundColor = "maroon"
		left = x
		top = y
	}
	mysheets[i].innerHTML = "<font color=ivory><marquee> Sanjeev Kaushik</marquee></font>"
	document.body.appendChild(mysheets[i])
	mysheets[i].onclick = addit
	i++
	y += 50
}
function removeit(){
	if(mysheets.length == 0)
		return;
	lastItem = mysheets[mysheets.length -1]
	document.body.removeChild(lastItem)
	mysheets[mysheets.length -1] = null
	tempArr = new Array()
	for(i=0;i<mysheets.length;i++) {
		if(mysheets[i] != null)
			tempArr[i] = mysheets[i]
	}
	mysheets = tempArr
	y -= 50
}
var mytimer
function init() {
	if(n < 5) {
		mytimer = setTimeout("init()",1000)
		addit()
	}else if (n < 9) {
		mytimer = setTimeout("init()",1000)
		removeit()
	}else {
		clearTimeout(mytimer)
		n = 0
		return false
	}
	n++
}
</script>
</head>
<body onload="init()">
<b>Hi Friends,</b>
<br>
<font color=maroon>
Here is the way, how you can create style sheets dynamically. By this you can do make tree structure, directory structure or animation game. This is mere an idea.
</font>
<div align=center id=mya1 title="Add an element" style="position:absolute;left:200;top:100;width:80;background-color:red;cursor:hand" onClick="addit()">
Add
</div>
<div id=mya2 align=center title="Remove an element" style="position:absolute;left:300;top:100;width:80;background-color:green;cursor:hand" onClick="removeit()">
Remove
</div>
</body>
</html>
```

