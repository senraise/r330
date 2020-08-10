# 类

我对类的理解就是 程序化的包装，让代码变的规范化，流程化。
更好使用。

定义一个类
--------

```
class CPython:
    """ 简单的类实例 """
    n = "demo"

    def get_name(self):
        return "CPython"

```

上面例子定义了一个类，类里有一个变量 n，和一个函数 get_name
这些都是例子，可以没有。

```
class test:
  pass
```

什么都没有的类。

继续讲CPython类。

调用
----

```
a = CPython()

print(a.n)

print(a.get_name())
```

这里的a 叫做CPython类的实例。


继续定一个 带初始化函数的类
------------------------

```
class CPython1:
    """ 简单的类实例 """
    n = "demo"

    def __init__(self):
        self.data = ['1',2,3,"456"]

    def get_name(self):
        return "CPython"

    def set_name(self,name):
        self.name = name


b = CPython1()

print(b.data)

b.set_name("cpython1")
print(b.name)

```

例子中 __init__ 是在 b = CPython1()的时候调用的。

set_name 是另一个函数，调用它可以设置变量name。这里都是例子。


下一个初始化函数带参数
------------------

```
"""带参数的初始化"""
class CPython2:
    """ 简单的类实例 """
    n = "demo"

    def __init__(self,name):
        self.data = ['1',2,3,"456"]
        self.name = name

    def get_name(self):
        return self.name

    def set_name(self,name):
        self.name = name

c = CPython2("cpython2")

print(c.get_name())

c.set_name("2cpython")

print(c.get_name())
```

通过参数设置name，通过set_name修改了name。
