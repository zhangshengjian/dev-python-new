# Python

## 常用网址

> 官网地址

https://www.python.org/



> 官网下载地址

https://www.python.org/downloads/release/python-390/





##  简单介绍

开始目录中 Python 相关文件介绍

```sh
C:\Users\eahzehs\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Python 3.9
IDLE (Python 3.9 64-bit) # Python 自带的简单的开发环境
Python 3.9 (64-bit) # Python 交互式命令行程序
Python 3.9 Manuals (64-bit) # Python 官方技术文档
Python 3.9 Module Docs (64-bit) # Python 已安装模块的文档
```





## 常用命令

> 执行 PYTHON 脚本

```sh
python [PYTHON FILE]
```





## 管理工具

pip 是 Python 包的管理工具，用来对 Python 包进行查找、下载、安装、卸载。



找到 Python 的根目录，在根目录下找到 Scripts 目录，然后进入到 Scripts 目录中



>显示 pip 的版本和路径

```sh
pip --version
```



> 获取 pip 有关的帮助

```sh
pip --help
```



>用来安装安装包

```sh
pip install [PACKAGE]

# eg.安装 Facker 的最新版本
pip install Faker

# eg.安装 beautifulsoup4 的最新版本
pip install beautifulsoup4

# eg.指定安装 beautifulsoup4 的 4.7.1 版本
pip install beautifulsoup4==4.7.1
```



> 列出已经安装的包

```sh
pip list
```



> 列出可升级的包

```sh
pip list -o
```



> 升级所安装的安装包

```sh
pip install --upgrade [PACKAGE]

# 升级为 beautifulsoup4 的最新版本
pip install --upgrade beautifulsoup4
```





## 内置函数

### print()

>输出函数

#### 输出数字

```python
# 输出数字
print(19940213)
print(19930506)
```



#### 输出字符串

```python
print('hello world')
print('hello python')
print('hello shell')
```



#### 输出含有运算符的表达式

```python
print(3 + 1)
```



#### 输出到文件

```python
# 将数据输出文件中，注意点：1.所指定的盘符存在 2.使用 file=fp
# a+ 如果文件不存在就创建，存在就在文件内容的后面继续追加
fp = open('C:/ERICSSON/DEV/dev-python/output/test.txt', 'a+')
print('hello python', file=fp)
fp.close()
```



#### 输出不进行换行

```python
print('hello', 'world', 'Python')
```



### input()

>输入函数

```python
# 输入函数 input
present = input('please input message: ')
print('input message is : ' + present)
```



```python
# 从键盘输入两个整数，计算两个整数之和
a = int(input('please input first number: '))
b = int(input('please input second number: '))
print(type(a), type(b))
print(a+b)
```



### range()

> 生成整数序列
>
> 返回值是一个迭代器对象
>
> range 类型的有点：不管 range 对象标识的整数序列有多长，所有的 range 对象占用的内存空间都是相同的，因为仅仅需要存储 start, stop 和 step，
>
> 只有当用到 range 对象时，才会去计算序列中的相关元素。
>
> in 与 not in 判断整数序列中是否存在（不存在）指定的整数

```python
# range() 的三种创建方式
"""
第一种创建方式，只有一个参数
"""
r = range(10)  # [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]，默认从 0 开始，默认相差 1，称为步长
print(r)  # range(0, 10)
print(list(r))  # list 用于查看 range 对象中的整数序列 --> list 是列表的意思

"""
第二种创建方式，两个参数
"""
r = range(1, 10)  # 指定了起始值，从 1 开始，到 10 结束（不包含 10），默认步长 1
print(list(r))  # [1, 2, 3, 4, 5, 6, 7, 8, 9]

"""
第三种创建方式，三个参数
"""
r = range(1, 10, 2)  # 指定了起始值，从 1 开始，到 10 结束（不包含 10），指定步长 2
print(list(r))  # [1, 3, 5, 7, 9]

"""
判断指定的整数 在序列中是否存在 in, not in
"""
print(10 in r)  # False, 10 不在当前的 r 这个整数序列中
print(9 in r)  # True, 9 在当前的 r 这个整数序列中

print(10 not in r)  # True
print(9 not in r)  # False

print(range(1, 20, 1))  # [1...19]
print(range(1, 101, 1))  # [1...100]
```

## 转义字符

```python
# 转义字符
print('hello\nworld')  # \ + 转移功能的首字母 n --> newline 的首字母表示换行
print('hello\tworld')  # tab 相当于 4 个空格
print('helloooo\tworld')

print('hello\rworld')  # \r 回车 enter, world 会把 hello 覆盖掉

print('hello\bworld')  # \b 退一个格, 将 o 退没有了

print('http:\\\\www.baidu.com')  # \\ 反斜杠

print('teacher say: \'hello python\'')  #  \' 单引号

# 原字符，不希望字符串中的转义字符起作用，就是使用原字符，即在字符串之前加上 r，或 R
# 注意事项：最后一个字符不能是反斜线，可以是两个不能单个
print(r'hello\nworld')
print(r'hello\nworld\\')

print(R'hello\nworld')
print(R'hello\nworld\\')
```



## 二进制与字符编码

```python
# 二进制
print(chr(0b0101111100100000))  # 0b 表示张的二进制
print(ord('张'))  # 24352

# 字符编码
# 二进制 0,1 ---> ASCII ---> GB2312(80) ---> GBK(90) ---> GB18030(00) ---> Unicode(几乎包含了全世界的字符) ---> UTF-8
#					 ---> 其他国家的字符编码---------------------------->
```



## 标识符和保留字

```python
import keyword

print(keyword.kwlist)

['False', 'None', 'True', '__peg_parser__', 'and', 'as', 'assert', 'async', 'await', 'break', 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise', 'return', 'try', 'while', 'with', 'yield']
```



规则：变量、函数、类、模块和其他对象起的名字就叫标识符

- 字母、数字、下划线
- 不能以数字开头
- 不能是保留字
- 严格区分大小写



## 变量

### 定义和使用

```python
# shengjian zhang
# 1578072555696
# <class 'str'>

name = 'shengjian zhang'

print('标识(id)', id(name))  # 标识

print('类型(type)', type(name))  # 类型

print('值(value)', name)  # 值
```



### 多次赋值

```python
name = 'shengjian zhang'

name = 'xinxin luo'

print('值(value)', name)  # 值
```



## 数据类型

### 常用数据类型

#### 整数类型

int -> 98

```python
# 数据类型 int
n1 = 100
n2 = -90
n3 = 0
print(n1, type(n1))
print(n2, type(n2))
print(n3, type(n3))

# 整数可以表示为二进制，十进制，八进制，十六进制
print('十进制', 626)
print('二进制', 0b101100111)  # 二进制以 0b 开头
print('八进制', 0o176)  # 八进制以 0o 开头
print('十六进制', 0x1EAF)  # 十六进制以 0x 开头
```



#### 浮点数类型

float -> 3.14159

浮点数整数部分和小数部分组成，浮点数存储不精确，使用浮点数进行计算时，可能会出现小数位数不确定的情况，解决方案：导入模块 decimal

```python
num1 = 1.1
num2 = 2.2
print(num1 + num2)

from decimal import Decimal

print(Decimal('1.1') + Decimal('2.2'))

3.3000000000000003
3.3
```



#### 布尔类型

bool -> True,False

```python
# 数据类型 bool
f1 = True
f2 = False
print(f1, type(f1))
print(f2, type(f2))

# 布尔值可以转成整数计算
print(f1+1)  # 2 1+1 = 2，True = 1
print(f2+1)  # 1 0+1 = 2，False = 0
```



#### 字符串类型

str ->'你好，Python'

```python
# 数据类型 str
str1 = 'hello python'
str2 = "hello python"
str3 = """hello
python"""
str4 = '''hello
python'''

print(str1, type(str1))
print(str2, type(str2))
print(str3, type(str3))
print(str4, type(str4))
```



### 类型转换

#### 字符串类型

