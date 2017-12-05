# SillyStroy
基本步骤：

1、在index.html的目录下新建一个文件，命名为main.js。
2、通过添加<script>标签，将外部的 JavaScript 文件应用到你的 HTML 中。

初始化变量和函数:

1、从原始的文件中，复制“1. COMPLETE VARIABLE AND FUNCTION DEFINITIONS”标题下的所有代码，并粘贴到你本地的 main.js 文件中。然后你就有了三个变量，分别代表着，"Enter custom name" 文本框(customName),  "Generate random story" 按钮 (randomize), 和 HTML body 底部的<p> 元素（生成的故事将会复制到这个 story 变量中）。另外，你还会得到一个叫做randomValueFromArray()函数，这个函数需要一个数组作为参数，然后随机返回数组中的一个元素。
2、现在看看原始文件中的第二部分 — "2. RAW TEXT STRINGS"。这一部分包含了一些字符串，这些字符串会输入进我们的项目。你需要将这些包含进 main.js 文件中的变量中去。
    在 storyText 变量中保存第一个长长的字符串。
    在 insertX 数组中保存第一组字符串（包含三个字符串）。
    在 insertY 数组中保存第二组字符串（包含三个字符串）。
    在 insertZ 数组中保存第三组字符串（包含三个字符串）。
    
加上事件处理器并且将函数补充完整：

现在回到原始文件。
复制"3. EVENT LISTENER AND PARTIAL FUNCTION DEFINITION"标题下面的代码并粘贴到你本地的 main.js 文件中。这样就：
给 randomize 变量增加了一个“点击”时间监听器。也就是说，当按钮白点击时，result( ) 函数就会运行。
给你的代码加上了一个部分完成的 result( ) 函数定义。剩下的任务就是完成函数里面的代码，让它正常工作。
将result()函数补充完整：
  1、声明一个叫做 newStory 的变量，并将它的值设置为storyText。这样，每次按下按钮之后，函数运行的时候就会生成一个新的随即笑话。如果我们直接改变 storyText 的话，我们永远只能够生成一个新的故事。
  2、声明三个变量： xItem, yItem, 和 zItem，并且另他们的值等于randomValueFromArray(insertX)，randomValueFromArray(insertY)和randomValueFromArray(insertZ)。
  3、接下来我们需要将 storyText 中的placeholder — :insertx:, :inserty:, and :insertz: — 置换成 xItem, yItem, and zItem 中保存的字符串。你可以使用字符串中专门的函数方法 — 每一次都使 newStory 变成执行了该方法后的值。这样每一次按下按钮后，这些placeholder就会变成随机产生的字符串。在给你一点提示，这种方法每次只会置换它找到的第一个 placeholder，因此你需要执行三次这个方法。
  4、在第一个 if 代码块中增加另一个字符串置换操作，将 ‘Bob’ 变用户输入的用户名。
  5、在第二个 if 代码块中，我们要检查 UK 是否被勾选。如果被勾选，我们需要将重量和温度从美式单位 weight and temperature 的值转化为英式单位 stones and centigrade 下的值。
      查找 pounds 和 stone，farenheit 和 centigrade 的转换等式。
      在定义了变量 weight 的那一行代码中， 将 pounds 下的94通过一个计算表达式转化为 stone 下的值。并且将单位' stone'添加到通过 Math.round() 函数获得整数后面。
      在定义了变量 temperature 的那一行代码中， 将 farenheit 下的94通过一个计算表达式转化为 centigrade 下的值。并且将单位' centigrade'添加到通过 Math.round() 函数获得整数后面。
      就在上面的变量定义下，增加两个字符串置换操作，将 '94 farenheit' 置换成为变量 temperature 的值，将 '300 pounds' 置换成为变量 weight 的值。
  6、最后，在函数的倒数第二行，将变量 newStory 的值赋值给变量 story.textContent。
提示
