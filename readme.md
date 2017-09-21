readme
=

Tags: 文档内容说明 DailyGoals 减重打卡表 倒计时 html&css笔记索引

---

## daily goals
**功能**  
制定目标并打卡  
**完成度**  
未完成，等掌握好了前端知识再来完善。

---

## loseweight sheet
**功能**
减重打卡表
**完成度**
100%
**用法**
1. 12.21-loseweight.js中&nbsp;*data数组*&nbsp;存放的是原始数据，可以按格式增添/删减；
2. *现重*&nbsp;每天都会有变化，要手动填入；
3. 按下&nbsp;*更新*&nbsp;按钮，会自动计算&nbsp;*减掉*&nbsp;多重，*剩下*&nbsp;多重要减，从&nbsp;*入表日期*&nbsp;开始计算&nbsp;*坚持*&nbsp;天数；
4. *删除*&nbsp;按钮可以删除该行，但不会改变&nbsp;*data数组*&nbsp;里的值。

---

## Countdown Timer
**功能**
简易倒计时，两个版本差不多，v1版在点击click后，对时分秒的内容做了一些判断。
**完成度**
100%
**用法**
三个圆圈，从左到右依次填入&nbsp;时&nbsp;分&nbsp;秒，单击`click`开始倒计时，如果超出当前时间会提示`吉时已过`。
**遇到的小问题**
1. 当时间到的时候提示的是`时间已过`，而不是`已到`；
2. 当出现提示时，时间停留在00：00：01，点确定后，才会变成00：00：00。

### 问题的根源
**关键词**
主线程 队列
1.alert是阻塞型代码，不点确定会阻止所有代码执行；
2.代码的改变和重绘到浏览器页面上是两件事，比如`function fn1(){var str=0; oSp.innerHTML=str;alert(str);}`;代码oSp.innerHTML先于alert执行，但浏览器页面上显示的oSp.innerHTML会在alert之后改变，因为一般情况下，浏览器页面重绘至少要16毫秒。

**解决办法**
用`setTimeout(function(){alert(str);},16)`，让页面有时间重绘后，再执行代码`alert(str);`

**小知识**

* *队列*
正在执行的代码称作主线程，在主线程执行的过程中响应的其他代码，会放到队列尾部，等主线程执行完了会**从前往后**执行队列里的代码。即：
`在队列中，最先进入队列的函数最先被执行。`
* *栈 stack*
stack堆叠，函数累积起来，**最上面的（后出现的）**先结束执行。即：
`在栈中，最后开始的函数最先结束。`
* *函数的调用关系是栈，事件的触发顺序是队列*
```
//栈：函数fn先出现，fn1后出现先结束。
function fn(){
    fn1();
};

```

## html&css note index
<br>
**功能**
**功   能**功能中间有两个tab<br>
**功       能**功能中间有四个tab
<br>
    自学慕课网HTML+CSS基础课程时记的豆瓣笔记的索引&nbsp;行首有两个tab
    <br>
    自学慕课网HTML+CSS基础课程时记的豆瓣笔记的索引&nbsp;行首有两个tab
    <br>
自学慕课网HTML+CSS基础课程时记的豆瓣笔记的索引&nbsp;行首没有两个tab
<br>
**完成度**
已完成
**用法**
大标题都是链接，可以点进去转到豆瓣日记看具体内容