```python
name = '张三'
age = 20

print(type(name), type(age))  # 说明 name 与 age 的数据类型不相同
# print('我叫' + name + '年龄' + age + '岁')  # 当将 str 类型与 int 类型进行连接时，报错，解决方案：使用类型转换
print('我叫' + name + '年龄' + str(age) + '岁')  # 将 int 类型通过 str() 函数转成了 str 类型

print('---------------------------str() 将其它类型转成 str 类型---------------------------')
a = 10
b = 198.8
c = False
print(type(a), type(b), type(c))
print(str(a), str(b), str(c), type(str(a)), type(str(b)), type(str(c)))
```

#### 整数类型

```python
print('---------------------------int() 将其它类型转成 int 类型---------------------------')
s1 = '128'
f1 = 98.7
s2 = '76.77'
ff = True
s3 = 'hello'
print(type(s1), type(f1), type(s2), type(ff), type(s3))
print(int(s1), type(int(s1)))  # 将 str 转成 int 类型，字符串为数字串
print(int(f1), type(int(f1)))  # 将 float 转成 int 类型，截取整数部分，舍掉小数部分
# print(int(s2), type(int(s2))) # 将 str 转成 int 类型，报错，因为字符串为小数串
print(int(ff), type(int(ff)))  # 将 bool 转成 int 类型
# print(int(s3), type(int(s3)))  # 将 str 转成 int 类型时，字符串必须为数字串(整数)，非数字串是不允许转换的
```

#### 浮点数类型

```python
print('---------------------------float() 将其它类型转成 float 类型---------------------------')
s1 = '128.98'
s2 = '76'
ff = True
s3 = 'hello'
i = 98
print(type(s1), type(s2), type(ff), type(s3))
print(float(s1), type(float(s1)))
print(float(s2), type(float(s2)))
print(float(ff), type(float(ff)))
#  print(float(s3), type(float(s3))) #  字符串中的数据如果是非数字串，则不允许转换
print(float(i), type(float(i)))
```

## 注释

### 单行注释

```python
# print hello world
print('hello python')
```



### 多行注释

```python
'''
hello
python
'''

"""
hello
python
hello
world
"""
```



## 运算符

### 算术运算符

```python
print(1 + 1)  # 加法运算
print(1 - 1)  # 减法运算
print(2 * 4)  # 乘法运算
print(1 / 2)  # 除法运算
print(11 / 2)  # 除法运算
print(11 // 2)  # 整除运算
print(11 % 2)  # 取余运算
print(2 ** 2)  # 表示的是 2 的 2 次方
print(2 ** 3)  # 表示的是 2 的 3 次方

print(9 // 4)  # 2
print(-9 // -4)  # 2

print(9 // -4)  # -3
print(-9 // 4)  # -3 一正一负的整数公式，向下取整

print(9 % -4)  # -3 公式 余数=被除数-除数*商  9-(-4)*(-3) 9-12=-3
print(-9 % 4)  # 3 公式 余数=被除数-除数*商 -9-4*(-3)=3
```



### 赋值运算符

```python
# 赋值运算符，运算顺序从右到左
a = 3 * 4
print(a)

# 链式赋值
a = b = c = 20
print(a, b, c)
print(a, id(a))
print(b, id(b))
print(c, id(c))

# 系列解包赋值
a, b, c = 20, 20, 20
print(a, b, c)
print(a, id(a))
print(b, id(b))
print(c, id(c))

# 值交换
i, j = 10, 20
print(i, j)
i, j = j, i
print(i, j)

# 参数赋值
a = 20
a += 30
print(a)

a -= 10
print(a)

a *= 2
print(a)

a /= 20
print(a)

a //= 2
print(a)

a %= 2
print(a)

```



### 比较运算符

```python
# 比较运算符
a, b = 10, 20
print(a > b)
print(a < b)
print(a >= b)
print(a <= b)
print(a == b)
print(a != b)

"""
一个 = 称为赋值运算符，== 称为比较运算符
一个变量由三部分组成，标识、类型、值
== 比较的是值还是标识呢？比较的是值
比较对象的标识使用 is
"""
a = 10
b = 10
print(a == b)  # True 说明 a 和 b 的值相等
print(a is b)  # True 说明 a 和 b 的标识相等


list1 = [11, 22, 33, 44]
list2 = [11, 22, 33, 44]
print(list1 == list2)  # value => True
print(list1 is list2)  # id => False
print(id(list1), id(list2))
print(list1 is not list2)
```



### 布尔运算符

```python
# 布尔运算符
a, b = 1, 2
print('------------------------ and ------------------------')
print(a == 1 and b == 2)  # True    True and True => True
print(a == 1 and b < 2)  # False    True and False => False
print(a != 1 and b == 2)  # False   False and True => False
print(a != 1 and b != 2)  # False   False and False => False

print('------------------------ or ------------------------')
print(a == 1 or b == 2)  # True    True or True => True
print(a == 1 or b < 2)  # True    True or False => True
print(a != 1 or b == 2)  # True   False or True => True
print(a != 1 or b != 2)  # False   False or False => False

''' 对 bool 类型的操作数取反 '''
print('------------------------ not ------------------------')
f = True
f2 = False
print(not f)  # True => False
print(not f2)  # False => True

print('------------------------ in / not in ------------------------')
s = 'hello world'
print('w' in s)
print('k' in s)
print('w' not in s)
print('k' not in s)
```



### 位运算

```python
# 位运算
print(4 & 8)  # 按位与 &，同为 1 时结果为 1
print(4 | 8)  # 按位或 |，同为 0 时结果为 0
print(4 << 1)  # 向左移动 1 位(移动一个位置)，相当于乘以 2
print(4 << 2)  # 向左移动 2 位(移动两个位置)
print(4 >> 1)  # 向右移动 1 位，相当于除以 2
print(4 >> 2)  # 向右移动 2 位，相当于除以 4
```



### 运算符的优先级

```
() -> 算术运算符 -> 位运算符 -> 比较运算符 -> 布尔运算符 -> 赋值运算符
```



## 对象的布尔值

```python
# 程序的组织结构 - 顺序结构
print('-----------------------all objects bool() are False-----------------------')
print(bool(False))
print(bool(0))
print(bool(0.0))
print(bool(None))
print(bool(''))
print(bool(""))
print(bool([]))  # 空列表
print(bool(list()))  # 空列表
print(bool(()))  # 空元组
print(bool(tuple()))  # 空元组
print(bool({}))  # 空字典
print(bool(dict()))  # 空字典
print(bool(set()))  #  空集合

print('-----------------------all objects bool() are True-----------------------')
print(bool(18))
print(bool(True))
print(bool('hello python'))
```



## 分支结构

### 单分支结构

```python
money = 1000  # 余额
s = int(input('please input money: '))
if money >= s:
    money = money - s
    print('take money successfully, balance is', money)
```

### 双分支结构

```python
money = 1000  # 余额
s = int(input('please input money: '))
if money >= s:
    money = money - s
    print('take money successfully, balance is', money)
else:
    print('take money failed, balance is not enough, balance is', money)
```

### 多分支结构

```python
s = int(input('please input score: '))
if s == 100:
    print('A')
elif 100 > s >= 90:
    print('B')
elif 90 > s >= 80:
    print('C')
elif 80 > s >= 70:
    print('D')
elif 70 > s >= 60:
    print('E')
else:
    print('Z')
```

### 嵌套 if 的使用

```python
s = input('please confirm if you are a member(Y/N): ')
m = int(input('please input money: '))
if s == 'Y':
    if m >= 200:
        print('discount 0.8, cost money', m * 0.8)
    elif 200 > m >= 100:
        print('discount 0.9, cost money', m * 0.9)
    else:
        print('no discount, cost money', m)
else:
    if m >= 200:
        print('discount 0.95, cost money', m * 0.95)
    else:
        print('no discount, cost money', m)
```



## 条件表达式

```python
num_a = int(input('please input number1: '))
num_b = int(input('please input number2: '))
'''
if num_a >= num_b:
    print(num_a, '>=', num_b)
else:
    print(num_a, '<', num_b)
'''

print('use condition expression to compare')
print(str(num_a) + '>=' + str(num_b) if num_a >= num_b else str(num_a) + '<' + str(num_b))
```



## pass 语句

