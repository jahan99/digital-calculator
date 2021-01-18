# digital-calculator
<!DOCTYPE html>
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
<title>Untitled Document</title>
<style>
#calculator
{
height:auto;
width:auto;
border: 3px solid black; 
display:inline-block;
}
input[type="button"]
{
height:40px;
width:18%;
padding: 22px;
background-color: white;

}
input[type="text"]
{
height:30px;
width:100%;
padding: 40px;
border-bottom: 2px solid grey;
text-align: right;

}

</style>
<script>
var value1;
var OP;
var value2;
var result;
function f(x)
{
document.getElementById("t1").value+=x;
value1=document.getElementById("t1").value;
}
function g(y)
{
OP= y;
value2=value1;
document.getElementById("t1").value="";
}
function eq()
{
if(OP=="+")
{
result=Number(value1)+Number(value2);
}
else if(OP=="-")
{
result=value2-value1;
}
else if(OP=="/")
{
result=value2/value1;
}
else if(OP=="*")
{
result=value1*value2;
}
else
{ 
alert("no operator selected");
}
document.getElementById("t1").value=result;
}
function h()
{
document.getElementById("t1").value="";
}
</script>
<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>
	<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.3/umd/popper.min.js" integrity="sha384-ZMP7rVo3mIykV+2+9J3UJ46jBk0WLaUAdn689aCwoqbBJiSnjAK/l8WvCWPIPm49" crossorigin="anonymous"></script>
	<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/js/bootstrap.min.js" integrity="sha384-ChfqqxuZUCnJSK3+MXmPNIyE6ZbWh2IMqE241rYiqJxyMiZ6OW/JmZQ5stwEULTy" crossorigin="anonymous"></script>
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css" integrity="sha384-MCw98/SFnGE8fJT3GXwEOngsV7Zt27NXFoaoApmYm81iuXoPkFOJwJ8ERdknLPMO" crossorigin="anonymous">
</head>
<body>
	<section id="calculator">
<form>
<input type="text"id="t1"/><br />
<input type="button"value="C"onclick="h()"  style="background-color: rgba(0,0,0,0.2);" />
<input type="button"value="/"onclick="g(this.value)" style="background-color: rgba(0,0,0,0.2);"/>
<input type="button"value="%"onclick="g(this.value)" style="background-color: rgba(0,0,0,0.2);"/>
<input type="button"value="%"onclick="g(this.value)" style="background-color: grey"/><br>
<input type="button"value="7"onclick="f(this.value)" />
<input type="button"value="8"onclick="f(this.value)" />
<input type="button"value="9"onclick="f(this.value)" />
<input type="button"value="*"onclick="g(this.value)" style="background-color: grey"/><br />
<input type="button"value="4"onclick="f(this.value)" />
<input type="button"value="5"onclick="f(this.value)" />
<input type="button"value="6"onclick="f(this.value)" />
<input type="button"value="-"onclick="g(this.value)" style="background-color: grey"/><br />
<input type="button"value="1"onclick="f(this.value)" />
<input type="button"value="2"onclick="f(this.value)"  />
<input type="button"value="3"onclick="f(this.value)"  />
<input type="button"value="+" onclick="g(this.value)" style="background-color: grey" /><br />
<input type="button"value="0"onclick="f(this.value)" />
<input type="button"value=" "onclick="f(this.value)" />
<input type="button" value="."onclick="f(this.value)" />
<input type="button"value="="onclick="eq()" style="background-color: yellow" />

</form>
</section>
</body>
</html>
