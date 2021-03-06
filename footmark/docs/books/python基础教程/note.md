# Python基础教程阅读笔记

Python是一种相当高级的语言。代码少的代价是运行速度慢，C程序运行1秒钟，Java程序可能需要2秒，而Python程序可能就需要10秒。对于初学者和完成普通任务，Python语言是非常简单易用的。Python可以做日常任务，比如自动备份你的MP3；可以做网站，很多著名的网站包括YouTube就是Python写的；可以做网络游戏的后台，很多在线游戏的后台都是Python开发的。总之就是能干很多很多事啦。Python不能写操作系统，写手机应用，只能用Objective-C（针对iPhone）和Java（针对Android）；写3D游戏，最好用C或C++。

Python是著名的“龟叔”Guido van Rossum在1989年圣诞节期间无聊编写的一个编程语言。C语言适合开发那些追求运行速度、充分发挥硬件性能的程序。而Python是用来编写应用程序的高级编程语言。

Python就为我们提供了非常完善的基础代码库，覆盖了网络、文件、GUI、数据库、文本等大量内容，被形象地称作“内置电池（batteries included）”。
除了内置的库外，Python还有大量的第三方库直接使用。

Python的哲学就是简单优雅，尽量写容易看明白的代码，尽量写少的代码。

Python适合开发哪些类型的应用呢？

首选是网络应用，包括网站、后台服务等等；

其次是许多日常需要的小工具，包括系统管理员需要的脚本任务等等；

另外就是把其他语言开发的程序再包装起来，方便使用。

Python的缺点。

第一个缺点就是运行速度慢，Python是解释型语言，翻译成机器码非常耗时。大量的应用程序不需要这么快的运行速度，因为用户根本感觉不出来。

第二个缺点就是代码不能加密。发布你的Python程序就是发布源代码，解释型的语言，则必须把源码发布出去。卖软件变为靠网站和移动应用卖服务的模式。

因为Python是跨平台的，它可以运行在Windows、Mac和各种Linux/Unix系统上。安装后，你会得到Python解释器（就是负责运行Python程序的），一个命令行交互环境，还有一个简单的集成开发环境。Python有两个版本，一个是2.x版，一个是3.x版，这两个版本是不兼容的，许多第三方库还暂时无法在3.x上使用。OS X 10.8或.9自带了Python 2.7。

编写Python代码得到的是一个包含Python代码的以.py为扩展名的文本文件。要运行代码，就需要Python解释器去执行.py文件。

Python官方网站下载的Python 2.7包含官方版本的解释器：CPython。用C语言开发的，命令行下运行python就是启动CPython解释器。是使用最广的Python解释器。IPython在交互方式上有所增强,CPython用>>>作为提示符，IPython用In [序号]:作为提示符。

PyPy采用JIT技术对Python代码进行动态编译显著提高Python代码的执行速度。绝大部分Python代码都可以在PyPy下运行,需要了了解其差异.

Jython是运行在Java平台上的Python解释器，可以直接把Python代码编译成Java字节码执行。IronPython是运行在微软.Net平台上的Python解释器，可以直接把Python代码编译成.Net的字节码。如果要和Java或.Net平台交互，最好的办法是通过网络调用来交互，确保各程序之间的独立性。

命令行中输入python启动交互式环境, 在提示符>>>下，直接输入代码，按回车，就可以立刻得到代码执行结果。用exit()退出Python。

输入和输出

print加上字符串，就可以向屏幕上输出指定的文字。跟上多个字符串，用逗号“,”隔开，会依次打印每个字符串，遇到逗号“,”会输出一个空格.

Python提供了一个raw_input，可以让用户输入字符串，并存放到一个变量里。raw_input可以让你显示一个字符串来提示用户.

raw_input和print是在命令行下面最基本的输入和输出，用户也可以通过其他更高级的图形界面完成输入和输出。

变量

在计算机程序中变量不仅可以为整数或浮点数，还可以是字符串。要打印变量的内容，除了直接写name然后按回车外，还可以用print语句.

