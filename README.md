# Python 基本概念

1、编译性语言
（1）只须编译一次就可以把源代码编译成机器语言，后面的执行无须重新编译，直接使用之前的编译结果就可以；因此其执行的效率比较高；
（2）编译性语言代表：C、C++、Pascal/Object Pascal（Delphi）；
（3）程序执行效率比较高，但比较依赖编译器，因此跨平台性差一些；

2、解释性语言
（1）源代码不能直接翻译成机器语言，而是先翻译成中间代码，再由解释器对中间代码进行解释运行；
     源代码—>中间代码—>机器语言

（2）程序不需要编译，程序在运行时才翻译成机器语言，每执行一次都要翻译一次；
（3）解释性语言代表：Python、JavaScript、Shell、Ruby、MATLAB等；
（4）运行效率一般相对比较低，依赖解释器，跨平台性好；

3、比较
（1）一般，编译性语言的运行效率比解释性语言更高；但是不能一概而论，部分解释性语言的解释器通过在运行时动态优化代码，
    甚至能使解释性语言的性能超过编译性语言；
（2）编译性语言的跨平台特性比解释性语言差一些；


is 和 '=='
Python中对象包含的三个基本要素，分别是：id(身份标识)、type(数据类型)和value(值)。
==比较操作符，is同一性运算符
is也被叫做同一性运算符，这个运算符比较判断的是对象间的唯一身份标识，也就是id是否相同
只有数值型和字符串型的情况下，a is b才为True，当a和b是tuple，list，dict或set型时，a is b为False。

>>> x = y = [4,5,6]
>>> z = [4,5,6]
>>> x == y
True
>>> x == z
True
>>> x is y
True
>>> x is z
False
>>>
>>> print id(x)
3075326572
>>> print id(y)
3075326572
>>> print id(z)
3075328140
>>> a = 1 #a和b为数值类型
>>> b = 1
>>> a is b
True
>>> id(a)
14318944
>>> id(b)
14318944
>>> a = 'cheesezh' #a和b为字符串类型
>>> b = 'cheesezh'
>>> a is b
True
>>> id(a)
42111872
>>> id(b)
42111872
>>> a = (1,2,3) #a和b为元组类型
>>> b = (1,2,3)
>>> a is b
False
>>> id(a)
15001280
>>> id(b)
14790408
>>> a = [1,2,3] #a和b为list类型
>>> b = [1,2,3]
>>> a is b
False
>>> id(a)
42091624
>>> id(b)
42082016
>>> a = {'cheese':1,'zh':2} #a和b为dict类型
>>> b = {'cheese':1,'zh':2}
>>> a is b
False
>>> id(a)
42101616
>>> id(b)
42098736
>>> a = set([1,2,3])#a和b为set类型
>>> b = set([1,2,3])
>>> a is b
False
>>> id(a)
14819976
>>> id(b)
14822256