```python
# pass 语句 什么都不做，只是一个占位符，用到需要写语句的地方
num_a = int(input('please input number1: '))
num_b = int(input('please input number2: '))
if num_a >= num_b:
    pass
else:
    pass
```



## 循环结构

### while

```python
"""
打印输出 1-9
"""
a = 1
while a < 10:
    print(a)
    a += 1

"""
计算 1-4 的和
"""
i = s = 0
while i < 5:
    s += i
    i += 1

print(s)  # 1+2+3+4



"""
计算 1-100 之间的偶数和
"""
i = 1
s = 0
while i < 101:
    # if i % 2 == 0:
    if not bool(i % 2):
        s += i
    i += 1

print(s)
```



### for in

```python
for item in 'PYTHON':
    print(item)

for i in range(1, 10):
    print(i)

for _ in range(5):
    print('hello python')

s = 0
for it in range(1, 101):
    if it % 2 == 0:
        s += it

print(s)

------------------------------------------
P
Y
T
H
O
N
1
2
3
4
5
6
7
8
9
hello python
hello python
hello python
hello python
hello python
2550
```



```python
for item in range(100, 1000):
    ge = item % 10  # 个位
    shi = item // 10 % 10  # 十位
    bai = item // 100  # 百位

    # print(bai, shi, ge)
    if ge ** 3 + shi ** 3 + bai ** 3 == item:
        print(item)
-----------------------------------------
153
370
371
407
```



### 嵌套循环

```python
for i in range(1, 4):  # 行表，执行三次，一次是一行
    for j in range(1, 5):
        print('*', end='\t')  # 不换行输出
    print()  # 打行

-------------------------------------------------
*	*	*	*	
*	*	*	*	
*	*	*	*	
```



示例：打印九九乘法表

```python
for i in range(1, 10):
    for j in range(1, i+1):
        print('*', end='\t')
    print()

print('----------------------------------------')


for i in range(1, 10):
    for j in range(1, i+1):
        print(str(i) + '*' + str(j) + '=' + str(i*j), end='\t')
    print()

######################################################
*	
*	*	
*	*	*	
*	*	*	*	
*	*	*	*	*	
*	*	*	*	*	*	
*	*	*	*	*	*	*	
*	*	*	*	*	*	*	*	
*	*	*	*	*	*	*	*	*	
----------------------------------------
1*1=1	
2*1=2	2*2=4	
3*1=3	3*2=6	3*3=9	
4*1=4	4*2=8	4*3=12	4*4=16	
5*1=5	5*2=10	5*3=15	5*4=20	5*5=25	
6*1=6	6*2=12	6*3=18	6*4=24	6*5=30	6*6=36	
7*1=7	7*2=14	7*3=21	7*4=28	7*5=35	7*6=42	7*7=49	
8*1=8	8*2=16	8*3=24	8*4=32	8*5=40	8*6=48	8*7=56	8*8=64	
9*1=9	9*2=18	9*3=27	9*4=36	9*5=45	9*6=54	9*7=63	9*8=72	9*9=81	
```

## 流程控制语句

### break

```python
# for => break
for item in range(3):
    pwd = input('please input password: ')
    if pwd == '8888':
        print('password is correct')
        break
    else:
        print('password is incorrect')
        

# while => break
a = 0
while a < 3:
    pwd = input('please input password: ')
    if pwd == '8888':
        print('password is correct')
        break
    else:
        print('password is incorrect')

    a += 1
```



### continue

```python
print('continue - for')
for item in range(1, 51):
    if item % 5 == 0:
        print(item)

print('continue - while')
i = 1
while i < 51:
    if i % 5 == 0:
        print(i)
    i += 1
```



### else

> else 和 while 或者 for 循环结合使用时，如果循环中最终未遇到 break（即循环正常执行完），则需要执行与其对应的 else 中的代码块

```python
for item in range(3):
    pwd = input('please input password: ')
    if pwd == '8888':
        print('password is correct')
        break
    else:
        print('password is incorrect')
else:
    print('sorry, three times all failed')
    

a = 0
while a < 3:
    pwd = input('please input password: ')
    if pwd == '8888':
        print('password is correct')
        break
    else:
        print('password is incorrect')

    a += 1
else:
    print('sorry, three times all failed')
```



## 列表

### 为什么需要列表

- 变量可以存储一个元素，二列表是一个 "大容器" 可以存储 N 多个元素，程序可以方便地对这些数据进行整体操作
- 列表相当于其他语言中的数组



### 列表对象的创建

```python
"""
创建列表的第一种方式，使用 []
"""
lst = ['hello', 'world', 98]

print(lst)

"""
创建列表的第二种方式，使用内置函数 list()
"""
lst = list(['hello', 'world', 98])

print(lst)
```



### 列表的特点

- 列表元素按顺序有序排序
- 索引映射唯一数据
- 列表可以存储重复数据
- 任意数据类型混存
- 根据需要动态分配的回收内存

```python
lst = ['hello', 'world', 98, 'hello']

print(lst)
print(lst[0], lst[-3])
```



### 列表 - 查询操作

#### 获取指定元素的索引

- 如果知道列表中存在 N 个相同元素，只返回相同元素中的第一个元素的索引
- 如果查询的元素在列表中不存在，则会抛出 ValueError
- 可以在指定的 startIndex 和 stopIndex 之间进行查找

```python
lst = ['hello', 'world', 98, 'hello']

print(lst.index('hello'))

# print(lst.index('Python'))  # ValueError: 'Python' is not in list
# print(lst.index('hello', 1, 3))  # ValueError: 'hello' is not in list

print(lst.index('hello', 1, 4))  # 3
```



#### 获取列表中指定的元素

- 正向索引从 0 到 N - 1，举例：lst[0]
- 逆向索引从 -N 到 -1，举例：list[-N]
- 指定索引不存，抛出 IndexError

```python
lst = ['hello', 'world', 98, 'hello', 'world', 234]
# 获取索引为 2 的元素
print(lst[2])

# 获取索引为 -3 的元素
print(lst[-3])

# 获取索引为 10 的元素
print(lst[10])  # IndexError: list index out of range
```



#### 获取列表中的多元素

切片操作

语法格式： 列表名[start : stop : step]

```python
lst = [10, 20, 30, 40, 50, 60, 70, 80]

# start = 1, stop = 6, step = 1
print(lst[1:6:1])  # [20, 30, 40, 50, 60]

print('原列表', id(lst))
lst2 = lst[1:6:1]
print('切的片段', id(lst2))

print(lst[1:6])  # 默认步长为 1
print(lst[1:6:])  # 默认步长为 1

# start = 1, stop = 6, step = 2
print(lst[1:6:2])
# stop = 6, step = 2, start 采用默认
print(lst[:6:2])
# start = 1, step = 2, stop 采用默认
print(lst[1::2])

print('----------------------- step 步长为负数的情况 -----------------------')
print(lst)
print(lst[::-1])  # 倒序打印 lst 元素
# start = 7, stop 省略, step = -1
print(lst[7::-1])
# start = 6, stop = 0, step = -2
print(lst[6:0:-2])

##################################################################
[20, 30, 40, 50, 60]
原列表 2257207968064
切的片段 2257207967936
[20, 30, 40, 50, 60]
[20, 30, 40, 50, 60]
[20, 40, 60]
[10, 30, 50]
[20, 40, 60, 80]
----------------------- step 步长为负数的情况 -----------------------
[10, 20, 30, 40, 50, 60, 70, 80]
[80, 70, 60, 50, 40, 30, 20, 10]
[80, 70, 60, 50, 40, 30, 20, 10]
[70, 50, 30]
```



#### 列表元素的判断及遍历

```python
lst = [10, 20, 'python', 'hello']
print(10 in lst)
print(100 in lst)
print(10 not in lst)
print(100 not in lst)
print('-------------------------------')
for item in lst:
    print(item)
```



### 列表元素 - 操作

#### 添加操作