基础篇
Python是一种计算机编程语言。自然语言在不同的语境下有不同的理解，而计算机要根据编程语言执行任务，就必须保证编程语言写出的程序决不能有歧义，所以，任何一种编程语言都有自己的一套语法，编译器或者解释器就是负责把符合语法的程序代码转换成CPU能够执行的机器码，然后执行。Python的语法比较简单，采用缩进方式

'#'开头的语句是注释，注释是给人看的，解释器会忽略掉注释。其他每一行都是一个语句，当语句以冒号“:”结尾时，缩进的语句视为代码块。

缩进没有规定缩进是几个空格还是Tab。但最好始终坚持使用4个空格的缩进。另一个好处是强迫你写出缩进较少的代码，你会倾向于把一段很长的代码拆分成若干函数，从而得到缩进较少的代码。缩进的坏处就是“复制－粘贴”功能失效了。Python程序是大小写敏感。

Python能够直接处理的数据类型

整数

Python可以处理任意大小的整数，当然包括负整数，程序中的表示方法和数学上的写法一模一样，如：1，100，-8080，0等,十六进制用0x前缀和0-9，a-f表示，如：0xff00。


浮点数

浮点数即小数，因为按照科学记数法表示时，一个浮点数的小数点位置是可变的，比如，1.23x109和12.3x108是相等的。浮点数可以用数学写法，如1.23，3.14，-9.01，很大或很小的浮点数必须用科学计数法表示，1.23x109就是1.23e9，或者12.3e8，0.000012可以写成1.2e-5，等等。

整数和浮点数在计算机内部存储的方式是不同的，整数运算永远是精确的（除法难道也是精确的？是的！），而浮点数运算则可能会有四舍五入的误差。

字符串

