# Introduction #

Javascript出现某些错误的时候并不返回错误或者给出提示，缺乏严格的语法检查。
null与undeﬁned，在C预言中，如果还没有为一个指针赋值，那么应该先用null来为这个指
针初始化。对与C预言来讲，任何一个量都是有值的，不管你有没有初始化，对于值类型，
内存地址上是什么就是什么，对于指针，如果没初始化可能会出错误。对于Javascript，一
个没有初始化的类型会定义为undeﬁned。

Number
C中的数值分为signed和unsigned，而在Javascript中，都是signed。因此在对signed进行移
位的时候，javascript会保留number的符号。因此引入了>>>用于以unsigned的方式位操作
一个数。


函数原型
由于Javascript需要保持向前兼容，因此其中函数原型不一致的情况也都保留下来了。如
String.substr()和String.substring()。在遇到这种问题时，可以参考和Javascript对应的标准
ECMAScript，ECMAScript中不合适的函数都被去掉了。