```python
# append() 在列表的末尾添加一个元素
lst = [10, 20, 30]
print('add before:', lst, id(lst))
lst.append(100)
print('add after:', lst, id(lst))

# extend() 在列表的末尾至少添加一个元素
lst2 = ['hello', 'world']
# lst.append(lst2)  # 将 lst2 作为一个元素添加到元素的末尾
lst.extend(lst2)  # 将 lst 的末尾一次性添加多个元素
print(lst)

# insert() 在列表的任意位置上添加一个元素
lst.insert(1, 90)
print(lst)

lst3 = [True, False, 'hello']
# 在列表的任意位置上添加至少一个元素
lst[1:] = lst3  # 切片
print(lst)
```



#### 删除操作

```python
# remove() 删除元素
lst = [10, 20, 30, 40, 50, 60, 30]
print(lst)
lst.remove(30)  # 从列表中移除一个元素，如果有重复元素只移第一个元素
print(lst)
# lst.remove(100)  # ValueError: list.remove(x): x not in list

# pop() 根据索引移除元素
lst.pop(1)
print(lst)
# lst.pop(5) # IndexError: pop index out of range 如果指定的索引位置不存在，将抛出异常
lst.pop()  # 如果不指定参数(索引)，将删除列表中的最后一个元素
print(lst)

# 切片操作
print('------------ 切片操作 - 删除至少一个元素，将产生一个新的列表对象 ------------')
new_list = lst[1:3]
print('原列表', lst)
print('切片后的列表', new_list)

"""
不产生新的列表对象，而是删除原列表中的内容
"""
lst[1:3] = []
print(lst)

"""
清除列表中的所有元素
"""
lst.clear()
print(lst)

"""
del 语句将列表对象删除
"""
del lst
# print(lst) NameError: name 'lst' is not defined
```



#### 修改操作

```python
lst = [10, 20, 30, 40]
# 一次修改一个值
lst[2] = 100
print(lst)

# 切片修改
lst[1:3] = [300, 400, 500, 600]
print(lst)

###########################################
[10, 20, 100, 40]
[10, 300, 400, 500, 600, 40]
```



#### 排序操作

```python
# 调用 sort() 方法
lst = [20, 40, 10, 98, 54]
print('sort before:', lst, id(lst))
# 开始排序，调用列表对象的 sort 方法，升序排序
lst.sort()
print('sort after:', lst, id(lst))

# 通过指定关键字参数，将列表中的元素进行升序排序
lst.sort(reverse=True)  # reverse=True 表示降序排序，reverse=False 就是升序排序
print(lst)
lst.sort(reverse=False)
print(lst)

# 调用内置函数 sorted()
print('------------------ 使用内置函数 sorted() 对列表进行排序，将产生一个新的列表对象 ------------------')
lst = [20, 40, 10, 98, 54]
print('原列表', lst)
# 开始排序
new_list = sorted(lst)
print(lst)
print(new_list)
# 指定关键字参数，实现列表元素的降序排序
desc_list = sorted(lst, reverse=True)
print(desc_list)
```



### 列表生成式

```python
lst = [i for i in range(1, 10)]
print(lst)

lst = [i*i for i in range(1, 10)]
print(lst)

# print 2, 4, 6, 8, 10
lst2 = [i*2 for i in range(1, 6)]
print(lst2)
```



## 字典

### 什么是字典

- Python 内置的数据结构之一，与列表一样是一个可变序列
- 以键值对的方式存储元素，字典是一个无序的序列



### 字典的实现原理

字典的实现原理与查字典类似，查字典是先根据部首或拼音查找汉字对应的页码，Python 中的字典是根据 key 查找 value 所在的位置。



### 字典的创建

```python
"""
使用 {} 创建字典
"""
scores = {'张三' : 100, '李四' : 98, '王五' : 45}
print(scores)
print(type(scores))

"""
使用 dict()
"""
student = dict(name='jack', age=20)
print(student)

"""
空字典
"""
d = {}
print(d)
```



### 字典元素的获取

```python
scores = {'张三': 100, '李四': 98, '王五': 45}
"""
使用 []
"""
print(scores['张三'])
# print(scores['陈六'])  # KeyError: '陈六'

"""
get()
"""
print(scores.get('张三'))
print(scores.get('陈六'))  # None
print(scores.get('张飞', 999))  # 99 是在查找 '张飞' 所对的 value 不存在时，提供的一个默认值
```



### 字典元素的操作

```python
"""
key 的判断
"""
scores = {'张三': 100, '李四': 98, '王五': 45}
print('张三' in scores)
print('张三' not in scores)


"""
字典元素的删除，删除指定的 key value 对
"""
del scores['李四']
print(scores)

"""
清空字典的元素
"""
scores.clear()
print(scores)

"""
字典元素的新增
"""
scores['陈六'] = 99
print(scores)

"""
字典元素的修改
"""
scores['陈六'] = 999
print(scores)
```



### 获取字典视图

```python
scores = {'张三': 100, '李四': 98, '王五': 45}
# 获取所有的 key
keys = scores.keys()
print(keys)
print(type(keys))
print(list(keys))  # 将所有的 key 组成的视图转成列表

# 获取所有的 value
values = scores.values()
print(values)
print(type(values))
print(list(values))

# 获取所有的 key value 对
items = scores.items()
print(items)
print(list(items))  # () 元组，转换之后的列表元素是有元组组成
```



### 字典元素的遍历

```python
scores = {'张三': 100, '李四': 98, '王五': 45}
for item in scores:
    print(item)
    
for item in scores:
    print(item, scores[item], scores.get(item))
    
###########################################
张三
李四
王五
张三 100 100
李四 98 98
王五 45 45
```



### 字典的特点

```python
d = {'name': '张三', 'name': '李四'}  # key 不允许重复，如果重复取后面的 key 和对应的 value
print(d)

d = {'name': '张三', 'nickname': '张三'}  # value 可以重复
print(d)

lst = [10, 20, 30]
lst.insert(1, 100)
print(lst)

d = {lst: 100}  # TypeError: unhashable type: 'list' list 不可以作为字典的 key 存在
print(d)
```



### 字典生成式

```python
items = ['Fruits', 'Books', 'Others']
prices = [96, 99, 23]
d = {item.upper(): price for item, price in zip(items, prices)}
print(d)
```



## 元组

### 什么是元组

#### 元组定义

Python 内置的数据结构之一，是一个不可变序列

#### 可变序列和不可变序列

```python
"""
可变序列 列表，字典

可以对序列执行增、删、改操作，对象地址不发生更改
"""
lst = [10, 20, 45]
print(id(lst))
lst.append(300)
print(id(lst))

"""
不可变序列，字符串，元组

没有增、删、改的操作
"""
s = 'hello'
print(id(s))
s = s + 'world'
print(id(s))
print(s)

##############################
1658500563776
1658500563776
1658500563504
1658500564144
helloworld
```



### 元组的创建方式

```python
"""
元组的创建方式
"""
"""
第一种创建方式，使用 ()
"""
t = ('Python', 'hello', 98)
print(t)
print(type(t))

t2 = 'Python', 'hello', 98
print(t2)
print(type(t2))

t3 = ('Python',)  # 只包含一个元组的元素需要带上逗号和小括号
print(t3)
print(type(t3))

"""
第二种创建方式，使用内置函数 tuple()
"""
t1 = tuple(('Python', 'world', 98))
print(t1)
print(type(t1))

"""
空列表的创建方式
"""
lst = []
lst1 = list()

"""
空字典的创建方式
"""
d = {}
d2 = dict()

"""
空元组的创建方式
"""
t = ()
t2 = tuple()

print('空列表', lst, lst1)
print('空字典', d, d2)
print('空元组', t, t2)
```



### 为什么要将元组设计成不可变序列

- 多任务环境下，同事操作对象时不需要加锁
- 因此，在程序中尽量使用不可变序列

> 注意事项：元组中存储的是对象的引用
>
> a) 如果元组中对象本身不可变对象，则不能再引用其它对象
>
> b) 如果元组中的对象是可变对象，则可变对象的引用不允许改变，但数据可以改变