字符串是以''或""括起来的任意文本，比如'abc'，"xyz"等。''或""本身不是属于字符串。字符串内部既包含'又包含"用转义字符\来标识.\n表示换行，\t表示制表符，\\表示字符\
```
'I\'m \"OK\"!'表示I'm "OK"!
```

字符串需转义的字符太多,需要加很多\，简单办法是用r''表示''内部的字符串默认不转义.
```
print '\\\t\\'  表示\       \
print r'\\\t\\' 表示\\\t\\
```
字符串内多换行，用\n写在一行里不好阅读，Python允许用'''...'''表示多行内容, 多行字符串'''...'''还可以在前面加上r使用.

布尔值

布尔值只有True、False两种值，Python中可以直接用True、False表示布尔值，也可以通过布尔运算计算,布尔值可以用and、or和not运算。and运算是与运算，只有所有都为True，and运算结果才是True,or运算是或运算，只要其中有一个为True，or运算结果就是True, not运算是单目运算符，把True变成False，False变成True.布尔值经常用在条件判断中.

空值

空值是Python里一个特殊的值，用None表示。


变量

变量可以是任意数据类型。用一个变量名表示, 必须是大小写英文、数字和_的组合，且不能用数字开头，Python中等号=是赋值语句，可以把任意数据类型赋值给变量，同一个变量可以反复赋值，而且可以是不同类型的变量.
这种变量本身类型不固定的语言称之为动态语言，静态语言在定义变量时必须指定变量类型，如果赋值的时候类型不匹配，就会报错。和静态语言相比，动态语言更灵活。

请不要把赋值语句的等号等同于数学的等号。理解变量在计算机内存中的表示也非常重要。

a = 'ABC'解释时,Python1)在内存中创建了一个'ABC'的字符串；2)在内存中创建了一个名为a的变量，并把它指向'ABC'。b =a 时创建变量b,让它指向变量a所指向的数据.

Python支持多种数据类型，任何数据都看成一个“对象”，变量用来指向这些数据对象的，对变量赋值就是把数据和变量给关联起来。

常量

是不能变的变量，在Python中，通常用全部大写的变量名表示常量, 如PI = 3.14159265359,但Python没有任何机制保证PI不会被改变。

无论整数做除法还是取余数，结果永远是整数，整数运算结果永远是精确的, 要做精确的除法，只需把其中一个整数换成浮点数做除法。

字符串比较特殊的是还有一个编码问题。

计算机只能处理数字，文本转换为数字才能处理。最早的计算机采用8个比特（bit）作为一个字节（byte），最大的整数就是255（二进制11111111=十进制255），两个字节可以表示的最大整数是65535，4个字节可以表示的最大整数是4294967295。

计算机是美国人发明，最早只有大小写英文字母、数字和一些符号组成127个字母ASCII编码被编码到计算机里，如大写字母A的编码是65，小写字母z的编码是122。

中文至少需要两个字节，还不能和ASCII编码冲突，中国制定了GB2312编码把中文编进去,日本把日文编到Shift_JIS里，韩国把韩文编到Euc-kr里。各国的标准不可避免地出现冲突，多语言混合的文本显示出来会有乱码。

Unicode把所有语言都统一到一套编码里解决乱码问题。ASCII编码和Unicode编码的区别：ASCII编码是1个字节，而Unicode编码通常是2个字节。全英文文件用Unicode编码比ASCII编码需要多一倍的存储空间，在存储和传输上就十分不划算。Unicode编码转化为“可变长编码”的UTF-8编码。UTF-8编码把一个Unicode字符根据不同的数字大小编码成1-6个字节，常用的英文字母被编码成1个字节，汉字通常是3个字节，只有很生僻的字符才会被编码成4-6个字节。ASCII编码实际上可以被看成是UTF-8编码的一部分，大量只支持ASCII编码的历史遗留软件可以在UTF-8编码下继续工作。

计算机系统通用的字符编码工作方式：内存中统一使用Unicode编码，保存到硬盘或者需要传输的时候转换为UTF-8编码。

Python对Unicode的支持

因为Python的诞生比Unicode标准发布的时间还要早，最早的Python只支持ASCII编码，普通的字符串'ABC'在Python内部都是ASCII编码的。Python提供了ord()和chr()函数用于字母和数字相互转换.Python在后来添加了对Unicode的支持，以Unicode表示的字符串用u'...'表示,\u十六进制的Unicode码表示一个Unicode字符。

两种字符串如何相互转换。把u'xxx'转换为UTF-8编码的'xxx'用encode('utf-8')方法,如u'中文'.encode('utf-8')输出'\xe4\xb8\xad\xe6\x96\x87'

英文字符转换后表示的UTF-8的值和Unicode值相等（但占用的存储空间不同），而中文字符转换后1个Unicode字符将变为3个UTF-8字符。len()函数可以返回字符串的长度.
字符串'xxx'转换为Unicode字符串u'xxx'用decode('utf-8')方法,如'\xe4\xb8\xad\xe6\x96\x87'.decode('utf-8')返回u'\u4e2d\u6587'

Python源代码中包含中文的时候，保存时需要指定保存为UTF-8编码,各文本软件有不同的方法。通常在文件开头写上这两行：
```
#!/usr/bin/env python    //通知nix系统是一个Python可执行程序，Win会忽略这个注释；
# -*- coding: utf-8 -*- //告诉Python解释器，按照UTF-8编码读取源代码
```
格式化

如何输出格式化的字符串。Python的格式化方式和C语言一致，用%实现,%运算符就是用来格式化字符串的。在字符串内部，%s表示用字符串替换，%d表示用整数替换，有几个%?占位符，后面就跟几个变量或者值，顺序要对应好。如果只有一个%?，括号可以省略。
```
>>> 'Hello, %s' % 'world'
'Hello, world'
```
常见的占位符有：%d  整数,%f 浮点数,%s   字符串, %x  十六进制整数, %%来表示一个%, %s永远起作用，它会把任何数据类型转换为字符串, Unicode字符串也可选输出,但确保替换的字符串也是Unicode字符串. 格式化整数和浮点数还可以指定是否补0和整数与小数的位数
```
>>> '%2d-%02d' % (3, 1)
' 3-01'
>>> '%.2f' % 3.1415926
'3.14'
```

由于历史遗留问题，Python 2.x版本虽然支持Unicode，但在语法上需要'xxx'和u'xxx'两种字符串表示方式。Python 3.x把'xxx'和u'xxx'统一成Unicode编码，而以字节形式表示的字符串则必须加上b前缀：b'xxx'。

list

Python内置数据类型,一种有序的集合，可以随时添加和删除其中的元素, len()函数可以获得list元素的个数, 用索引来访问list中每一个位置的元素,索引超出了范围时，Python会报一个IndexError错误。取最后一个元素，除了计算索引位置外，还可以用-1做索引.

list是一个可变的有序表，可以使用append()往list中追加元素到末尾,也可以使用insert(1, 'Jack')把元素插入到指定的位置，用pop()方法删除list末尾的元素,删除指定位置的元素，用pop(i)方法, 替换某个元素可以直接赋值给对应的索引位置,list里面的元素的数据类型也可以不同，元素也可以是另一个list。

如果一个list中一个元素也没有，就是一个空的list，它的长度为0.

tuple

tuple和list非常类似，但是tuple一旦初始化就不能修改，没有append()，insert()这样的方法。获取元素的方法和list是一样的，你可以正常地使用classmates[0]，classmates[-1]，但不能赋值成另外的元素。因为tuple不可变，所以代码更安全。如果可能，能用tuple代替list就尽量用tuple。

tuple在定义时tuple的元素就必须被确定下来t = (1, 2)表示两个元素,t = ()表示空tuple,格外注意t = (1,)表示1个元素,也只能用这种方式表示.

tuple所谓的“不变”是说，tuple的每个元素，指向永远不变, 但指向的对象本身内容是可变的！

## 函数部分

有规律的重复组织成带有意义的名称的函数实现编写一次，多次调用。内置函数可以直接调用

抽象是数学中非常常见的概念。借助抽象，我们才能不关心底层的具体计算过程，而直接在更高的层次上思考问题。函数就是最基本的一种代码抽象的方式

调用一个函数，需要知道其名称和参数。内置函数直接从Python的官方网站[查看文档](http://docs.python.org/2/library/functions.html)

也可以在交互式命令行通过help()查看,函数入参数数量或参数类型不对，会报TypeError的错误，并指出错误原因, 如
TypeError: abs() takes exactly one argument (2 given)仅有1个参数，但给出了两个
TypeError: bad operand type for abs(): 'str'  str是错误的参数类型

Python内置的常用函数还包括数据类型转换函数，函数名其实就是指向一个函数对象的引用，把函数名赋给一个变量，相当于给这个函数起了一个“别名”.


Python定义一个函数要使用def语句，依次写出函数名、括号、括号中的参数和冒号':', 在缩进块中编写函数体，返回值用return语句返回。函数执行中遇到return时就执行完毕将结果返回。没有return语句结尾会返回None。return None可以简写为return。

空函数: 一个只包含用pass语句作为占位符的函数。pass也可以用在C语言中直接使用';'的地方.

对于自定义函数,参数个数不对会自动检查出来，并抛出TypeError,参数类型不对无法帮我们检查。自己对参数类型做检查，可以用内置函数isinstance实现.

python语法上返回一个tuple可以省略括号，而多个变量可以同时接收一个tuple，按位置赋给对应的值，所以Python的函数返回多值其实就是返回一个tuple.


定义函数的时候，我们把参数的名字和位置确定下来，函数的接口定义就完成了。对于函数的调用者来说，只需要知道如何传递正确的参数，以及函数将返回什么样的值就够了，函数内部的复杂逻辑被封装起来，调用者无需了解。

Python的函数参数分为必选参数、默认参数、可变参数和关键字参数，使得函数定义出来的接口，不但能处理复杂的参数，还可以简化调用者的代码。

默认参数注意：

1. 必选参数在前，默认参数在后，否则Python的解释器会报错

2. 变化大的参数放前面，变化小的参数放后面。变化小的参数就可以作为默认参数。

默认参数降低了函数调用的难度，而一旦需要更复杂的调用时，又可以传递更多的参数来实现。无论是简单调用还是复杂调用，函数只需要定义一个。

有多个默认参数时，调用的时候，既可以按顺序提供默认参数，也可以不按顺序提供部分默认参数。当不按顺序提供部分默认参数时，需要把参数名写上。

Python函数在定义的时候，默认参数如果指向[]，调用时只改变其中的内容,下次调用会看到上次调用的结果。所以，定义默认参数要牢记一点：默认参数必须指向不变对象！不变对象一旦创建，对象内部的数据就不能修改，这样就减少了由于修改数据导致的错误。此外，由于对象不变，多任务环境下同时读取对象不需要加锁，同时读一点问题都没有。

可变参数

可变参数就是传入的参数个数是可变的，实现可变参数可以使用list, tuple将参数包装起来一次性传入.

定义可变参数和定义list或tuple参数相比，仅仅在参数前面加了一个*号。函数代码完全不变。调用该函数时，可以传入任意个参数，包括0个参数

用list或者tuple调用可变参数时，在list或tuple前面加一个*号，把list或tuple的元素变成可变参数传进去：

关键字参数

关键字参数允许你传入0个或任意个含参数名的参数，这些关键字参数在函数内部自动组装为一个dict。关键字参数可以扩展函数的功能。和可变参数类似，也可以先组装出一个dict，把该dict转换为关键字参数传进去,只是要加两个'*'

在Python中定义函数，可以用必选参数、默认参数、可变参数和关键字参数，这4种参数都可以一起使用，或者只用其中某些，但是请注意，参数定义的顺序必须是：必选参数、默认参数、可变参数和关键字参数。

对于任意函数，都可以通过类似```func(*args, **kw)```的形式调用它，无论它的参数是如何定义的。使用*args和**kw是Python的习惯写法.

在函数内部，可以调用其他函数。如果一个函数在内部调用自身本身，这个函数就是递归函数。递归函数的优点是定义简单，逻辑清晰。理论上，所有的递归函数都可以写成循环的方式。

使用递归函数需要注意防止栈溢出。解决递归调用栈溢出的方法是通过尾递归优化，事实上尾递归和循环的效果是一样的，所以，把循环看成是一种特殊的尾递归函数也是可以的。

尾递归是指，在函数返回的时候，调用自身本身，并且，return语句不能包含表达式。这样，编译器或者解释器就可以把尾递归做优化，使递归本身无论调用多少次，都只占用一个栈帧，不会出现栈溢出的情况。Python解释器没有针对尾递归做优化，尾递归方式也会导致栈溢出。

python默认迭代次数不能超过998次，超过会报错RuntimeError: maximum recursion depth exceeded，调用sys.setrecursionlimit(1200)来增加数量.


但是在Python中，代码不是越多越好，而是越少越好。代码不是越复杂越好，而是越简单越好。

切片 取一个list或tuple的部分元素是非常常见的操作。Python提供了切片（Slice）操作符简化这种操作。L[0:3]表示，从索引0开始取，直到索引3为止，但不包括索引3。L[-2:],表示取最后两个元素, L[-2:-1]表示取倒数第二个元素. 切片可以用于list, tuple, 字符串,包括unicode.


通过for循环来遍历list或tuple称为迭代（Iteration）。在Python中，迭代是通过for ... in来完成的, 它可以用在list或tuple及其他可迭代对象上。可迭代对象，无论有无下标，都可以迭代,如默认情况下，dict迭代的是key。如果要迭代value，可以用for value in d.itervalues()，如果要同时迭代key和value，可以用for k, v in d.iteritems()。字符串也是可迭代对象

通过collections模块的Iterable类型判断判断一个对象是可迭代对象.

对list实现下标循环要使用Python内置的enumerate函数, 它可以把一个list变成索引-元素对来同时迭代索引和元素本身：

```
>>> for i, value in enumerate(['A', 'B', 'C']):
...     print i, value
...
0 A
1 B
2 C
```

列表生成式即List Comprehensions，是Python内置的非常简单却强大的可以用来创建list的生成式。
```
生成list [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]可以用range(1, 11)：

