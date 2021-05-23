- [Python的变量与常量](#python的变量与常量)
  - [变量](#变量)
    - [变量的概念](#变量的概念)
    - [变量的命名规则](#变量的命名规则)
    - [变量的命名规范](#变量的命名规范)
    - [变量的命名法](#变量的命名法)
    - [变量的相关示例](#变量的相关示例)
  - [常量](#常量)
    - [常量的概念](#常量的概念)
    - [常量的命名规范](#常量的命名规范)
    - [常量的命名法](#常量的命名法)
  - [Python中的关键字](#python中的关键字)
  - [相关概念](#相关概念)
    - [del语句](#del语句)

# Python的变量与常量

## 变量

### 变量的概念

```
变量来源于数学，是计算机语言中能储存计算结果或能表示值的抽象概念。
变量可以通过变量名访问。在指令式语言中，变量通常是可变的；但在纯函数式语言（如Haskell）中，变量可能是不可变的。
```

### 变量的命名规则

```
变量名由字母、数字、下划线（_）组成。
变量名首字符不能为数字。
变量名不能为Python关键字。
```

### 变量的命名规范

```
变量名应见名知意。
变量名不应使用中文或拼音。
变量名不应过长。
变量名应使用下划线、小驼峰、大驼峰命名法。
```

### 变量的命名法

```
下划线：
age_of_qiqi = 25
小驼峰：
ageOfQiqi = 25
大驼峰：
AgeOfQiqi = 25
```

### 变量的相关示例

* 示例1，变量的定义

  * var_name = value

    ```python
    name = "qiqi"
    age = 25
    print(name, age)
    ```

    ```
    qiqi 25
    
    ```

* 示例2，获取变量的内存地址

  * id(var_name)

    ```python
    name = "qiqi"
    print(id(name))
    ```

    ```
    140043017212016
    
    ```

    

* 示例3，删除变量对象的引用

  * del var_name

    ```python
    name = "qiqi"
    del name
    print(id(name))
    ```

    ```
    Traceback (most recent call last):
      File "/home/qiqi/Python-tutorials/var_name.py", line 3, in <module>
        print(id(name))
    NameError: name 'name' is not defined
    
    ```

## 常量

### 常量的概念

```
常量”的广义概念是：‘不变化的量’（例如：在计算机程序运行时，不会被程序修改的量。）常量可区分为不同的类型，如：25、0为整型常量，6.8为实型常量，‘a’、‘b’为字符常量。常量一般从其字面形式即可判断。这种常量称为字面常量或直接常量。
```

### 常量的命名规范

```
Python中没有专门的关键字或者语法表示常量，常量命名应字母全大写，单词之间以下划线分割。
```

### 常量的命名法

```
字母全大写，单词之间下划线分割：
AGE_OF_QIQI = 18
```

## Python中的关键字

* 示例1

  ```python
  import keyword
  
  print(keyword.kwlist)
  ```

  ```
  ['False', 'None', 'True', 'and', 'as', 'assert', 'async', 'await', 'break', 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise', 'return', 'try', 'while', 'with', 'yield']
  
  ```

## 相关概念

### del语句

```
del是删除引用而不是删除对象，对象由自动垃圾回收机制（GC）删除。del语句操作某个对象的时候, 并不是直接将该对象在内存中删除, 而是将该对象的引用计数-1。Python中的垃圾回收算法是采用引用计数, 当一个对象的引用计数为0时, Python的垃圾回收机制就会将对象回收。
```