```python
t = (10, [20, 30], 9)
print(t)
print(type(t))
print(t[0], type(t[0]), id(t[0]))
print(t[1], type(t[1]), id(t[1]))
print(t[2], type(t[2]), id(t[2]))

"""
尝试将 t[1] 修改为 100
"""
print(id(100))
# t[1] = 100  # TypeError: 'tuple' object does not support item assignment 元组是不允许修改元素的
"""
由于 [20,30] 是列表，而列表是可变序列的，所以可以想列表中添加元素，而列表的内存地址不变
"""
t[1].append(40)  # 向列表中添加内容，list 是可变的
print(t, id(t[1]))
```



### 元组的遍历

```python
"""
元组的遍历
"""
t = ('Python', 'world', 98)
"""
第一种获取元组的方式，使用索引
"""
print(t[0])
print(t[1])
print(t[2])
# print(t[3])  # IndexError: tuple index out of range
"""
遍历元组
"""
for item in t:
    print(item)
```



## 集合

### 集合的概述与创建

集合

- Python 语言提供的内置数据结构
- 与列表、字典一样都属于可变类型的序列
- 集合是没有 value 的字典

```python
"""
集合的创建方式
"""

"""
第一种创建方式使用 {}
"""
s = {2, 3, 4, 5, 6, 7, 6, 7}  # 集合中的元素不允许重复
print(s)

"""
第二种创建方式使用 set()
"""
s1 = set(range(6))
print(s1, type(s1))

# 将列表转成集合
s2 = set([1, 2, 4, 5, 5, 5, 6])
print(s2, type(s2))

# 将元组转成集合
s3 = set((1, 2, 3, 4, 5, 55, 6, 65))  # 集合中的元素是无序的
print(s3, type(s3))

# 将字符串转成集合
s4 = set('Python')
print(s4)

# 将集合转成集合
s5 = set({12, 4, 23, 23, 42})
print(s5)

# 定义一个空集合
s6 = {}  # dict 字典类型
print(type(s6))

s7 = set()
print(type(s7))
```



### 集合元素 - 操作

#### 判断操作

```python
# 集合的相关操作
s = {10, 20, 30, 405, 60}

"""
集合元素的判断操作
"""
print(10 in s)  # True
print(100 in s)  # False
print(10 not in s)  # False
print(100 not in s)  # True
```



#### 新增操作

```python
"""
集合元素的新增操作
"""
# 集合的相关操作
s = {10, 20, 30, 405, 60}

# 一次添加一个元素
s.add(80)
print(s)
# 一次至少添加一个元素
s.update({200, 400, 500})
print(s)
s.update([100, 99, 8])
s.update((22, 33, 44))
print(s)
```



#### 删除操作

```python
"""
集合元素的删除操作
"""
# 集合的相关操作
s = {10, 20, 30, 405, 60}

s.remove(100)
print(s)
# s.remove(2000)
# print(s)  # KeyError: 2000

s.discard(2000)
print(s)

s.pop()
print(s)

# 全部清除
s.clear()
print(s)
```



### 集合间的关系

```python
"""
两个集合是否相等（元素相同，就相等）
"""
s = {10, 20, 30, 40}
s2 = {30, 40, 20, 10}
print(s == s2)  # True
print(s != s2)  # False

"""
一个集合是否是另一个集合的子集
"""
s1 = {10, 20, 30, 40, 50, 60}
s2 = {10, 20, 30, 40}
s3 = {10, 20, 90}
print(s2.issubset(s1))  # True
print(s3.issubset(s1))  # False

"""
一个集合是否是另一个集合的超集
"""
print(s1.issuperset(s2))  # True
print(s1.issuperset(s3))  # False


"""
两个集合是否含有交集
"""
print(s2.isdisjoint(s3))  # False 有交集为 False

s4 = {100, 200, 300}
print(s2.isdisjoint(s4))  # True 没有交集为 True
```



### 集合的数据操作

```python
"""
集合交集
"""
s1 = {10, 20, 30, 40}
s2 = {20, 30, 40, 50, 60}
print(s1.intersection(s2))
print(s1 & s2)  # intersection() <=> &

print(s1)
print(s2)

"""
并集操作
"""
print(s1.union(s2))
print(s1 | s2)  # union() <=> |
print(s1)
print(s2)

"""
差集操作
"""
print(s1.difference(s2))  # {10}
print(s1 - s2)  # difference() <=> -
print(s2.difference(s1))  # {50, 60}

"""
对称差集
"""
print(s1.symmetric_difference(s2))  # {50, 10, 60}
print(s1 ^ s2)
```



### 集合生成式

```python
lst = {i for i in range(1, 10)}
print(lst)

lst = {i*i for i in range(1, 10)}
print(lst)

# print 2, 4, 6, 8, 10
lst2 = {i*2 for i in range(1, 6)}
print(lst2)

#########################################
{1, 2, 3, 4, 5, 6, 7, 8, 9}
{64, 1, 4, 36, 9, 16, 49, 81, 25}
{2, 4, 6, 8, 10}
```



### 总结

|  数据结构  | 是否可变 |          是否重复          | 是否有序 |  定义符号   |
| :--------: | :------: | :------------------------: | :------: | :---------: |
| 列表 list  |   可变   |           可重复           |   有序   |     []      |
| 元组 tuple |  不可变  |           可重复           |   有序   |     ()      |
| 字典 dict  |   可变   | key 不可重复，value 可重复 |   无序   | {key:value} |
|  集合 set  |   可变   |          不可重复          |   无序   |     {}      |





## 字符串

### 创建与驻留机制

字符串：在 Python 中字符串是基本数据类型，是一个不可变的字符序列。

字符串驻留机制：仅保存一份相同且不可变字符串的方法，不同的值被存放在字符串的驻留池中，Python 的驻留机制对相同的字符串只保留一份拷贝，

后续创建相同字符串时，不会开辟新空间，而是把该字符串的地址赋给新创建的变量。

```python
a = 'Python'
b = "Python"
c = '''Python'''
print(a, id(a))
print(b, id(b))
print(c, id(c))
```



字符串驻留机制的优缺点：

- 当需要值相同的字符串时，可以直接从字符串池里拿来使用，避免频繁的创建和销毁，提升效率和节约内存，因此拼接字符串和修改字符串是会比较影响性能的
- 在需要进行字符串拼接时建议使用 str 类型的 join 方法，而非 +，因为 join() 方法是先计算出所有字符串中的长度，然后再拷贝，只 new 一次对象，效率要比 "+" 效率高

### 字符串的查询操作

```python
# 字符串的查询操作
s = 'hello,hello'
print(s.index('lo'))  # 3
print(s.find('lo'))  # 3
print(s.rindex('lo'))  # 9
print(s.rfind('lo'))  # 9

# print(s.index('k'))  # ValueError: substring not found
print(s.find('k'))  # -1
# print(s.rindex('k'))  # ValueError: substring not found
print(s.rfind('k'))  # -1
```



### 字符串的大小写转换操作方法

```python
# 字符串中的大小写转换的方法
s = 'hello,Python'
a = s.upper()  # 转换成大写之后，会产生一个新的字符串对象
print(a, id(a))
print(s, id(s))

b = s.lower()  # 转换成小写之后，会产生一个新的字符串对象
print(b, id(b))
print(s, id(s))
print(b == s)  # True
print(b is s)  # False

s2 = s.swapcase()  # 把字符串中所有大写字母转换成小写字母，把所有小写字母都转换成大写字母
print(s2)

s3 = s.capitalize()  # 把第一个字符转换成大写，把其余字符转换成小写
print(s3)

s4 = s.title()  # 把每个单词的第一个字符转换成大写，把每个单词的剩余字符转换为小写
print(s4)
```



### 字符串内容对齐操作方法

```python
"""
左对齐
"""
s = 'hello'
print(s.ljust(20, '*'))
print(s.ljust(10))
print(s.ljust(20))

"""
右对齐
"""
print(s.rjust(20, '*'))
print(s.rjust(20))
print(s.rjust(10))

"""
右对齐，使用 0 进行填充
"""
print(s.zfill(20))
print(s.zfill(10))
print('-8910'.zfill(8))
```



### 字符串的分割

```python
s = 'hello world Python'
lst = s.split()
print(lst)

s1 = 'hello|world|Python'
print(s1.split(sep='|'))
print(s1.split(sep='|', maxsplit=1))

print('------------------------------')
"""
rsplit() 从右侧开始分割
"""
print(s.rsplit())
print(s1.rsplit('|'))
print(s1.rsplit(sep='|', maxsplit=1))
```



