# h2cc
1.h2cc.py 把头文件中的实现去掉，转成只有interfance的文件和对应的实现文件cpp,cc
2. h2interface.py  
只是去掉头文件中的实现，转成只有接口的头文件,同时为了pyplusplus能处理，做了一些hack的注释,
比如
 static bool& func()
 int func(int &&x)
 int func() = 0;
这些都被注释掉

没有做大规模复杂情况测试，复杂代码可能有bug