>>> [x * x for x in range(1, 11)] // 把要生成的元素x * x放到前面，后面跟for循环，就可以把list创建出来
[1, 4, 9, 16, 25, 36, 49, 64, 81, 100]

>>> [x * x for x in range(1, 11) if x % 2 == 0] // 加for
[4, 16, 36, 64, 100]

>>> [m + n for m in 'ABC' for n in 'XYZ'] // 多重循环
['AX', 'AY', 'AZ', 'BX', 'BY', 'BZ', 'CX', 'CY', 'CZ']
```


Python中，这种一边循环一边计算的机制，称为生成器（Generator）。创建一个generator，第一种方法是将一个列表生成式的[]改成()，就创建了一个generator：
```
>>> g = (x * x for x in range(10))
>>> g
<generator object <genexpr> at 0x104feab40>
```
通过generator的next()方法打印出generator的每一个元素呢,计算到最后一个元素时，抛出StopIteration的错误。正确的方法是使用for循环，因为generator也是可迭代对象：

>>> g = (x * x for x in range(10))
>>> for n in g:
...     print n

generator还可以用函数来实现, 一个函数定义中包含yield关键字，那么这个函数就不再是一个普通函数，而是一个generator。遇到return语句或者执行到函数体最后一行语句，就是结束generator的指令，for循环随之结束.变成generator的函数，在每次调用next()的时候执行，遇到yield语句返回，再次执行时从上次返回的yield语句处继续执行。

```
def fib(max):
    n, a, b = 0, 0, 1
    while n < max:
        yield b
        a, b = b, a + b
        n = n + 1