### 字符串判断的相关方法

```python
"""
isidentifier() 判断指定的字符串是不是合法的标识符
"""
s = 'hello,python'
print('1', s.isidentifier())  # False
print('2', 'hello'.isidentifier())  # True
print('3', '张三'.isidentifier())  # True
print('4', '张三_123'.isidentifier())  # True

"""
isspace() 判断指定的字符串是否全部由空白字符组成（回车、换行、水平制表符）
"""
print('5', '\t'.isspace())  # True

"""
isalpha() 判断指定的字符串是否全部由字母组成
"""
print('6', 'abc'.isalpha())  # True
print('7', '张三'.isalpha())  # True ?
print('8', '张三1'.isalpha())  # False

"""
isdecimal() 判断指定字符串是否全部由十进制的数字组成
"""
print('9', '123'.isdecimal())  # True
print('10', '123四'.isdecimal())  # False
print('11', 'ⅡⅡⅡ'.isdecimal())  # False

"""
isnumeric() 判断指定的字符串是否全部由数字组成
"""
print('12', '123'.isnumeric())  # True
print('13', '123四'.isnumeric())  # True
print('14', 'ⅡⅡⅡ'.isnumeric())  # True

"""
isalnum() 判断指定的字符串是否全部由字母和数字组成
"""
print('15', 'abc1'.isalnum())  # True
print('16', '张三123'.isalnum())  # True
print('17', 'abc!'.isalnum())  # False
```



### 替换与合并

```python
"""
replace() 将 Python 替换成 Java
"""
s = 'hello,Python'
print(s.replace('Python', 'Java'))

"""
replace() 将前两个 Python 替换成 Java
"""
s1 = 'hello,Python,Python,Python'
print(s1.replace('Python', 'Java', 2))

"""
将 List 中的元素连接
"""
lst = ['hello', 'Java', 'Python']
print('|'.join(lst))
print(''.join(lst))

"""
将元组中的元素连接
"""
t = ('hello', 'Java', 'Python')
print(''.join(t))

"""
将字符串中的字符连接
"""
print('*'.join('Python'))
```



### 字符串的比较操作

```python
print('apple' > 'app')  # True
print('apple' > 'banana')  # False
print(ord('a'), ord('b'))

print(chr(97), chr(98))

"""
== 与 is 的区别
前者比较的是 value
后者比较的是 id，即内存地址
"""
a = b = 'Python'
c = 'Python'
print(a == b)
print(a == c)
print(a is b)
print(a is c)
print(id(a), id(b), id(c))

######################################
True
False
97 98
a b
True
True
True
True
2127659121264 2127659121264 2127659121264
```



### 字符串的切片操作

字符串是不可变类型，不具备增删改查等操作；切片操作将产生新的字符串

```python
s = 'hello,Python'
s1 = s[:5]  # 由于没有指定起始位置，所以从 0 开始切
s2 = s[6:]  # 由于没有指定结束位置，所以切到字符串的最后一个元素
s3 = '!'
s4 = s1 + s2 + s3
print(s1)
print(s2)
print(s4)

print('------------------')
print(id(s))
print(id(s1))
print(id(s2))
print(id(s3))
print(id(s4))

print('---------------------------------切片[start:end:step]---------------------------------')
print(s[1:5:1])  # 从 1 开始截到 5（不包含5），步长为 1
print(s[::2])  # 默认从 0 开始，没有写结束，默认到字符串的最后一个元素，步长为 2，两个元素之间的索引间隔为 2
print(s[::-1])  # 默认从字符串的最后一个元素开始，到字符串的第一个元素结束，因为步长为负数
print(s[-6::1])  # 从索引为 -6 开始，到字符串的最后一个元素结束，步长为 1

###########################################
hello
Python
helloPython!
------------------
2157197149744
2157197149424
2157197170672
2157197149296
2157197169136
---------------------------------切片[start:end:step]---------------------------------
ello
hloPto
nohtyP,olleh
Python
```



### 字符串的格式化

```python
# 格式化字符串

"""
1. % 占位符
"""
name = '张三'
age = 20
print('我叫 %s，今年 %d 岁' % (name, age))

"""
2. {} 占位符
"""
print('我叫 {0}，今年 {1} 岁'.format(name, age))


"""
3. f-string
"""
print(f'我叫 {name}，今年 {age} 岁')


print('%10d' % 99)  # 10 表示的是宽度
print('%f' % 3.1415926)
print('%.3f' % 3.1415926)  # 保留 3 位小数，会四舍五入 .3 表示是小数点后三位

# 同时表示宽度和精度
print('%10.3f' % 3.1415926)  # 一共总宽度为 10，小数点后 3 位

print('hellohello')

print('{0}'.format(3.1415926))

print('{0:.3}'.format(3.1415926))  # .3 表示的是一共是 3 位数

print('{:.3f}'.format(3.1415926))
print('{0:.3f}'.format(3.1415926))  # .3f 表示的是一共是 3 位小数

print('{:10.3f}'.format(3.1415926))  # 同时设置宽度和精度，一共是 10 位，3 位是小数
```



### 字符串的编码与解码

```python
s = '坚持到放弃'
# 编码，将字符串转换为二进制数据 bytes
print(s.encode(encoding='GBK'))  # 在 GBK 这种编码格式中，一个中文占两个字节
print(s.encode(encoding='UTF-8'))  # 在 UTF-8 这种编码格式中，一个中文占三个字节

# 解码，将 bytes 类型的数据转换成字符串类型
# byte 代表就是一个二进制数据（字节类型的数据）
byte = s.encode(encoding='GBK')  # 编码
print(byte.decode(encoding='GBK'))  # 解码

byte = s.encode(encoding='UTF-8')
print(byte.decode(encoding='UTF-8'))
```





## 函数

### 函数的定义与调用

```python
"""
函数的创建
"""
def calc(a, b):
    c = a + b
    return c

"""
函数的调用 - 位置参数
"""
result = calc(10, 20)
print(result)

"""
函数的调用 - 关键字实参
"""
res = calc(b=10, a=20)
print(res)
```



### 函数的参数传递

```python
def fun(arg1, arg2):
    print('arg1', arg1)
    print('arg2', arg2)
    arg1 = 100
    arg2.append(10)
    print('arg1', arg1)
    print('arg2', arg2)
    # return


n1 = 11
n2 = [22, 33, 44]
print('n1', n1)
print('n2', n2)
fun(n1, n2)
print('n1', n1)
print('n2', n2)

"""
在函数调用过程中，进行参数的传递

如果是不可变对象，在函数体的修改不会影响实参的值 arg1 修改为 100，不会影响到 n1 的值
如果是可变对象，在函数体的修改会影响到实参的值 arg2 的修改，append(10) 会影响到 n2 的值
"""
```





### 函数的返回值

```python
def fun(num):
    odd = []  # 存奇数
    even = []  # 存偶数
    for i in num:
        if i % 2:
            odd.append(i)
        else:
            even.append(i)
    return odd, even


lst = [10, 29, 34, 23, 44, 53, 55]
print(fun(lst))

"""
函数的返回值
1.如果函数没有返回值【函数执行完毕之后，不需要给调用处提供数据】return 可以省略不写
2.函数的返回值，如果是 1 个，直接返回类型
3.函数的返回值，如果是多个，返回的结果为元组
"""


def fun1():
    print('hello')
    # return


fun1()


def fun2():
    return 'hello'


res = fun2()
print(res)


def fun3():
    return 'hello', 'world'


print(fun3())

"""
函数在定义时，是否需要返回值，视情况而定
"""
```





### 函数的参数定义



