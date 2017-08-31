<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<script src="https://apps.bdimg.com/libs/jquery/2.1.4/jquery.min.js"></script>
</head>
<body>
<form>
第一个数字：<br>
<input type="text" id="num1" value="100">
<br>
第二个数字：<br>
<input type="text" id="num2" value="200">
<br>
</form>
<button id="add">点我+</button>
<button id="sub">点我-</button>
<button id="mul">点我x</button>
<button id="div">点我/</button>
<br/><hr/>
运算结果：
<p id="result">结果将在这里显示</p>
<br/>

<script type="text/javascript">
//获取input的指并转化为数字
var a_int,b_int;
function getInputNum(){
	var a=$('#num1').val();
	var b=$('#num2').val();
	a_int=parseInt(a,10);
	b_int=parseInt(b,10);
}
$("#add").click(function(){
	getInputNum();
	var result=addition(a_int,b_int);
	$("#result").html(String(result));
})
$("#sub").click(function(){
	getInputNum();
	var result=subtraction(a_int,b_int);
	$("#result").html(String(result));
})
$("#mul").click(function(){
	getInputNum();
	var result=multiplication(a_int,b_int);
	$("#result").html(String(result));
})
$("#div").click(function(){
	getInputNum();
	var result=division(a_int,b_int);
	$("#result").html(String(result));
})
//加减乘除函数
function addition(x,y){
	return x+y;
}
function subtraction(x,y){
	return x-y;
}
function multiplication(x,y){
	return x*y;
}
function division(x,y){
	if(y==0){
		alert("0不能做除数");
		return '无法相除';
	}
	else{
		return x/y;
	}
}
</script>
</body>
</html>