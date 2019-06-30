1. python是解释性语言
    - 编译性语言和解释性语言的区别: 前者经过专门的编译程序进行编译,转换成机器语言 ,后者直接翻译
2. 输入输出:
    - (1). 输入: `input()`函数
    ```python
    //命令行不会有任何提示,等待从键盘输入任意字符,回车结束. 输入的字符保存到变量variable中
    variable = input(); 

    //命令行将提示字符Enter any chararters, 然后等待输入,将结果保存到变量variable中.
    variable = input('Enter any chararters');   
    ```
    - (2). 输出: `print()`函数
        + a. 括号内的内容为字符串时则原样输出
        ```python
        print('string'); //此处输出string
        ```
        + b. 括号内容为变量时输出变量内容, 为表达式时输出表达式计算结果
        ```python
        print(variable); //输出variable的值
        print(variable*3 + 2); //输出计算结果
        ```
        + c. 括号内容用逗号`,`分割时, 输出把`,`变为空格
3. python代码逻辑使用缩进嵌套
4. python基本数据类型:`整数`, `浮点数`, `字符串`, `布尔值`
    -  内存模型: 例如门牌号和房间的区别, 当新建一个一个变量例如variable, 即会创建一个名为variable的门牌号, 当variable被赋值时, 解释器才会在内存当中开辟一个房间,这个房间内容为你的变量具体值. 
    >Note: 

    这里我们需要明白, 如果代码
    ```python
    variable_1 = 'string'
    variable_2 = variable_1
    variable_1 = 'string has been changed'
    ```
    那么内存开辟了两个房间,分别存放`string`,  `string has been changed`, variable_2这个门牌号依然挂在前者房间之前.

5. python运算符和优先级
6. python自带的数据结构
    - (1). `list` 一个列表, 可以存放任意数据类型的变量常量. 但最终存储的结果是不受其他变量影响的.
    ```例如
    variable_1 = 'string'
    list_test = [variable_1, 1000, 'this is a string']  //则此处的list_test内容为['string', 1000, 'this is a string']
    variable_1 = False  //将其赋值为布尔值False, 那么原列表list不变
    ``` 
        + 通过索引访问列表 `list_test[0] = False`, 注意索引范围(可通过负数索引倒序访问)
        + 列表常用方法