```python
"""
默认值参数
"""

def fun(a, b=10):  # b 为默认参数
    print(a, b)


# 函数的调用
fun(100)
fun(20, 30)

print('hello', end='\t')
print('world')


"""
个数可变的位置参数，结果为一个元组
"""
def fun(*args):
    print(args)
    print(args[0])


fun(10)
fun(10, 20, 30)

"""
个数可变的关键字形参，结果为一个字典
"""
def fun2(**args):
    print(args)


fun2(a=10)
fun2(a=10, b=20, c=30)


"""
def fun3(*args, *a):
    pass
    以上参数，程序会报错，个数可变的位置参数，只能是 1 个
    
def fun4(**args1, **args2):
    pass
    以上代码，程序会报错，个数可变的关键字参数，只能是 1 个
"""

def fun5(*args1, **args2):
    pass

"""
def fun6(**args1, *arg2):
    pass
    在一个函数的定义过程中，既有个数可变的关键字形参，也有个数可变的位置形参
    要求个数可变的位置形参放在个数可变的关键字形参之前
"""
```





### 函数的参数总结



```python
def fun(a, b, c):  # a, b, c 在函数的定义处，所以是形式参数
    print('a=', a)
    print('b=', b)
    print('c=', c)


# 函数的调用
fun(10, 20, 30)  # 函数调用时的参数传递，称为位置参数
lst = [11, 22, 33]
fun(*lst)  # 在函数调用时，将列表中的每个元素都转换为位置实参传入

print('-------------------------------')
fun(a=100, c=300, b=200)  # 函数的调用，所以是关键字实参

"""
dic = {'a': 111, 'b': 222, 'c': 333}  # TypeError: fun() missing 2 required positional arguments: 'b' and 'c'
fun(dic)
"""
dic = {'a': 111, 'b': 222, 'c': 333}
fun(**dic)  # 函数调用时，将字典中的键值对都转换为关键字实参

def fun(a, b=10):  # b 是在函数的定义处，所以 b 是形参，而且进行了赋值，所以 b 成为默认值形参
    print('a=', a)
    print('b=', b)


def fun2(*args):  # 个数可变的位置形参
    print(args)


def fun3(**args):  # 个数柯柏年的关键字形参
    print(args)


fun2(10, 20, 30, 40)
fun3(a=11, b=22, c=33, d=44, e=55)

"""
需求，c，d 只能采用关键字实参传递
从 * 之后的参数，在函数调用时，只能采用关键字参数传递
"""


def fun4(a, b, *, c, d):  # 从 * 之后的参数，在函数调用时，只能采用关键字参数传递
    print('a=', a)
    print('b=', b)
    print('c=', c)
    print('d=', d)


# fun4(10, 20, 30, 40)  # 位置实参传递  TypeError: fun4() takes 2 positional arguments but 4 were given
fun4(a=10, b=20, c=30, d=40)  # 关键字实参传递
fun4(10, 20, c=30, d=40)  # 前两个参数，采用的是位置实参传递，而 c，d 采用的是关键字实参传递

"""
函数定义时的形参的顺序问题
"""


def fun5(a, b, *, c, d, **args):
    pass


def fun6(*args, **args2):
    pass


def fun7(a, b=10, *args, **args2):
    pass
```





### 变量的作用域

```python
def fun():
    global age  # 函数内部定义的变量，局部变量，局部变量使用 global 生命，这个变量实际上就变成了全局变量
    age = 20
    print(age)


fun()
print(age)
```





### 递归函数

```python
def fac(n):
    if n == 1:
        return 1
    else:
        return n*fac(n-1)


print(fac(6))
```



### 斐波那契数列

```python
def fib(n):
    if n == 1:
        return 1
    elif n == 2:
        return 1
    else:
        return fib(n - 1) + fib(n - 2)


# 斐波那契数列第 6 位上的数字
print(fib(6))

print('----------------------------')
# 输出这个数列的前 6 位上的数字
for i in range(1, 7):
    print(fib(i))
```







## 异常

> try...except... 结构

```python
try:
    a = int(input('please input first integer number: '))
    b = int(input('please input second integer number: '))
    result = a / b
    print('result is:', result)
except ZeroDivisionError:
    print('sorry, can\'t support zero division')
except ValueError:
    print('invalid literal for int()')
except BaseException:
    print('other exception...')
print('finish')
```



> try...except...else 结构

如果 try 块中没有抛出异常，则执行 else，如果 try 中抛出异常，则执行 except

```python
try:
    a = int(input('please input first integer number: '))
    b = int(input('please input second integer number: '))
    result = a / b
    print('result is:', result)
except BaseException as e:
    print('other exception...')
    print(e)
else:
    print('final result is:', result)
print('finish')
```



> try...except...else...finally 结构

finally 块无论是否发生异常都会被执行，能常用来释放 try 块中申请的资源

```python
try:
    a = int(input('please input first integer number: '))
    b = int(input('please input second integer number: '))
    result = a / b
    print('result is:', result)
except BaseException as e:
    print('other exception...')
    print(e)
else:
    print('else result is:', result)
finally:
    print('final result is:', result)
print('finish')
```



> 常见的异常类型



| 序号 | 异常类型          | 描述                           |
| ---- | ----------------- | ------------------------------ |
| 1    | ZeroDivisionError | 除（或取模）零（所有数据类型） |
| 2    | IndexError        | 序列中没有此索引（Index）      |
| 3    | KeyError          | 映射中没有这个键               |
| 4    | NameError         | 未声明/初始化对象（没有属性）  |
| 5    | SyntaxError       | Python 语法错误                |
| 6    | ValueError        | 传入无效的参数                 |

```python
"""
ZeroDivisionError: division by zero
"""
# print(10/0)

"""
IndexError: list index out of range
"""
# lst = [11, 22, 33, 44]
# print(lst[4])

"""
KeyError: 'gender'
"""
# dic = {'name': '张三', 'age': 20}
# print(dic['gender'])

"""
NameError: name 'num' is not defined
"""
# print(num)

"""
SyntaxError: invalid syntax
"""
# int a = 20

"""
ValueError: invalid literal for int() with base 10: 'hello'
"""
# a = int('hello')
```



> traceback 模块的使用

```python
import traceback

try:
    print('-----------------------')
    print(1 / 0)
except:
    traceback.print_exc()
    
```



## 类

### 类的定义

```python
class Student:
    native_place = '大连'  # 直接写在类里的变量，称为类属性

    def __init__(self, name, age):
        self.name = name  # self.name 称为实体属性，进行了一个赋值操作，将局部变量的 name 的值赋给实体属性
        self.age = age

    # 实例方法
    def eat(self):
        print('student is eating...')

    # 静态方法，不需要在括号中写 self
    @staticmethod
    def method():
        print('static method using: @staticmethod')

    @classmethod
    def cm(cls):
        print('class method using: @classmethod')



# 在类之外定义的称为函数，在类之内定义的称为方法
def drink():
    print('drinking...')
```



### 对象的创建

```python
# 创建 Student 类的对象
# 对象的创建又称为类的实例化
stu1 = Student('shengjian', 28)
"""
stu1 为实例对象
"""
print(id(stu1))  # 2074327785232
print(type(stu1))  # <class '__main__.Student'>
print(stu1)  # <__main__.Student object at 0x000001E2F7921F10>  1E2F7921F10 是 2074327785232 的十六进制
print('-----------------')
"""
Student 为类对象
"""
print(id(Student))  # 2126278039136
print(type(Student))  # <class 'type'>
print(Student)  # <class '__main__.Student'>
```



```python
class Student:
    native_place = '大连'  # 直接写在类里的变量，称为类属性

    def __init__(self, name, age):
        self.name = name  # self.name 称为实体属性，进行了一个赋值操作，将局部变量的 name 的值赋给实体属性
        self.age = age

    # 实例方法
    def eat(self):
        print('student is eating...')

    # 静态方法，不需要在括号中写 self
    @staticmethod
    def method():
        print('static method using: @staticmethod')

    @classmethod
    def cm(cls):
        print('class method using: @classmethod')


# 创建 Student 类的对象
stu1 = Student('shengjian', 28)
stu1.eat()  # 对象名.方法名()
print(stu1.name)
print(stu1.age)

print('-----------------------------')
Student.eat(stu1)  # line@24 与 line@29 代码功能相同，都是调用 Student 中的 eat 方法
                   # 类名.方法名(对象名) -> 实际上就是方法定义处的 self
```



### 使用方式

