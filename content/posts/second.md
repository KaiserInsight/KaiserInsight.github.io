---
title: "Python 基础教程"
date: 2026-07-16T08:00:00+08:00
summary: "Python 基本语法。"
cover: "image/Still_002_001.png"
---



## 1. Hello World

```python
print("Hello, World!")
```

输出：

```
Hello, World!
```

---

# 2. 注释

## 单行注释

```python
# 这是一个注释
print("Python")
```

## 多行注释

```python
"""
这是多行注释
可以写多行内容
"""
```

---

# 3. 变量与数据类型

Python 不需要声明变量类型。

```python
name = "Tom"
age = 18
height = 1.75
is_student = True
```

常见数据类型：

| 类型 | 示例 |
|---|---|
| 字符串 str | `"hello"` |
| 整数 int | `123` |
| 浮点数 float | `3.14` |
| 布尔 bool | `True` |
| 列表 list | `[1,2,3]` |
| 元组 tuple | `(1,2,3)` |
| 字典 dict | `{"a":1}` |
| 集合 set | `{1,2,3}` |

查看类型：

```python
x = 10
print(type(x))
```

---

# 4. 输入输出

## 输出

```python
print("你好")
```

多个变量：

```python
name = "Tom"
age = 20

print(name, age)
```

格式化输出：

```python
name = "Tom"
age = 20

print(f"{name}今年{age}岁")
```

## 输入

```python
name = input("请输入名字:")
print(name)
```

输入数字：

```python
age = int(input("年龄:"))
```

---

# 5. 运算符

## 算术运算

```python
a = 10
b = 3

print(a+b)
print(a-b)
print(a*b)
print(a/b)
print(a//b)   # 整除
print(a%b)    # 取余
print(a**b)   # 幂
```

---

## 比较运算

```python
a > b
a < b
a == b
a != b
a >= b
a <= b
```

---

## 逻辑运算

```python
and
or
not
```

例：

```python
age = 20

if age > 18 and age < 60:
    print("成年人")
```

---

# 6. 条件判断

## if

```python
age = 18

if age >= 18:
    print("成年")
```

## if else

```python
age = 15

if age >= 18:
    print("成年")
else:
    print("未成年")
```

## if elif else

```python
score = 90

if score >= 90:
    print("优秀")
elif score >= 60:
    print("及格")
else:
    print("不及格")
```

---

# 7. 循环

## while循环

```python
i = 0

while i < 5:
    print(i)
    i += 1
```

---

## for循环

```python
for i in range(5):
    print(i)
```

输出：

```
0
1
2
3
4
```

遍历列表：

```python
names = ["Tom","Bob","Jack"]

for name in names:
    print(name)
```

---

# 8. range()

```python
range(5)
```

表示：

```
0 1 2 3 4
```

指定范围：

```python
range(1,5)
```

结果：

```
1 2 3 4
```

步长：

```python
range(0,10,2)
```

结果：

```
0 2 4 6 8
```

---

# 9. 字符串

创建：

```python
s = "Python"
```

索引：

```python
print(s[0])
```

输出：

```
P
```

切片：

```python
print(s[0:3])
```

输出：

```
Pyt
```

常用方法：

```python
s.upper()       # 大写
s.lower()       # 小写
s.replace()     # 替换
s.split()       # 分割
len(s)          # 长度
```

---

# 10. 列表 list

创建：

```python
nums = [1,2,3,4]
```

访问：

```python
print(nums[0])
```

添加：

```python
nums.append(5)
```

删除：

```python
nums.remove(3)
```

长度：

```python
len(nums)
```

遍历：

```python
for n in nums:
    print(n)
```

---

# 11. 元组 tuple

不可修改。

```python
t = (1,2,3)
```

访问：

```python
print(t[0])
```

---

# 12. 字典 dict

创建：

```python
person = {
    "name":"Tom",
    "age":20
}
```

读取：

```python
print(person["name"])
```

修改：

```python
person["age"] = 21
```

添加：

```python
person["city"]="LA"
```

遍历：

```python
for key,value in person.items():
    print(key,value)
```

---

# 13. 集合 set

创建：

```python
s = {1,2,3}
```

添加：

```python
s.add(4)
```

删除：

```python
s.remove(2)
```

特点：

- 无序
- 不重复

---

# 14. 函数

定义：

```python
def hello():
    print("Hello")
```

调用：

```python
hello()
```

带参数：

```python
def add(a,b):
    return a+b

print(add(3,5))
```

---

# 15. 默认参数

```python
def hello(name="User"):
    print(name)

hello()
hello("Tom")
```

---

# 16. 匿名函数 lambda

普通：

```python
def add(x,y):
    return x+y
```

lambda：

```python
add = lambda x,y:x+y

print(add(1,2))
```

---

# 17. 类 Class

定义：

```python
class Person:

    def __init__(self,name):
        self.name=name

    def hello(self):
        print(self.name)


p = Person("Tom")

p.hello()
```

---

# 18. 文件操作

打开文件：

```python
file = open("test.txt","r")

data = file.read()

file.close()
```

写文件：

```python
with open("test.txt","w") as f:
    f.write("Hello")
```

---

# 19. 异常处理

```python
try:
    x = 10 / 0

except:
    print("错误")
```

完整：

```python
try:
    num=int(input())
except ValueError:
    print("输入错误")
finally:
    print("结束")
```

---

# 20. 模块导入

导入：

```python
import random
```

使用：

```python
random.randint(1,10)
```

指定导入：

```python
from math import sqrt

print(sqrt(16))
```

---

# 21. 列表推导式

普通：

```python
nums=[]

for i in range(5):
    nums.append(i)
```

简写：

```python
nums=[i for i in range(5)]
```

---

# 22. 常用内置函数

```python
print()
len()
type()
int()
str()
float()
list()
dict()
sum()
max()
min()
sorted()
```

---

# 23. Python缩进规则

Python 使用缩进表示代码块。

正确：

```python
if True:
    print("yes")
```

错误：

```python
if True:
print("yes")
```

推荐：

- 4个空格缩进
- 不混用Tab和空格

---

# 24. 主程序入口

```python
def main():
    print("运行程序")


if __name__ == "__main__":
    main()
```

---

