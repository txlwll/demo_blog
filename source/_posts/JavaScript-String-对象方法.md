---
title: JavaScript String 对象常用的方法
date: 2016-05-07 13:47:04
tags:
---
### charAt() 方法可返回指定位置的字符
1. 语法：stringObject.charAt(index)
index（表示字符串中某个位置的数字，即字符在字符串中的下标。）
2. example
 ```javascript
    var str="Hello world!"
    console.log(str.charAt(3))
```
### indexOf() 方法可返回某个指定的字符串值在字符串中首次出现的位置
1. 语法
stringObject.indexOf(searchvalue,fromindex)
   searchvalue   规定需检索的字符串值
   formindex  字符串中开始检索的位置；值可以是0~stringObject.lenght-1
2.  example
  ```javascript
     var str = "abcdc"
     console.log(str.indexOf(e)    
     console.log(str.indexOf(b)
     console.log(str.indexOf(c,3)
     //以上代码输出分别是：-1，1，4
```
     
### replace() 方法用于在字符串中用一些字符替换另一些字符，或替换一个与正则表达式匹配的子串。
1. 语法：stringObject.replace(regexp/substr,replacement)
2.  example
  ```html
<script type="text/javascript">
var str="Visit Microsoft!"
document.write(str.replace(/Microsoft/, "W3School"))
</script>
输出：Visit W3School!
```
   ```html
<script type="text/javascript">
var str="Welcome to Microsoft! "
str=str + "We are proud to announce that Microsoft has "
str=str + "one of the largest Web Developers sites in the world."
document.write(str.replace(/Microsoft/g, "W3School"))
</script>
输出：Welcome to W3School! We are proud to announce that W3School
has one of the largest Web Developers sites in the world.
```
### slice() 方法可提取字符串的某个部分，并以新的字符串返回被提取的部分。
1. 语法：stringObject.slice(start,end)
   star 要抽取的片断的起始下标。如果是负数，则该参数规定的是从字符串的尾部开始算起的位置。也就是说，-1 指字符串的最后一个字符，-2 指倒数第二个字符，以此类推。
   end  紧接着要抽取的片段的结尾的下标。如果该参数是负数，那么它规定的是从字符串的尾部开始算起的位置。
2.  example
  ```html
<script type="text/javascript">
var str="Hello happy world!"
document.write(str.slice(6))
</script>
输出：happy world!
```
  ```html
<script type="text/javascript">
var str="Hello happy world!"
document.write(str.slice(6,11))
</script>
输出：happy
```
### substr() 方法可在字符串中抽取从 start 下标开始的指定数目的字符。
1. 语法：stringObject.substr(start,length)
   star 要抽取的子串的起始下标。必须是数值。如果是负数，那么该参数声明从字符串的尾部开始算起的位置。也就是说，-1 指字符串中最后一个字符，-2 指倒数第二个字符，以此类推。
   lenght  可选。子串中的字符数。必须是数值。如果省略了该参数，那么返回从 stringObject 的开始位置到结尾的字串。
2.  example
  ```html
<script type="text/javascript">
var str="Hello world!"
document.write(str.substr(3))
</script>
输出：lo world!
```
  ```html
<script type="text/javascript">
var str="Hello world!"
document.write(str.substr(3,7))
</script>
输出：lo worl
```
### substring() 方法用于提取字符串中介于两个指定下标之间的字符。
1. 语法：stringObject.substring(start,stop)
   star   必需。一个非负的整数，规定要提取的子串的第一个字符在 stringObject 中的位置。
   lenght  可选。一个非负的整数，比要提取的子串的最后一个字符在 stringObject 中的位置多 1。
2.  example
  ```html
<script type="text/javascript">
var str="Hello world!"
document.write(str.substr(3))
</script>
输出：lo world!
```
  ```html
<script type="text/javascript">
var str="Hello world!"
document.write(str.substr(3,7))
</script>
输出：lo w
```

### split() 方法用于把一个字符串分割成字符串数组。
  1. 语法：stringObject.split(separator,howmany)
   separator  必需。字符串或正则表达式，从该参数指定的地方分割 stringObject。
   howmany  可选。该参数可指定返回的数组的最大长度。如果设置了该参数，返回的子串不会多于这个参数指定的数组。如果没有设置该参数，整个字符串都会被分割，不考虑它的长度。
   >如果把空字符串 ("") 用作 separator，那么 stringObject 中的每个字符之间都会被分割。
  2.  example
  ```html
<script type="text/javascript">
var str="How are you doing today?"

document.write(str.split(" ") + "<br />")
document.write(str.split("") + "<br />")
document.write(str.split(" ",3))

</script>
输出：lo world!How,are,you,doing,today?
H,o,w, ,a,r,e, ,y,o,u, ,d,o,i,n,g, ,t,o,d,a,y,?
How,are,you
```
  ```html
"2:3:4:5".split(":")	//将返回["2", "3", "4", "5"]
"|a|b|c".split("|")	//将返回["", "a", "b", "c"]
```   