```python
class Student:
    native_place = '大连'  # 直接写在类里的变量，称为类属性

    def __init__(self, name, age):
        self.name = name  # self.name 称为实体属性，进行了一个赋值操作，将局部变量的 name 的值赋给实体属性
        self.age = age

    # 实例方法
    def eat(self):
        print('student is eating...')

    # 静态方法，不需要在括号中写 self
    @staticmethod
    def method():
        print('static method using: @staticmethod')

    @classmethod
    def cm(cls):
        print('class method using: @classmethod')
        
        
# 类属性的使用方式
# print(Student.native_place)
stu1 = Student('张三', 20)
stu2 = Student('李四', 30)
print(stu1.native_place)
print(stu2.native_place)
Student.native_place = '辽宁'
print(stu1.native_place)
print(stu2.native_place)
stu1.native_place = '吉林'
print(stu1.native_place)
print(stu2.native_place)

# 类方法的使用方式
Student.cm()

# 静态方法的使用方式
Student.method()


####################################
大连
大连
辽宁
辽宁
吉林
辽宁
class method using: @classmethod
static method using: @staticmethod
```



### 动态绑定属性和方法

```python
class Student:
    
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def eat(self):
        print(self.name + ' is eating')


stu1 = Student('张三', 20)
stu2 = Student('李四', 30)
print(id(stu1))
print(id(stu2))

print('----------为 stu1 动态绑定性别属性----------')
stu1.gender = '女'
print(stu1.name, stu1.age, stu1.gender)
print(stu2.name, stu2.age)
# print(stu2.name, stu2.age, stu2.gender)

stu1.eat()
stu2.eat()


def show():
    print('定义在类之外的，成为函数')


stu1.show = show
stu1.show()
# stu2.show()
```



### 面向对象的三大特征

#### 封装

```python
class Student:
    def __init__(self, name, age):
        self.name = name
        self.__age = age  # 年龄不希望在类的外部被使用，所以加了两个 __

    def show(self):
        print(self.name, self.__age)


stu = Student('张三', 28)
stu.show()

# 在类的外部使用 name 和 age
print(stu.name)
# print(stu.__age)

print(dir(stu))
print(stu._Student__age)  # 在类的外部可以通过 _Student__age 进行访问
```



#### 继承

语法格式：

```python
class 子类类名(父类1,父类2...):
    pass
```

- 如果一个类没有继承任何类，则默认继承 Object
- Python 支持多继承
- 定义子类时，必须在其构造函数中调用父类的构造函数



```python
class Person(object):  # Person 继承 Object 类
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def info(self):
        print(self.name, self.age)


class Student(Person):
    def __init__(self, name, age, no):
        super().__init__(name, age)
        self.no = no


class Teacher(Person):
    def __init__(self, name, age, year):
        super().__init__(name, age)
        self.year = year


stu = Student('张三', 20, '1001')
teacher = Teacher('李四', 34, 10)

stu.info()
teacher.info()

```



```python
"""
多继承
"""
class A(object):
    pass


class B(object):
    pass


class C(A, B):
    pass
```



####  多态

> 多态就是 "具有多种形态"，它指的是：即便不知道一个变量所引用的对象到底是什么类型，仍然可以通过这个变量调用方法，
>
> 在运行过程中根据变量所引用对象的类型决定调用哪个对象中的方法。

```python
class Animal(object):
    def eat(self):
        print('animal can eat')


class Dog(Animal):
    def eat(self):
        print('dog eat meat')


class Cat(Animal):
    def eat(self):
        print('cat eat fish')


class Person(object):
    def eat(self):
        print('person eat anything')


def fun(animal):
    animal.eat()


fun(Dog())
fun(Cat())
fun(Person())

#############################################
dog eat meat
cat eat fish
person eat anything
```





#### 方法重写

```python
class Person(object):
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def info(self):
        print('name:{0}, age:{1}'.format(self.name, self.age))


class Student(Person):
    def __init__(self, name, age, stu_no):
        super().__init__(name, age)
        self.stu_no = stu_no

    def info(self):
        super().info()
        print('stu_no:{0}'.format(self.stu_no))


class Teacher(Person):
    def __init__(self, name, age, year):
        super().__init__(name, age)
        self.year = year

    def info(self):
        super().info()
        print('year:{0}'.format(self.year))


stu = Student('Tom', 28, '1001')
stu.info()

teacher = Teacher('Jack', 20, 10)
teacher.info()

```



### object 类

```python
class Student(object):
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def __str__(self):
        return 'name is {0}, age is {1}'.format(self.name, self.age)


stu = Student('tom', 28)  # 注意参数的传入
print(dir(stu))
print(stu)  # 默认会调用 __str__() 这样的方法
print(type(stu))

```



### 特殊属性

```python
class A:
    pass


class B:
    pass


class C(A, B):
    def __init__(self, name, age):
        self.name = name
        self.age = age


class D(A):
    pass


# 创建 C 类的对象
x = C('Jack', 20)  # x 是 C 类的一个实例对象
print(x.__dict__)  # 获取实例对象所绑定的所有属性的字典
print(C.__dict__)  # 获取类对象所绑定的所有方法的字典
print(x.__class__)  # <class '__main__.C'> 输出了对象所属的类
print(C.__bases__)  # 获取 C 类的父类(基类)类型的元组
print(C.__base__)  # 获取 C 类的父类(基类)类型(最前面的一个,比如 C(A,B) 则输出 A)
print(C.__mro__)  # 获取类的层次结构
print(A.__subclasses__())  # 获取类的子类，如果是多个子类则获取的是一个列表

#########################################
{'name': 'Jack', 'age': 20}
{'__module__': '__main__', '__init__': <function C.__init__ at 0x00000258E4E8E550>, '__doc__': None}
<class '__main__.C'>
(<class '__main__.A'>, <class '__main__.B'>)
<class '__main__.A'>
(<class '__main__.C'>, <class '__main__.A'>, <class '__main__.B'>, <class 'object'>)
[<class '__main__.C'>, <class '__main__.D'>]
```





### 特殊方法



|          | 名称         | 描述                                                         |
| -------- | ------------ | ------------------------------------------------------------ |
| 特殊属性 | `__dict__`   | 获得类对象或实例对象所绑定的所有属性和方法的字典             |
| 特殊方法 | `__len__()`  | 通过重写` __len__()`方法，让内置函数 len() 的参数可以是自定义类型 |
|          | `__add__()`  | 通过从写 `__add__()` 方法，可使用自定义对象具有 "+" 功能     |
|          | `__new__()`  | 用于创建对象                                                 |
|          | `__init__()` | 对创建的对象进行初始化                                       |



```python
"""
__add__
"""
a = 20
b = 100
c = a + b  # 两个整数类型的对象相加操作
d = a.__add__(b)
print(c)
print(d)


class Student:
    def __init__(self, name):
        self.name = name

    def __add__(self, other):
        return self.name + other.name

    def __len__(self):
        return len(self.name)


stu1 = Student('zhangsan')
stu2 = Student('lisi')

s = stu1 + stu2  # 需要重写 __add__ 方法来支持相加操作
print(s)


s1 = stu1.__add__(stu2)
print(s1)

"""
__len__
"""
lst = [11, 22, 33, 44]
print(len(lst))  # len 是内置函数
print(lst.__len__())
print(len(stu1))


"""
1.Person('zhangsan', 20) -> __new__ -> __init__
"""
class Person(object):
    def __new__(cls, *args, **kwargs):
        print('__new__ is executed, the id of cls is {0}'.format(id(cls)))  # 2962685190224
        obj = super().__new__(cls)
        print('the id of create object is {0}'.format(id(obj)))  # 2962688978704
        return obj

    def __init__(self, name, age):
        print('__init__ is executed, the id of self is {0}'.format(id(self)))  # 2962688978704
        self.name = name
        self.age = age


print('the id of object class is {0}'.format(id(object)))  # 140717536919040
print('the id of Person class is {0}'.format(id(Person)))  # 2962685190224

# 创建 Person 类的实例对象
p1 = Person('zhangsan', 20)
print('the id of p1 instance is {0}'.format(id(p1)))  # 2962688978704
```

