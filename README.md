# JavaScript学习笔记

## JS变量

当声明一个变量后并未赋值，此时该变量的值为undefined。
变量在重新声明后并不会覆盖之前的值内容。

## JS数据类型

JS的数据类型包括：String, Number, Boolean, Array, Object, Null和Undefined。

Undefined和Null
变量值未赋值时为 **undefined** ，变量可以通过null设置为空值（empty）

## JS数字

通过数字的toString()方法可以将数字转化为16进制，8进制或2进制。
```
var myNumber = 128;
myNumber.toString(16);
myNumber.toString(8);
myNumber.toString(2);
```

数字中的Infinity表示数字溢出，除零时的结果也是Infinity。

## JS操作符

### delete操作符

delete操作符用于删除对象的属性，它对变量和方法不起作用。

```
var person = {
    firstName: "Kevin",
    lastName: "Lee",
    age: 35,
    eyeColor: "black"
};

delete person.age;
console.log("%o", person); // 此处通过%o可以在console中显示person对象内容
```

## JS类型转换

### JavaScript中包含五种数据类型

1. string
2. number
3. boolean
4. object
5. function

### 三种对象类型

1. Object
2. Date
3. Array

### 不能包含值的两种数据类型

1. null
2. undefined

### constructor属性

**constructor** 属性返回所有JavaScript变量的构造函数定义。

## JS错误处理

+ **try** 用来测试语句中是否出现错误
+ **catch** 用来处理错误
+ **throw** 用来创建自定义错误
+ **finally** 在 **try** 和 **catch** 后执行，无论他们处理结果如何，**finally** 语句始终会被执行.

```
try {
    Block of code to try
} catch (err) {
    Block of code to handle errors
} finally {
    Block of code to be executed regardless of the try / catch result
}
```

### 抛出异常的类型包括

1. String
2. Number
3. Boolean
4. Object

## JS正则表达式

在JavaScript中我们主要通过字符串的search()和replace()方法使用正则表达式。

+ **search()** 方法查找匹配的字符序列并返回匹配字符序列的位置。
+ **replace()** 方法在字符串中替换匹配的字符序列。

### 正则表达式Patterns

[Regular Expression Patterns](www.w3schools.com/js/js_regexp.asp)

### 使用正则对象

使用 **test()** 方法

```
var patt = /e/;
patt.test("The best things in life are free!");
```

使用 **exec()** 方法

```
/e/.exec("The best things in life are free!");
```

## JS提升（Hoisting）

**Hoisting** 是JS的默认行为，它将所有声明语句提升当前作用范围（scope）的最前端（当前脚本或当前方法）。

对于JS中的初始化并不会提升，也就是说在提升变量声明的同时并不执行初始化操作。

我们在编写程序时尽量不要采用JS提升特性，因为这种习惯很容易产生bug，尽可能在顶端声明你的变量。