```



函数是Python内建支持的一种封装，函数就是面向过程的程序设计的基本单元。而函数式编程（请注意多了一个“式”字）——Functional Programming，虽然也可以归结到面向过程的程序设计，但其思想更接近数学计算。函数式编程就是一种抽象程度很高的编程范式，纯粹的函数式编程语言编写的函数没有变量，因此，任意一个函数，只要输入是确定的，输出就是确定的，这种纯函数我们称之为没有副作用。而允许使用变量的程序设计语言，由于函数内部的变量状态不确定，同样的输入，可能得到不同的输出，因此，这种函数是有副作用的。函数式编程的一个特点就是，允许把函数本身作为参数传入另一个函数，还允许返回一个函数！Python对函数式编程提供部分支持。由于Python允许使用变量，因此，Python不是纯函数式编程语言。



高阶函数 思想就是,变量不光可以指向数据和对象,还可以指向函数, 函数名其实就是指向函数的变量.一个函数就可以接收另一个函数作为参数，这种函数就称之为高阶函数。

Python内建了map()和reduce()函数。map()函数接收两个参数，一个是函数，一个是序列，map将传入的函数依次作用到序列的每个元素，并把结果作为新的list返回。
```
>>> def f(x):
...     return x * x
...
>>> map(f, [1, 2, 3, 4, 5, 6, 7, 8, 9])
[1, 4, 9, 16, 25, 36, 49, 64, 81]
```

reduce把一个函数作用在一个序列[x1, x2, x3...]上，这个函数必须接收两个参数，reduce把结果继续和序列的下一个元素做累积计算.
```
reduce(f, [x1, x2, x3, x4]) = f(f(f(x1, x2), x3), x4)

