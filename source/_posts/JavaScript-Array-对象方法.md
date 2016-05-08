---
title: JavaScript Array 对象方法
date: 2016-05-07 16:30:24
tags:
---
#JavaScript Array对象常用方法
 ### 一、 concat() 方法用于连接两个或多个数组。
 1. 语法：arrayObject.concat(arrayX,arrayX,......,arrayX)
     arrayX    必需。该参数可以是具体的值，也可以是数组对象。可以是任意多个。
 2. example
 ```javaScript
   var a = [1,2,3]
   for (i=4;i<10;i++) {
        a = a.concat(i)
   }
 console.log(a)
 //输出a：[1,2,3,4,5,6,7,8,9]
 ```
 ```html
 <script type="text/javascript">

var arr = new Array(3)
arr[0] = "George"
arr[1] = "John"
arr[2] = "Thomas"

var arr2 = new Array(3)
arr2[0] = "James"
arr2[1] = "Adrew"
arr2[2] = "Martin"

var arr3 = new Array(2)
arr3[0] = "William"
arr3[1] = "Franklin"

document.write(arr.concat(arr2,arr3))

</script>
输出：George,John,Thomas,James,Adrew,Martin,William,Franklin
```
### 二、join()方法用于把数组中的所有元素放入一个字符串。
1. 语法：arrayObject.join(separator)
    separator  可选。指定要使用的分隔符。如果省略该参数，则使用逗号作为分隔符。
2. example
   ```javasceipt
      var a = ["hello","nice","to","meet","you"]
      console.log(a.join(";"))
      //输出：hello;nice;to;meet;you
   ```
### 三、pop()方法用于删除并返回数组的最后一个元素。
1. 语法：arrayObject.pop()
    返回值  arrayObject的最后一个元素。
2. example
   ```html
 <script type="text/javascript">
var arr = new Array(3)
arr[0] = "George"
arr[1] = "John"
arr[2] = "Thomas"
document.write(arr)
document.write("<br />")
document.write(arr.pop())
document.write("<br />")
document.write(arr)
</script>
     输出：George,John,Thomas
     Thomas
     George,James   
   ```
### 四、shift()方法用于把数组的第一个元素从其中删除，并返回第一个元素的值。
1. 语法：arrayObject.shift()
2. example
   ```javasceipt
      var a = ["hello","nice","to","meet","you"]
      console.log(a.shift())
      //输出：hello
   ```   
### 五、push() 方法可向数组的末尾添加一个或多个元素，并返回新的长度。
1. 语法：arrayObject.push(newelement1,newelement2,....,newelementX)
       newelement1:必需，要添加到数组的第一个元素。
        newelementX：可选
2. example
   ```javasceipt
      var a = ["hello","nice","to","meet","you"]
      console.log(a.push("Lili"))
      //输出：6
   ```
### 六、reverse() 方法用于颠倒数组中元素的顺序。
1. 语法：arrayObject.reverse()
2. example
   ```html
<script type="text/javascript">
var arr = new Array(3)
arr[0] = "George"
arr[1] = "John"
arr[2] = "Thomas"

document.write(arr + "<br />")
document.write(arr.reverse())
</script>
    输出：George,John,Thomas
    Thomas,John,George
   ```
### 七、slice() 方法可从已有的数组中返回选定的元素。
1. 语法：arrayObject.slice((start,end)
    start  必需。规定从何处开始选取。如果是负数，那么它规定从数组尾部开始算起的位置。也就是说，-1 指最后一个元素，-2 指倒数第二个元素，以此类推。
    end   可选。规定从何处结束选取。该参数是数组片断结束处的数组下标。如果没有指定该参数，那么切分的数组包含从 start 到数组结束的所有元素。如果这个参数是负数，那么它规定的是从数组尾部开始算起的元素。
2. example   
   ``` javaScript
   var a = ["how","are","dsf","abc"]
   console.log(a.slice(2))
    //输出 ["dsf", "abc"]
    ```
### 八、sort() 方法用于对数组的元素进行排序。
1. 语法：arrayObject.sort(sortby)
        sortby  可选。规定排序顺序。必须是函数。
2. example
   ```html
<script type="text/javascript">
var arr = new Array(6)
arr[0] = "10"
arr[1] = "5"
arr[2] = "40"
arr[3] = "25"
arr[4] = "1000"
arr[5] = "1"
document.write(arr + "<br />")
document.write(arr.sort())
</script>
    输出：10,5,40,25,1000,1
         1,10,1000,25,40,5
   ```
   ```javaScript
var arr = new Array(6)
arr[0] = "10"
arr[1] = "5"
arr[2] = "40"
arr[3] = "25"
arr[4] = "1000"
arr[5] = "1"
console.log(arr.sort(function(a,b) {})
["10", "5", "40", "25", "1000", "1"]
arr.sort(function(a,b) {
   return parseInt(a)-parseInt(b)
}))
  //输出：["1", "5", "10", "25", "40", "1000"] 
   ```
### 九、splice() 方法向/从数组中添加/删除项目，然后返回被删除的项目。
  1. 语法：arrayObject.splice(index,howmany,item1,.....,itemX)
  2. example
    ```html
<script type="text/javascript">

var arr = new Array(6)
arr[0] = "George"
arr[1] = "John"
arr[2] = "Thomas"
arr[3] = "James"
arr[4] = "Adrew"
arr[5] = "Martin"
document.write(arr + "<br />")
arr.splice(2,3,"William")
document.write(arr)
</script>
  输出：George,John,Thomas,James,Adrew,Martin
       George,John,William,Martin
   ```
   
### 十、toString() 方法可把数组转换为字符串，并返回结果。
  1. 语法：arrayObject.toString()
  2. example
    ```html
<script type="text/javascript">
var arr = new Array(3)
arr[0] = "George"
arr[1] = "John"
arr[2] = "Thomas"
document.write(arr.toString())
</script>
输出：George,John,Thomas
```
### 十一、unshift() 方法可向数组的开头添加一个或更多元素，并返回新的长度。
    1. 语法：arrayObject.unshift(newelement1,newelement2,....,newelementX)
    2. example
    ```html
<script type="text/javascript">
var arr = new Array()
arr[0] = "George"
arr[1] = "John"
arr[2] = "Thomas"
document.write(arr + "<br />")
document.write(arr.unshift("William") + "<br />")
document.write(arr)
</script>
    输出：George,John,Thomas
            4
         William,George,John,Thomas
    ```
### 十二、valueOf() 方法返回 Array 对象的原始值。
     语法：arrayObject.valueOf()
    
    
    
   
   