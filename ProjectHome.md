一个python脚本用于帮助生成C++实现文件的初始框架.
```
This is an auto converter to help you create the initial structure of
.cc/cpp file from .h file.

From void foo(); in a.h to help auto create
void foo()
{
}
int a.cc/cpp,
also support class member function, template class member
function,right now does not support fuctions declare throw() excepetions.

You may also write all your code in .h and
finally convert the non inline ones to the .cc/cpp file.
Hope it can help you write your c++ coder easier:)
```
  * 会将你在头文件中声明的函数,类成员函数自动在对应的实现文件中生成初始函数定义的初始结构.

  * 你可以将所有的代码类实现代码写到定义类的.h文件中,最后h2cc.py可以帮你自动将所有代码转到.cc/cpp文件中.

  * 如果你在.h中修改增加了函数接口,新的函数的初始实现会到.cc文件中的末尾,即不会影响前面的代码.

> 如果需要你把它们移到自己觉得更合适的位置,尤其是有namesapce的时候,需要你收工稍微修改一下.

> 而如果选择2中的实现代码从.h中转移到.cc/cpp的功能,会自动备份原始.h文件到.h.bak.

支持普通函数,类函数,模板类函数.

因为个人觉得即使是模板类也尽量把代码量大的函数转移到.cc/cpp文件中,代码会更加清晰.

另外这样也比较好区分inline和非inline函数.

由于C++语法的复杂性,我只对自己写的程序均使用它,其它特殊情况可能会有问题,

如标明throw()的函数,但是对于一般的情况都运行良好.