>>> def add(x, y):
...     return x + y
...
>>> reduce(add, [1, 3, 5, 7, 9])
25
```

Python内建的filter()函数用于过滤序列。它接收一个函数和一个序列,把传入的函数依次作用于每个元素，根据返回值是True还是False决定保留还是丢弃该元素。

排序算法

排序也是在程序中经常用到的算法。无论使用冒泡排序还是快速排序，排序的核心是比较两个元素的大小。如果是数字，我们可以直接比较，但如果是字符串或者两个dict呢？直接比较数学上的大小是没有意义的，因此，比较的过程必须通过函数抽象出来。通常规定，对于两个元素x和y，如果认为x < y，则返回-1，如果认为x == y，则返回0，如果认为x > y，则返回1，这样，排序算法就不用关心具体的比较过程，而是根据比较结果直接排序。

Python内置的sorted()函数就可以对list进行排序, sorted()函数也是一个高阶函数，它还可以接收一个比较函数来实现自定义的排序。
```
def reversed_cmp(x, y):
    if x > y:
        return -1
    if x < y:
        return 1
    return 0

>>> sorted([36, 5, 12, 9, 21], reversed_cmp)
[36, 21, 12, 9, 5]
```

高阶函数除了可以接受函数作为参数外，还可以把函数作为结果值返回。函数中又定义了函数，内部函数可以引用外部函数的参数和局部变量，返回函数时，相关参数和变量都保存在返回的函数中，称为“闭包（Closure）”。每次调用都会返回一个新的函数，即使传入相同的参数.

返回闭包时牢记的一点就是：返回函数不要引用任何循环变量，或者后续会发生变化的变量。

如果一定要引用循环变量怎么办？方法是再创建一个函数，用该函数的参数绑定循环变量当前的值，无论该循环变量后续如何更改，已绑定到函数参数的值不变：
```
>>> def count():
...     fs = []
...     for i in range(1, 4):
...         def f(j):
...             def g():
...                 return j*j
...             return g
...         fs.append(f(i))
...     return fs
... 
>>> f1, f2, f3 = count()
>>> f1()
1
>>> f2()
4
>>> f3()
9
```


传入函数时，有时不需要显式地定义函数，直接传入匿名函数更方便。

在Python中，对匿名函数提供了有限支持. 关键字lambda表示匿名函数，冒号前面的表示函数参数。匿名函数只能有一个表达式，不用写return，返回值就是该表达式的结果。用匿名函数有个好处，因为函数没有名字，不必担心函数名冲突。此外，匿名函数也是一个函数对象，也可以把匿名函数赋值给一个变量，再利用变量来调用该函数：


装饰器

在代码运行期间动态增加功能的方式，称之为“装饰器”（Decorator）。本质上，decorator就是一个返回函数的高阶函数。Python的@语法，把decorator置于函数的定义处.
```
def log(func):
    def wrapper(*args, **kw):
        print 'call %s():' % func.__name__
        return func(*args, **kw)
    return wrapper

