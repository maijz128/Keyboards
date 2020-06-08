# Capslock+

# 概述

- 简介：Capslock+是一个加强 Capslock 键的功能，以提高效率的工具。
- 版本：3.1.0 | 2020-04-25 by 陈俊凯
- [官网](https://capslox.com/capslock-plus/)
- 源码：[GitHub](https://github.com/wo52616111/capslock-plus)

------

# 了解 Capslock+

如果你还不清楚 Capslock+ 有什么用，建议先看看这里：[Capslock+ 有什么用](https://capslox.com/capslock-plus/what-is-the-use-of-capslock-plus/)

它图文并茂地介绍了 Capslock+ 有哪些功能，以及你可以怎样去使用这些功能。而这下面的说明比较无聊（但详尽），你可以看完那篇东西再回来这里。或者是忘记了某些功能的时候按下`Capslock+F1`来打开这页查看。

以下是其他网站（用户）发表的介绍文章：

- Topbook：[CapsLock+ | 按键功能增强应用，提高操作效率。](https://topbook.cc/overview/7?selectedArticle=1698)
- 异次元软件：[Capslock+ 键盘党都爱的高效利器 - 让 Windows 快捷键操作更加灵活强大](http://www.iplaysoft.com/capslock-plus.html)
- 少数派：[Capslock+，Windows 上的新一代快捷键神器 by 阡陌-PM | Matrix 精选](http://sspai.com/34479)



------

# 功能说明

以下功能都需要按下`Capslock`，而说明中基本都省略或缩写了`Capslock`，例如`+Q`是`Capslock+Q`

按键对应的功能可以在`Capslock+settings.ini`下的`[Keys]`设置，具体请参考`Capslock+settingsDemo.ini`

*在绝大多数功能的基础上加上`Alt`会是该功能的“增强版”，记住这个规律可以让你需要记忆的热键更少，更容易上手。

## 基础功能

|   Capslock **+**    | 功能                                                         | 说明                                                         |
| :-----------------: | ------------------------------------------------------------ | ------------------------------------------------------------ |
|        短按         | 切换大小写                                                   | 如果需要修改按键动作，可以在 `CapsLock+settings.ini` 下的 `[Keys]` 下添加设置，例如：`press_caps=keyFunc_esc`，按下 Caps Lock 发送 Esc。 |
|        长按         | 不操作                                                       | 视为犹豫操作                                                 |
|       E D S F       | 上 / 下 / 左 / 右                                            |                                                              |
|    LAlt**+** E D    | 上 / 下 3 次                                                 |                                                              |
|    LAlt**+** S F    | 左 / 右 5 次                                                 |                                                              |
|         T B         | 上 / 下 10 次                                                |                                                              |
|    LAlt**+** T B    | 上 / 下 30 次                                                |                                                              |
|         A G         | 向左 / 右按单词移动[1]                                       | [1]: 中文的话不好界定“单词”界限，一般会整句跳过              |
|    LAlt**+** A G    | 向左 / 右移动 3 个单词                                       |                                                              |
|         P ;         | 移动至行首 / 行尾                                            |                                                              |
|    LAlt**+** P ;    | 移动至页首 / 页尾                                            |                                                              |
|       I K J L       | 上 / 下 / 左 / 右选中文字                                    |                                                              |
|    LAlt**+** I K    | 向上 / 下选中 3 次                                           |                                                              |
|    LAlt**+** J L    | 向左 / 右选中 5 次                                           |                                                              |
|         Y N         | 向上 / 下选中 10 次                                          |                                                              |
|    LAlt**+** Y N    | 向上 / 下选中 30 次                                          |                                                              |
|         H .         | 向左 / 右选中单词                                            |                                                              |
|    LAlt**+** H .    | 向左 / 右选中 3 个单词                                       |                                                              |
|          ,          | 选中当前单词                                                 |                                                              |
|     LAlt**+** ,     | 选中当前行                                                   |                                                              |
|         U O         | 选中至行首 / 行尾                                            |                                                              |
|    LAlt**+** U O    | 选中至页首 / 页尾                                            |                                                              |
|         W R         | 向后 / 向前删除                                              |                                                              |
|    LAlt**+** W R    | 向后 / 向前删除单词                                          |                                                              |
|         [ /         | 删除至行首 / 行尾                                            |                                                              |
|    LAlt**+** [ /    | 删除至页首 / 页尾                                            |                                                              |
|      Backspace      | 删除当前行                                                   |                                                              |
| LAlt**+** Backspace | 删除全部内容                                                 |                                                              |
|        Space        | 发送按键：Enter                                              |                                                              |
|        Enter        | 向下插入一行                                                 |                                                              |
|         X C         | 选中(文字、文件、文件夹)时，正常`剪切` / `复制`(文字编辑时)没有选中文字时，`剪切` / `复制`光标所在行的文字 | 不在文字编辑中，又没选中任何内容时，可能会有意外的操作([实现机制](https://capslox.com/capslock-plus/#关于文字操作的机制)问题，会全选文件并复制之类的)，最好别乱按复制粘贴的内容和系统复制粘贴内容独立开，可以分别复制不同内容剪贴板中的内容一直是最后一次使用（包括剪切、复制、粘贴）剪贴板的内容，例如：`Ctrl+C`复制文字`apple`，然后`Capslock+C`复制`banana`，这时`右键`->`粘贴`，结果会是`banana`。然后`Ctrl+V`，结果会是`apple`，再`右键`->`粘贴`，结果会是`apple`原本在 Excel 中，选中一行（列）以上表格，再使用复制相关功能会导致弹出`图片太大，超过部分将被截取。`的问题。这是因为在 Excel 中将剪贴板大量的数据保存起来时，Excel 就会这样提醒，在其他一些剪贴板管理软件上也会有这问题，这应该算 Excel 的问题。对于这个问题目前 Capslock+ 的解决办法是，在保存剪贴板数据时取消对 Excel 窗口的激活，不让 Excel 检测到数据的保存，保存完数据再切回去，这样做的副作用是 Excel 窗口看起来会闪烁一下，暂时没有想到更好的解决办法，如果觉得接受不了的话你可以按下 `Capslock+F12` 来暂时关掉 Capslock+ 的剪贴板功能。 |
|          V          | 粘贴`+X` / `+C`的内容                                        |                                                              |
|   LAlt **+** X C    | `剪切` / `复制`                                              | 同上，另一套独立剪贴板                                       |
|    LAlt **+** V     | 粘贴`+LAlt+X` / `+LAlt+C`的内容                              |                                                              |
|         F1          | 打开本文档页面                                               |                                                              |
|         F2          | 弹出计算板窗口                                               | 所支持的运算请看[关于计算的详细说明](https://capslox.com/capslock-plus/#关于计算的详细说明)在本界面下，按住`Shift`（或切换成大写后）： `u``i``o``p``[` `j``k``l``;``'` `m``,``.` `Space``RAlt` 将输出： `7``8``9``*``/` `4``5``6``+``-` `1``2``3` `0``.``Shift+Enter`会（计算完结果后）将结果输出到下一行的开头`Ctrl+Enter`换行在本界面下，光标左边所有字符都将认定为数学表达式，而不像`+Tab`[1]那样自动匹配表达式在本界面下，`Enter`会计算光标左边的数学表达式并在表达式右边输出`=xxx`，具体规则和`+Tab`[1]的相似，只是所有表达式都会自动补上`=`号，而不是用结果替换掉表达式。[1]: `+Tab`的说明在[下面](https://capslox.com/capslock-plus/#clTabScript)可以看到 |
|         F3          | 翻译选中的或光标所在的单词                                   | 英语单词可以不用选中，只要输入光标靠着单词中文单词不好界定"单词"界限，最好选中后再翻译翻译结果框清空内容后重新输入文本，回车可以再次翻译在复制不了任何文字的窗口会直接弹出空白翻译框获取单词通过发送`Ctrl+C`实现，需确保`+F3`按下时`Ctrl+C`不会有意外操作。详细解释请看[关于文字操作的机制](https://capslox.com/capslock-plus/#关于文字操作的机制)翻译功能通过调用[有道API](http://fanyi.youdao.com/openapi)实现，API接口的请求频率限制为每小时1000次，超过限制会被封禁。也就是说所有使用 Capslock+ 翻译的人一小时内翻译的次数加起来不能超过1000次。需求较高的话可以自己申请一个Key，然后填入 `CapsLock+settings.ini`[1]->`TTranslate`->`apiKey`来独享翻译接口，注意同时要填写`apiType`，因为有道 api 的 key 有两种——免费版和收费版，通过上面那个链接进去申请的就是免费版，那应该填写`apiType=0`，收费版就是`apiType=1`（收费版是要 email 他们来申请的）。以及免费版的 key 会有一个`keyFrom`参数，也需要在`TTranslate`下填写好。具体请查看`CapsLock+settingsDemo.ini`[1]文件中的说明。由于 Capslock+ 是单进程的，网络太差的时候使用翻译的话，进程会因为等待数据传送而造成阻塞，也就是 Capslock+ 会假死。如果出现这种情况，稍等就好。另外，不建议网络情况太差的时候使用翻译功能。[1]: `CapsLock+settings.ini`和`CapsLock+settingsDemo.ini`文件是 Capslock+ 初次运行时自动生成的文件，要快速打开它们请看下面`Qbar`的`cl set`命令说明 |
|         F4          | 短按，将当前窗口变为半透明 / 不透明； 长按，配合`鼠标滚轮上 / 下`以增加 / 减少窗口透明度 | 部分窗口无效，例如 QQ                                        |
|         F5          | 重载程序                                                     |                                                              |
|         F6          | 置顶 / 解除置顶一个窗口                                      |                                                              |
|         F8          | 获取转义后的选中的字符，供调试用                             | 详情看[这里](https://capslox.com/capslock-plus/#tab-js)，不熟悉`JavaScript`的同学可以无视这个功能 |
|         F12         | 关闭 / 打开独立剪贴板功能                                    | 主要给 Excel 里复制时弹窗`图片太大，超过部分将被截取。`用，关闭了就不会弹窗了。 |

## 高级功能

## TabScript

Capslock**+**

Tab

### 功能

1. 光标左边的字符串如果在`Capslock+settings.ini`文件[1]中的`[TabHotString]`，`[QRun]`或`[QWeb]`字段下有相应键名，则将其替换成该键名对应的值
2. 计算光标左边的数学表达式的值（实际上是运行`JavaScript`代码）

### 说明

- 关于热字串功能：

  1. 举个例子，在`Capslock+settings.ini`文件的`[TabHotString]`段下有这么一条设置：`email=123456789@abc.com`，那么在任意能输入文字的地方输入：`asdfghjkl**email**`，按下`Capslock+Tab`，就会变成`asdfghjkl**123456789@abc.com**`
  2. 如果不同字段下有同名的键名，三个标签的优先级是：
     `[TabHotString]` > `[QRun]` > `[QWeb]`
     例如：
     `[TabHotString]`段下有设置：`a=apple`
     `[QRun]`段下有设置：`a=e:\banana`
     那么输入`a`后，`Capslock+Tab`将得到`apple`（而不是`e:\banana`）
     （虽然理论上不同段名下的键名可以同名，但`[QRun]`和`[QWeb]`下的键名不应重名，否则在使用`+Q`功能时会有问题）

- 关于计算功能：

  1. 支持较复杂的数学表达式：多种进制的数值，任意数量嵌套的括号，三元运算，关系运算，逻辑运算，位运算，算术运算，各种函数等。
     详细看下面的[关于计算的详细说明](https://capslox.com/capslock-plus/#关于计算的详细说明)

  2. 当数学表达式最后不带`=`号时，计算结果会替换掉表达式。例如：`1+2+3`->`Capslock+Tab`->`6`

  3. 当数学表达式最后带有`=`号时，计算结果输出到等号右边。例如：`1+2+3=`->`Capslock+Tab`->`1+2+3=6`

  4. 当计算不出结果，会输出一个`?`号。例如：`1+2+=`->`Capslock+Tab`->`1+2+=?`

  5. 从光标向左，直到遇到第一个空格符或行首，之间的字符串将认定为是表达式，如果需要计算的表达式带有空格，请选中该表达式，或在表达式开头加上

     ```
     `
     ```

     （反引号），例如：

     ```
     `1 + 1 = 
     ```

     ，

     选中的或反引号右边的所有字符都将被判定为表达式

     。

     超过一行的表达式只能先选中它们，例如：

     

     ```
     a=1;
     b=2;
     c=3;
     a+b+c=
     ```

     

  \* Capslock+ 不保证计算结果绝对正确。对于要求比较严格的计算中（例如金钱的计算），请谨慎使用计算功能！

  1. 对于熟悉`JavaScript`的同学：

  2. 其实所谓的计算数学表达式，只是在运行 JavaScript 代码。例如你可以这样：
     输入``var i=0,j=101; while(j--)i+=j;`，然后`Capslock+Tab`来求1~100的和。

  3. Capslock+ 还允许这样来调用函数：

     

     ```
     any text any text
     any text any text
     .functionX()
     ```

     

     这样调用函数，其实就是把除了写在最后一行的函数以外的所有其他字符处理成单行字符串后，再调用后面的方法。而处理过程实际上是：在

     ```
     '
     ```

     ```
     "
     ```

     ```
     &
     ```

     ```
     \
     ```

     ```
     \n
     ```

     ```
     \r
     ```

     ```
     \t
     ```

     ```
     \b
     ```

     ```
     \f
     ```

     这些符号前添加转义符

     ```
     \
     ```

     ，然后再将每个换行符都替换成

     ```
     \n
     ```

     。

     所以选中以上3行后`Capslock+Tab`，相当于执行：

     

     ```
     'any text any text\nany text any text'.functionX()
     ```

     

     例如，对于以下一段：

     

     ```
     apple banana apple cat
     apple dog apple banana
     apple cat apple dog
     .replace(/apple/g, 'egg') //将所有'apple'换成'egg'
     ```

     

     选中以上4行，

     ```
     Capslock+Tab
     ```

     后，内容将变为：

     

     ```
     egg banana egg cat
     egg dog egg banana
     egg cat egg dog
     ```

     

  4. 可以在 Capslock+ 目录下的`loadScript`文件夹添加`js`文件，并在`CapsLock+settings.ini`的`Global`字段下的`loadScript`键设置需要需要自动加载的`js`文件的文件名（以`,`隔开）。Capslock+ 会在启动时按设置的顺序加载文件，从而扩展`Capslock+Tab`功能。自己的函数不要直接写在`scriptDemo.js`里，版本更新的话会被覆盖的。

  5. 因为上面那种调用函数的方法，实际上会把除了最后一行函数以外的其他字符经过转义，变成单行字符串（看上面第 2 条），那么你如果想自己编写函数来处理字符的话，你的函数必须是针对这样的格式的字符串进行操作的。在自动生成的`loadScript`文件夹下的`scriptDemo.js`里面有函数例子，你可以用来参考。另外你可以选中一段文字，再按下`Capslock+F8`来获取调试用的字符串，它会给你一行由那一段字符转义得到的字符串。你可以把你的`js`文件引入到一个`html`文件，然后用浏览器打开那个`html`文件，然后就可以在控制台用刚才拿到的字符串调试你的函数了。

  6. 调用 js 的功能是调用了 IE 引擎来实现的，所以你的代码需要根据你系统上的 IE 引擎版本来躲坑。可以用`navigator.userAgent`->`Capslock+Tab`来看具体版本。

- 综上，`+Tab`对各种形式的字符生效的优先级从高到低排列如下：

  1. 选中字符的情况下：
     1. 多行，并且最后一行格式为`.xxx()`的字符 --`JavaScript`
     2. 其他情况 --`JavaScript`
  2. 未选中字符情况下：
     1. 光标左边有匹配`[TabHotString]`，`[QRun]`或`[QWeb]`的字符 --`HotString`
     2. 从行首开始第一个```符号至光标之间的字符 --`JavaScript`
     3. 从光标向左直到遇到第一个空格或行首，之间的字符 --`JavaScript`

[1]: `CapsLock+settings.ini`文件是 Capslock+ 初次运行时自动生成的文件，要快速打开它请看下面`Qbar`的`cl set`命令说明

## WinBind

Capslock**+**

Win

**+** 

### 功能

1. 绑定窗口到相应按键：
   - 模式1： 单击，绑定当前激活的窗口到相应按键
   - 模式2： 双击，追加绑定当前激活的窗口到相应按键
   - 模式3： 三击，绑定当前激活的窗口所属程序所拥有的所有窗口到相应按键

Capslock**+**

0~9

### 功能

1. `激活`/`最小化`绑定在该按键的窗口

### 说明

- 关于绑定：
  1. 模式1和模式3会覆盖当前按键上已有的绑定窗口
  2. 模式2绑定在按键现有模式是模式1或模式2时会追加窗口，是模式3时不追加，而会覆盖原绑定设置，绑定当前激活窗口（与模式1效果一样）
  3. 模式2操作示例：
     1. 激活窗口A（鼠标点击一下是方法之一），依次按下`Capslock``Alt`不放，再按两次`1`；
     2. 激活窗口B，同样操作；
     3. 激活窗口C，同样操作；
     4. 按下`Capslock`不放，（多次）按下`1`来在A,B,C三个窗口之间实现类似`Alt+Tab`的窗口切换。
  4. 模式2绑定的窗口被关闭至只剩下1个时，将自动转换成模式1绑定（可以激活 / 最小化窗口）
- 关于窗口激活 / 最小化：
  1. 模式1下，在原窗口不存在时，激活动作会自动绑定窗口所属程序的另一个窗口
  2. 模式1和模式3下，在原绑定窗口所属程序未启动时，激活动作将启动该程序
  3. 绑定的窗口只有一个时，所有模式都将激活 / 最小化该窗口

## Qbar

Capslock**+**

Q

### 功能

1. 弹出输入框，输入不同命令执行不同操作（见下面的`cl` `set`等）

### 说明

1. 按下`ESC`键或失去焦点后将关闭界面
2. 选中字符再按下`+Q`可以将其填入输入框
3. 选中文件再按下`+Q`，它的路径会填入输入框

### 命令

| 命令                                                         | 功能                                                         | 说明                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| `cl about`                                                   | 查看版本信息                                                 |                                                              |
| `cl set`                                                     | 打开`Capslock+settings.ini`文件和`Capslock+settingsDemo.ini`文件 | `Capslock+settings.ini`各字段作用：`Global`：全局设置`QSearch`：设置搜索命令`QWeb`：设置打开网页`QRun`：设置启动程序`QStyle`：设置`+Q`输入框的样式`TabHotString`：设置`+Tab`热字串*更具体的说明请查看`CapsLock+settingsDemo.ini`文件 |
| `ooo -> xxx`                                                 | 在`Capslock+settings.ini`以下的某字段添加一行： `ooo=xxx`如果是搜索网址： `[QSearch]`如果是文件路径： `[QRun]`如果是网址[1]： `[QWeb]`都不是： `[TabHotString]` | 例如输入`mdn -> developer.mozilla.org`，记录完成后就可以在`+Q`输入`mdn`来打开`developer.mozilla.org`如果文件是快捷方式，会自动找到快捷方式所指向的文件的路径来记录如果所记录的字符串格式类似文件路径或者网址[1]，例如`com.com.com`，就会被记录到`QWeb`，要将这类字符串记录到`[TabHotString]`，可以用`->string`命令，它会把字符串记录到`TabHotString`； 同样，`->search`会记录到`QSearch`；`->run`会记录到`QRun`；`->web`会记录到`QWeb`。*更具体的说明请查看`CapsLock+settingsDemo.ini`文件[1]: 只有以`http://`或`https://`或`www.`开头，或者包含`.com`或`.net`或`.org`的字符串才会被认为是网址 |
| `ooo ->search xxx``ooo ->run xxx``ooo ->web xxx``ooo ->str xxx` | 在Capslock+settings.ini下的`[QSearch]` / `[QRun]` / `[QWeb]` / `[TabHotString]`字段添加一行： `ooo=xxx` | 记录完成后可以在`+Q`输入`ooo`来搜索 / 打开路径为`xxx`的文件（夹） / 网址 / 使用`+Tab`的热字串功能*更具体的说明请查看`CapsLock+settingsDemo.ini`文件 |
| `web xxx`                                                    | 打开xxx网址                                                  | 如果`xxx`以`http://`或`https://`或`www.`开头，或者包含`.com`或`.net`或`.org`，`web`命令可以省略。例如：`google.com` |
| `s xxx``bd xxx`                                              | 百度搜索`xxx`                                                | 百度是默认搜索引擎，即可以省略命令直接输入关键词进行搜索，除非关键词中包含其他的命令关键词可以在`Capslock+settings.ini`文件中修改默认搜索引擎，以及修改或添加搜索命令以支持其他搜索引擎。* 更具体的说明请查看`CapsLock+settingsDemo.ini`文件 |
| `g xxx``gg xxx`                                              | 谷歌搜索`xxx`                                                |                                                              |
| `m xxx`                                                      | MDN搜索`xxx`                                                 |                                                              |
| `wk xxx`                                                     | 维基搜索`xxx`                                                |                                                              |
| `tb xxx`                                                     | 淘宝搜索`xxx`                                                |                                                              |
| `aa bb`                                                      | 用`aa`打开`bb`                                               | `aa`：`[QRun]`上有记录的一个程序`bb`：`[QRun] / [QWeb]`上有记录的一个文件（夹） / 网址简写，或具体的文件（夹）路径 / 网址例如： `[Qrun]`下记录了`ie=C:\Program Files\Internet Explorer\iexplore.exe` `[QWeb]`记录了`clp=http://cjkis.me/capslock+/` 那`ie clp`就可以用`ie`来打开`http://cjkis.me/capslock+/` 也可以直接`ie cjkis.me/capslock+` |
| `xxx`                                                        | 如果`[QRun]`或`[QWeb]`内有记录则运行对应文件或打开对应网址如果是文件（夹）路径，打开该文件（夹）如果是网址[1]，打开该网址不是以上情况的话，百度[2] |                                                              |
| 能根据输入，展示`[QRun]`和`[QWeb]`的记录，或输入的路径下的文件（夹）[3]可以使用通配符`?`和`*`来匹配任意一个 / 多个字符，例如： `?at`可以匹配 `bat`, `cat`, `fat`... `g*d`可以匹配 `god`, `good`, `gold`...无提示列表的情况下`Tab`展开提示列表（如果`QRun`或`QWeb`有记录的话）有提示列表的情况下，如果有选中某文件名，`Tab`可以将选中的文件名放到输入框，否则，会将第一个文件名放到输入框在展示路径下的文件时，`\`键（或`/`[4]）可以将文件（夹）名填入输入框，`Capslock+-`可以回到上级目录，`Capslock+=`可以前进到下一层目录如果要搜索类似网址的关键字，请带上搜索命令，如`s com.com`，否则将被当成网址打开`Capslock+settings.ini`中，提供给`Qbar`使用的段名`[QSearch],[QRun],[QWeb]`，支持在键名后加上`<xxx>`来作为提示，它们不会影响命令的使用。例如： `[QWeb]`下有`cx <capslox>=capslox.com`，那么`QBar`下输入`cx`打开`capslox.com``[QRun]`下需要为程序添加启动参数或以管理员权限打开的话，程序路径要用引号引起来，然后在这部分的左边加上`*RunAs`以管理员权限打开，在这部分的右边加上启动参数。例如： `ie=*RunAs "C:\Program Files\Internet Explorer\iexplore.exe" -k` *具体参照`Capslock+SettingsDemo.ini``Ctrl+Enter`会在输入的字符串前后加上`www.``.com`，并当成网址打开。例如： 输入`capslox`->`Ctrl+Enter`->打开`www.capslox.com`Qbar 支持搜索全部已安装程序，如果在启动 Capslock+ 后有安装 / 卸载程序，需要重载 Capslock+ 。[1]: 只有以`http://`或`https://`或`www.`开头，或者包含`.com`或`.net`或`.org`的字符串才会被认为是网址。否则，请在网址前面加上命令`web`。[2]: 通过修改`Capslock+settings.ini`文件下，`[QSearch]`段的`default`可以设置默认搜索[3]: 在展示输入的路径下的文件时，为了保证加载速度，在文件过多的时候，会放弃加载部分文件的图标，直接使用一个`空白文件`样式的图标[4]: `\`键在文件路径输入时会频繁使用，而`\`键实在太远了，所以特地让`/`键也实现和`\`键一样的功能，如果需要输出`/`符号可以用`Capslock+/` |                                                              |                                                              |

------

# 补充说明

## 关于文字操作的机制

Capslock+ 不少功能是根据不同文字内容做不同操作的，例如选中文字自动填入 Qbar、翻译、TabScript 的字符替换、数学表达式计算等。这些功能都是通过发送一个`Ctrl+C`来获取文字，再对文字进行操作的。 因为这个原因，**在使用这些功能时需要注意Ctrl+C会不会引起意外的操作，例如在命令行下这个组合键通常是退出操作。**

在很多编程工具下，`Ctrl+C`会在未选中任何文本时复制光标所在行整行文本，这样就会造成在这些界面下无法准确判断用户到底有没选中文本。 现在对于这个问题的解决办法是通过判定复制到的文本最后是不是换行符来判断获取到的文本是不是这些软件自带的复制功能复制到的。 这个方法暂时只发现在某些带有这个功能的界面的最后一行下会有问题，因为是最后一行，所以文本最后可能不带换行符，这时如果未选中文字使用了相关功能，就会被判定为选中了整行文字，而按选中文字的情况作出相应的操作。 对于这种情况，只要不在最后一行编辑——回车一下，再回到上面编辑文本即可。

## 关于计算的详细说明

- Capslock+F2 和 Capslock+Tab 的计算功能支持使用函数（也叫方法）帮助计算。函数就是类似`functionxxx()`这样格式的东西，使用函数只要把需要计算的数值写在括号里，多个数值之间用逗号隔开。例如，使用average()函数来求平均值：`average(1,3,5,7,12,32)`

- 支持的常量和函数：[JavaScript Math 对象](http://www.w3school.com.cn/jsref/jsref_obj_math.asp)

- 除了上面页面中列出的函数外，还支持以下函数：

  | 函数                 | 描述                     |
  | -------------------- | ------------------------ |
  | average(a,b,c...)    | 计算 a,b,c... 的平均值   |
  | variance(a,b,c...)   | 计算 a,b,c... 的方差     |
  | spVariance(a,b,c...) | 计算 a,b,c... 的样本方差 |

  *如果你有需要用到的公式想添加到 Capslock+，可以用 JavaScript 写好，放到

  ```
  loadScript
  ```

  文件夹中，并在

  ```
  CapsLock+settings.ini
  ```

  ->

  ```
  Global
  ```

  ->

  ```
  loadScript
  ```

  中设置，这样 Capslock+ 在启动时就会加载该 js 文件，来添加你编写的函数。也可以

  联系我

  ，可行的话我会添加到 Capslock+。

- 支持的数值：[JavaScript Number 对象](http://www.w3school.com.cn/js/js_obj_number.asp)

- 支持的运算符：[JavaScript 运算符](http://www.w3school.com.cn/js/js_operators.asp)

- 支持的比较和逻辑运算符：[JavaScript 比较和逻辑运算符](http://www.w3school.com.cn/js/js_comparisons.asp)

- 想了解更多你需要学习 JavaScript：[JavaScript 教程](http://www.w3school.com.cn/js/index.asp)

- 例子：（在这里试试`Capslock+Tab`？）

- 因为计算的功能实际上是用了 JavaScript 引擎来运算，而在 JavaScript 里，小数的运算可能会有一些偏差，例如：`0.1+0.2=0.30000000000000004`。 对于这个问题，Capslock+ 在 Capslock+F2 的计算板和 Capslock+Tab 功能中，虽然用了一些方法去解决了这个问题。 **但是 Capslock+ 仍然不保证计算功能可以能得到一个绝对正确的结果，在使用计算功能的时候需要慎重，并自行承担后果。** 对于这个问题，更详细的说明请看[这里](http://cjkis.me/2016/floating-point-calculation-in-javascript/)。

