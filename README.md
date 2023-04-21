<h1 align="center" paddin> МИНИСТЕРСТВО НАУКИ И ВЫСШЕГО ОБРАЗОВАНИЯ РОССИЙСКОЙ ФЕДЕРАЦИИ ФЕДЕРАЛЬНОЕ ГОСУДАРСТВЕННОЕ БЮДЖЕТНОЕ ОБРАЗОВАТЕЛЬНОЕ УЧРЕЖДЕНИЕ ВЫСШЕГО ОБРАЗОВАНИЯ «САХАЛИНСКИЙ ГОСУДАРСТВЕННЫЙ УНИВЕРСИТЕТ»</h1>

<p align="center">Лабораторная работа №8 "JavaScript" </p>

<p align="right">Выполнил: Рогаль Сергей Александрович</p>
<p align="right">Проверил: Соболев Е. И.</p>

<p align="center">г. Южно-Сахалинск <br> 2023 год</p>

<h2 align="center">Введение</h2>
<p align="justify">JavaScript — это язык программирования, который используют для написания frontend- и backend-частей сайтов, а также мобильных приложений.JS поддерживают все популярные браузеры. Во frontend-части сайтов язык используют для создания интерактива (анимаций, всплывающих форм, автозаполнения), так как он связан с HTML и CSS и может ими манипулировать. В backend-части с языком JavaScript работают на платформе Node.js. С ее помощью, например, разрабатывают серверные веб-приложения и подключают библиотеки. В поисковике Google на JavaScript работает строка автозаполнения, а Netflix, Uber, eBay используют его в своем backend. Уже 6 лет JS — самый популярный язык среди разработчиков по версии GitHub.
</p>

<h2 align="center">Цели и задачи</h2>
<palign="justify">Цели: решить задачи с применением языка JavaScript</p>
<palign="justify">Задачи: применить технологии JavaScript.</p>

<h2>Решение задач</h2>
<p>1</p>
<pre>
<script>
var str = 'fgfggg'
alert(str[0]);
</script>
</pre>
<p>2</p>
<pre>
<script>
function func(a,b,c,d)
{
	var res="";
	res=res+b+a+c+a+d;
	return res;
}
alert(func('*','1','b',"1c"));
</script>
</pre>
<p>3</p>
<pre>
<script>
class Node {
    constructor(data) {
        this.data = data; 
        this.left = null;  
        this.right = null; 
    }
}
class BinarySearchTree {
    constructor() {
        this.root = null; 
    }
insert(data) {
    let newNode = new Node(data);
    if (this.root === null) {
        this.root = newNode;
    } else {
        this.insertNode(this.root, newNode); 
    }
}
insertNode(node, newNode) {
    if (newNode.data < node.data) {
        if (node.left === null) {
            node.left = newNode;
        } else {
            this.insertNode(node.left, newNode);
        }
    } else {
        if (node.right === null) {
            node.right = newNode;
        } else {
            this.insertNode(node.right, newNode);
        }
    }
}	
helpSum(node)
{
var sum=0;
if (node==null) return 0;
sum+=node.data;
sum += this.helpSum(node.left) + this.helpSum(node.right);
return sum;
}	
treeSum()
{
  
  if(this.root === null) return 0;
  var sum = this.helpSum(this.root);
  return sum; 
}	

}	
var tree = 	new BinarySearchTree();
tree.insert(1);
tree.insert(2);
tree.insert(3);
tree.insert(4);
tree.insert(5);
alert(tree.treeSum());	
</script>
</pre>
<p>4</p>
<pre>
div {
width: 200px; 
height: 100px;
background: blue;
border-radius: 100px/50px;
}
</pre>
<p>5</p>
<pre>
<script>
var array = [new Date(2021, 5, 21), new Date(2021, 4, 21), new Date(2023, 4, 21)];

for(let j=0; j<array.length-1; j++){
for (let i=0; i<array.length-1; i++)
{
	if (array[i]<=array[i+1])
	{
		let temp = array[i];
		array[i]=array[i+1];
		array[i+1] = temp;
	}
}
}
for (let i=0; i<array.length; i++)
{
	console.log(array[i].toString());
}
</script>
</pre>
<p>6</p>
<pre>
<script>
function EqualTwoStrings(str1, str2)
{
	str2+="";
	var len = str1.length;
	if (len<str2.length)
	{
		len = str2.length;
		let temp = str1;
		str1=str2;
		str2 = temp;
	}
	for (let i=0; i<str1.length; i++)
	{
		if (!str2.includes(str1[i])) 
		{			
			return false;
		}
	}
	return true;
}

function EqualStrings()
{
	var res = true;
	var i = 0;
	var len = arguments.length;
	while (res & i<arguments.length-1)
	{
		res = EqualTwoStrings(arguments[i],arguments[i+1])
		i++;	
	}
	if (res) alert("Строки состоят из одинаковых символов");
	else alert("Строки состоят из разных символов");
}
EqualStrings('кот','ток','окт');
</pre>
<p>7</p>
<pre>
<script>
var maxSum=101*50;
var array;
var sum=0;
for (let i=0; i<array.length; i++)
	{
		sum+=array[i];
	}
alert('Потеряли число' maxSum-sum);
</script>
</pre>
<p>8</p>
<pre>
var array = [7,5,4,2,6,3];

for(let j=0; j<array.length-1; j++){
for (let i=0; i<array.length-1; i++)
{
	if (array[i]<=array[i+1])
	{
		let temp = array[i];
		array[i]=array[i+1];
		array[i+1] = temp;
	}
}
}
for (let i=0; i<array.length; i++)
{
	console.log(array[i].toString());
}
</pre>
<p>9</p>
<pre>
<script>
function ToPolish(str)
{
    let temp = str.split(' ');
    let operands = [];
	let x,y;
    for(let i = 0; i < temp.length; i++)
    {
        switch(temp[i])
        {
            case "+":
                let sum = 0;
                 x =  operands.pop();
				 y =  operands.pop();
                    sum = x+y;
                operands.push(sum);
                break;
            case "-":
                 x =  operands.pop();
				 y =  operands.pop();
                let dif = x-y;
                operands.push(dif);
                break;
            case "*":
                let mult = 1;
                 x =  operands.pop();
				 y =  operands.pop();
                mult = x*y;
                operands.push(mult);
                break;
            case "/":
                 x =  operands.pop();
				 y =  operands.pop();
				let div =x/y;
                operands.push(div);
                break;
            default:
                operands.push(parseInt(temp[i]));
                break;
        }
    }
    return operands.pop();
}
 console.log(ToPolish("2 2 + 2 *"));
</script>
</pre>
<p>10</p>
<pre>
<script>
  function Palindrom(str)
{
    str = str.replaceAll(" ","");
	str = str.toLowerCase();    
    for(let i = 0; i < Math.floor(str.length / 2); i++)
    {
       if(str[i] != str[str.length - (i+1)])
            return false;
    }
    return true;
}
alert(Palindrom('А роза упала на лапу Азора'));
</script>
</pre>
<h2 align="center">Вывод</h2>
<p align="justify">Таким образом, я закрепил навык работы с JavaScript, лучше стал ориентироваться в нём, все поставленные цели были выполнены. </p>