@log
def now():
    print '2013-12-25'

>>> now() // 原来的now()函数仍然存在，现在同名的now变量指向了新的函数，调用now()在log()函数中返回的wrapper()函数。

call now():
2013-12-25
```

wrapper()函数的参数定义是(*args, **kw)，因此，wrapper()函数可以接受任意参数的调用。

要自定义log的文本：
```
def log(text):
    def decorator(func):
        def wrapper(*args, **kw):
            print '%s %s():' % (text, func.__name__)
            return func(*args, **kw)
        return wrapper
    return decorator
```

和两层嵌套的decorator相比，3层嵌套的效果是这样的：

>>> now = log('execute')(now)
我们来剖析上面的语句，首先执行log('execute')，返回的是decorator函数，再调用返回的函数，参数是now函数，返回值最终是wrapper函数。

经过decorator装饰之后的函数，它们的__name__已经从原来的'now'变成了'wrapper', 所以，需要把原始函数的__name__等属性复制到wrapper()函数中，否则，有些依赖函数签名的代码执行就会出错。Python内置的functools.wraps就是干这个事的.
```
import functools

def log(func):
    @functools.wraps(func)
    def wrapper(*args, **kw):
        print 'call %s():' % func.__name__
        return func(*args, **kw)
    return wrapper
```

Python的functools模块提供偏函数（Partial function）。通过设定参数的默认值，可以降低函数调用的难度。而偏函数也可以做到这一点,functools.partial用于创建一个偏函数。
```
>>> int('12345', base=8)
5349
>>> import functools
>>> int2 = functools.partial(int, base=2)
>>> int2('1000000')
64
>>> int2('1010101')
85
```

简单总结functools.partial的作用就是，把一个函数的某些参数给固定住（也就是设置默认值），返回一个新的函数，调用这个新函数会更简单。

