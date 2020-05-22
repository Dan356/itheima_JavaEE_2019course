# Day01 【前言、入门程序、常量、变量】

## 今日内容

- Java语言的发展历史
- Java开发环境搭建 
- 编写HelloWorld程序 
- 常量和变量 

## 教学目标

- [ ] 能够计算二进制和十进制数之间的互转 
- [ ] 能够使用常见的DOS命令 
- [ ] 理解Java语言的跨平台实现原理 
- [ ] 理解JDK和JRE的组成和作用 
- [ ] 能够配置环境变量JAVA_HOME 
- [ ] 能够编写HelloWorld程序编译并执行 
- [ ] 理解关键字的含义 理解标识符的含义 
- [ ] 能够定义出所有类型的常量 
- [ ] 理解Java中的基本数据类型分类 
- [ ] 能够定义8种基本数据集类型的变量

## 第一章 开发前言

### 1.1 Java语言概述

#### 1.1.1 什么是Java语言

Java语言是美国Sun公司（Stanford University Network），在1995年推出的高级的编程语言。所谓编程语言，是 计算机的语言，人们可以使用编程语言对计算机下达命令，让计算机完成人们需要的功能。 

#### 1.1.2 Java语言发展历史

- 1995年Sun公司发布Java1.0版本 
- 1997年发布Java 1.1版本 
- 1998年发布Java 1.2版本 
- 2000年发布Java 1.3版本 
- 2002年发布Java 1.4版本 
- 2004年发布Java 1.5版本 
- 2006年发布Java 1.6版本
- 2009年Oracle甲骨文公司收购Sun公司，并于2011发布Java 1.7版本 
- 2014年发布Java 1.8版本 
- 2017年发布Java 9.0版本

#### 1.1.3 Java语言能做什么

Java语言主要应用在互联网程序的开发领域。常见的互联网程序比如天猫、京东、物流系统、网银系统等，以及服 务器后台处理大数据的存储、查询、数据挖掘等也有很多应用。



### 1.2 计算机基础知识

#### 1.2.1 二进制

计算机中的数据不同于人们生活中的数据，人们生活采用十进制数，而计算机中全部采用二进制数表示，它只包含 0、1两个数，逢二进一，1+1=10。每一个0或者每一个1，叫做一个bit（比特）。

下面了解一下十进制和二进制数据之间的转换计算。

- 十进制数据转成二进制数据：使用除以2获取余数的方式

  ![image-20200521093549446](https://picgo-dan356.oss-cn-shanghai.aliyuncs.com/img/20200521093551.png)



- 二进制数据转成十进制数据：使用8421编码的方式

  ![image-20200521093630680](https://picgo-dan356.oss-cn-shanghai.aliyuncs.com/img/20200521093942.png)

> 小贴士：
>
> 二进制数系统中，每个0或1就是一个位，叫做bit（比特）。 

#### 1.2.2 字节

字节是我们常见的计算机中小存储单元。计算机存储任何的数据，都是以字节的形式存储，右键点击文件属性， 我们可以查看文件的字节大小。

8个bit（二进制位） 0000-0000表示为1个字节，写成1 byte或者1 B。

- 8 bit = 1 B 
- 1024 B = 1 KB 
- 1024 KB = 1 MB 
- 1024 MB = 1 GB 
- 1024 GB = 1 TB

#### 1.2.3 常用DOS命令

Java语言的初学者，学习一些DOS命令，会非常有帮助。DOS是一个早期的操作系统，现在已经被Windows系统取 代，对于我们开发人员，目前需要在DOS中完成一些事情，因此就需要掌握一些必要的命令。

- 进入DOS操作窗口

  - 按下Windows+R键盘，打开运行窗口，输入cmd回车，进入到DOS的操作窗口。

    ![image-20200521094304010](https://picgo-dan356.oss-cn-shanghai.aliyuncs.com/img/20200521094305.png)

  - 打开DOS命令行后，看到一个路径 c:\user 就表示我们现在操作的磁盘是c盘。

    ![image-20200521094340989](https://picgo-dan356.oss-cn-shanghai.aliyuncs.com/img/20200521094343.png)

- 常用命令

  | 命令             | 操作符号      |
  | ---------------- | ------------- |
  | 盘符切换命令     | `盘符名:`     |
  | 查看当前文件夹   | `dir`         |
  | 进入文件夹命令   | `cd 文件夹名` |
  | 退出文件夹命令   | `cd..`        |
  | 退出到磁盘根目录 | `cd\`         |
  | 清屏             | `cls`         |



## 第二章 Java语言开发环境搭建

### 2.1 Java虚拟机——JVM

- JVM（Java Virtual Machine ）：Java虚拟机，简称JVM，是运行所有Java程序的假想计算机，是Java程序的运行环境，是Java 具吸引力的特性之一。我们编写的Java代码，都运行在 JVM 之上。 
- 跨平台：任何软件的运行，都必须要运行在操作系统之上，而我们用Java编写的软件可以运行在任何的操作系 统上，这个特性称为Java语言的跨平台特性。该特性是由JVM实现的，我们编写的程序运行在JVM上，而JVM 运行在操作系统上。

![image-20200521100124277](https://picgo-dan356.oss-cn-shanghai.aliyuncs.com/img/20200521100126.png)

如图所示，Java的虚拟机本身不具备跨平台功能的，每个操作系统下都有不同版本的虚拟机。



### 2.2 JRE和JDK

- JRE  (Java Runtime Environment) ：是Java程序的运行时环境，包含 JVM 和运行时所需要的核心类库 。
  - 我们想要运行一个已有的Java程序，那么只需安装 JRE 即可。 
- JDK  (Java Development Kit)：是Java程序开发工具包，包含 JRE 和开发人员使用的工具。
  - 我们想要开发一个全新的Java程序，那么必须安装 JDK 。

![image-20200521100423078](https://picgo-dan356.oss-cn-shanghai.aliyuncs.com/img/20200521100425.png)



### 2.3 JDK9安装图解

![image-20200521100727010](https://picgo-dan356.oss-cn-shanghai.aliyuncs.com/img/20200521100728.png)

![image-20200521100800503](https://picgo-dan356.oss-cn-shanghai.aliyuncs.com/img/20200521100802.png)

![image-20200521101009256](https://picgo-dan356.oss-cn-shanghai.aliyuncs.com/img/20200521101010.png)

> 小贴士：
>
> 安装路径中，不要包含中文和空格。



### 2.4 JAVA_HOME环境变量配置

#### 2.4.1 环境变量配置作用

为了开发方便，我们想在任意的目录下都可以使用JDK的开发工具，则必须要配置环境变量，配置环境变量的意义 在于告诉操作系统，我们使用的JDK开发工具在哪个目录下。 

#### 2.4.2 环境变量配置步骤

- 桌面上，鼠标右键`此电脑`，打开`属性`

  ![image-20200521101625453](https://picgo-dan356.oss-cn-shanghai.aliyuncs.com/img/20200521101626.png)

- 打开`高级系统设置`，选择`环境变量`

  ![image-20200521101852122](https://picgo-dan356.oss-cn-shanghai.aliyuncs.com/img/20200521101853.png)

- 点击下方系统变量的新建 ，创建新的环境变量，变量名输入 `JAVA_HOME` ，变量值输入JDK9的安装目录

![image-20200521102407525](https://picgo-dan356.oss-cn-shanghai.aliyuncs.com/img/20200521102408.png)

- 在列表里找到`path`，点击`编辑`，选择`新建`，新建一行`%JAVA_HOME%\bin`

  ![image-20200521102828251](https://picgo-dan356.oss-cn-shanghai.aliyuncs.com/img/20200521102829.png)

- 环境变量配置完成，重新开启`DOS命令行`，在任意目录下输入 `javac  -version`命令。

  ![image-20200521103005461](https://picgo-dan356.oss-cn-shanghai.aliyuncs.com/img/20200521103015.png)

>小贴士：
>
>我在学习的过程中，已经是Java11了，所以安装的是Java11的版本，步骤都一样





## 第三章 Hello World入门程序

### 3.1 程序开发步骤说明

开发环境已经搭建完毕，可以开发我们第一个Java程序了。
Java程序开发三步骤：编写、编译、运行。

![image-20200521111450736](https://picgo-dan356.oss-cn-shanghai.aliyuncs.com/img/20200521111452.png)



### 3.2 编写Java源程序

1. 在 `d:\day01`目录下新建文本文件，完整的文件名修改为`HelloWorld.java` ，其中文件名为 `HelloWorld` ，后缀名必须为 `.java` 。 

2. 用记事本打开`HelloWorld.java`文件

3. 在文件中键入文本并保存，代码如下：

   ```java
   public class HelloWorld {    
   public static void main(String[] args){
   	        System.out.println("Hello World!");         
   	}    
   } 
   ```

   > 小贴士：
   >
   > 文件名必须是 `HelloWorld` ，保证文件名和类的名字是一致的，注意大小写。
   > 每个字母和符号必须与示例代码一模一样。
   
   第一个HelloWord`源程序`就编写完成了，但是这个文件是程序员编写的，JVM是看不懂的，也就不能运行，因此我们必须将编写好的 `Java源文件`编译成JVM可以看懂的`字节码文件` 。



### 3.3 编译Java源文件

在DOS命令行中，进入Java源文件的目录，使用 `javac`命令进行编译

命令：

```
javac Java源文件名.后缀名
```

举例：

```
javac HelloWorld.java
```

![image-20200521113929498](https://picgo-dan356.oss-cn-shanghai.aliyuncs.com/img/20200521113930.png)

编译成功后，命令行没有任何提示。打开`d:\day01`目录，发现产生了一个新的文件`HelloWorld.class `，该文件 就是编译后的文件，是Java的可运行文件，称为`字节码文件`，有了字节码文件，就可以运行程序了。 



### 3.4 运行Java程序

在DOS命令行中，进入Java源文件的目录，使用`java`命令进行运行。

命令：

```
java 类名字 
```

举例：

```
java HelloWorld
```

![image-20200521113751896](https://picgo-dan356.oss-cn-shanghai.aliyuncs.com/img/20200521113941.png)



### 3.5 入门程序说明



#### 3.5.1 编译和运行是两回事

- 编译：是指将我们编写的`Java源文件`翻译成JVM认识的`.class文件`，在这个过程中， javac 编译器会检查我们所写的程序是否有错误，有错误就会提示出来，如果没有错误就会编译成功。 
- 运行：是指将`.class文件`交给JVM去运行，此时JVM就会去执行我们编写的程序了。

#### 3.5.2 关于main方法

main方法：称为主方法。写法是`固定格式不可以更改`。main方法是程序的入口点或起始点，无论我们编写多 少程序，JVM在运行的时候，都会从main方法这里开始执行。



### 3.6 添加注释comment

- 注释：就是对代码的解释和说明。其目的是让人们能够更加轻松地了解代码。为代码添加注释，是十分必须 要的，它不影响程序的编译和运行。 
- Java中常用的注释有单行注释和多行注释
  - 单行注释以 `//`开头换行结束
  - 多行注释以 `/`开头 ，以`/`结束 



### 3.7 关键字keywords

关键字：是指在程序中，Java已经定义好的单词，具有特殊含义。 

- HelloWorld案例中，出现的关键字有`public`、`class`、`static`、`void`等，这些单词已经被 Java定义好，全部都是小写字母。
- 关键字比较多，不能死记硬背，学到哪里记到哪里即可。



### 3.8 标识符

标识符：是指在程序中，我们自己定义内容。比如类的名字、方法的名字和变量的名字等等，都是标识符。

- 命名规则：`硬性要求`
  - 标识符可以包含 英文字母26个(区分大小写) 、 0-9数字 、 $（美元符号） 和 _（下划线） 。 
  - 标识符不能以数字开头。 
  - 标识符不能是关键字。 
- 命名规范：`软性建议` 
  - 类名规范：首字母大写，后面每个单词首字母大写（大驼峰式）。 
  - 方法名规范： 首字母小写，后面每个单词首字母大写（小驼峰式）。 
  - 变量名规范：全部小写



## 第四章 常量

### 4.1 概述

常量：是指在Java程序中固定不变的数据。



### 4.2 分类

| 类型       | 含义                                     | 数据举例                 |
| ---------- | ---------------------------------------- | ------------------------ |
| 整数常量   | 所有的整数                               | 0，1，567，-9            |
| 小数常量   | 所有的小数                               | 0.0，-0.1，2.55          |
| 字符常量   | 单引号引起来，只能写一个字符，必须有内容 | 'a'，' '，'好'           |
| 字符串常量 | 双引号引起来，可以写多个字符，也可以不写 | "A"，"Hello"，"你好"，"" |
| 布尔常量   | 只有两个值（流程控制中讲解）             | true，false              |
| 空常量     | 只有一个值（引用数据类型中讲解）         | null                     |



### 4.3 练习

需求：输出各种类型的常量

```java
public class Demo01Constant {
    public static void main(String[] args) {
        //字符串常量
        System.out.println("ABC");
        System.out.println("");     //字符串两个双引号中间的内容为空
        System.out.println("XYZ");

        //整数常量
        System.out.println(30);
        System.out.println(-500);

        //浮点数常量
        System.out.println(3.14);
        System.out.println(-2.5);

        //字符常量
        System.out.println('A');
        System.out.println('6');
        //System.out.println('');       //两个单引号中间必须有且仅有一个字符，没有不行
        //System.out.println('AB');     //两个单引号中间必须有且仅有一个字符，有两个不行

        //布尔常量
        System.out.println(true);
        System.out.println(false);

        //空常量，空常量不能直接用来打印输出
        //System.out.println(null);
    }
}
```



## 第五章 变量和数据类型

### 5.1 数据类型

#### 5.1.1 数据类型分类

Java的数据类型分为两大类： 

- 基本数据类型：包括整数 、 浮点数 、 字符 、 布尔 。 
- 引用数据类型：包括类 、 数组 、 接口 。 

#### 5.1.2 基本数据类型

四类八种基本数据类型：

|   数据类型   |     关键字     | 内存占用 |              取值范围              |
| :----------: | :------------: | :------: | :--------------------------------: |
|    字节型    |      byte      | 1个字节  |             -128 ~ 127             |
|    短整型    |     short      | 2个字节  |           -32768 ~ 32767           |
|     整型     |  int（默认）   | 4个字节  | -2<sup>31</sup> ~ 2<sup>31</sup>-1 |
|    长整型    |      long      | 8个字节  | -2<sup>63</sup> ~ 2<sup>63</sup>-1 |
| 单精度浮点数 |     float      | 4个字节  |      1.4013E-45 ~ 3.4028E+38       |
| 双精度浮点数 | double（默认） | 8个字节  |       4.9E-324 ~ 1.7977E+308       |
|    字符型    |      char      | 2个字节  |             0 ~ 65535              |
|   布尔类型   |    boolean     | 1个字节  |             true,false             |

>小贴士：
>
>- 字符串不是基本类型，而是引用类型
>- 浮点型可能只是一个近似值，并非确定的值。
>- 数据范围与字节数不一定相关，例如float数据范围比long更加广泛，但是float是4个字节，而long是8个字节。
>- 浮点数当中默认类型是`double`，如果一定要使用`float`，则需要加上后缀`F`。
>- 整数当中默认类型是`int`，如果一定要使用`long`类型，则需要加上后缀`L`。



### 5.2 变量

#### 5.2.1 变量的概述

变量：常量是固定不变的数据，那么在程序中可以变化的量称为变量。

> 数学中，可以使用字母代替数字运算,例如 x=1+5 或者 6=x+5。
> 程序中，可以使用字母保存数字的方式进行运算，提高计算能力，可以解决更多的问题。比如x保存5，x也可 以保存6，这样x保存的数据是可以改变的，也就是我们所讲解的变量。

Java中要求一个变量每次只能保存一个数据，必须要明确保存的数据类型。



#### 5.2.2 变量的定义

变量定义的格式包括三个要素：`数据类型`、`变量名`、`数据值`。 

格式：

```java
数据类型 变量名 = 数据值;
```

练习： 定义所有基本数据类型的变量

```java
public class Demo02Variable {
    public static void main(String[] args) {
        //创建一个变量
        //格式：数据类型 变量名称；
        int num1;
        //向变量当中存入一个数据
        //格式：变量名称 = 数据值
        num1 = 10;
        System.out.println(num1);   //10

        //改变变量当中本来的数字，变成新的数字
        num1 = 20;
        System.out.println(num1);   //20

        //使用一步到位的格式来定义变量
        //格式：数据类型 变量名称 = 数据值;
        int num2 = 25;
        System.out.println(num2);   //25

        num2 = 35;
        System.out.println(num2);   //35

        System.out.println("===================");

        byte num3 = 30;     //注意：右侧数值的范围不能超过左侧数据类型的取值范围
        System.out.println(num3);   //30
        //byte num4 = 400;    //右侧数值超出了byte数据的范围，错误！

        System.out.println("===================");

        short num5 = 50;
        System.out.println(num5);   //50

        System.out.println("===================");

        long num6 = 30000000000L;
        System.out.println(num6);   //3000000000

        System.out.println("===================");

        float num7 = 2.5F;
        System.out.println(num7);   //2.5

        System.out.println("===================");

        double num8 = 1.2;
        System.out.println(num8);   //1.2

        System.out.println("===================");

        char zifu1 = 'A';
        System.out.println(zifu1);  //A
        zifu1 = '中';
        System.out.println(zifu1);  //中

        System.out.println("===================");

        boolean var1 = true;
        System.out.println(var1);   //true
        var1 = false;
        System.out.println(var1);   //false

        //将一个变量的数据内容，赋值交给另一个变量
        //右侧的变量名称var1已经存在，里面装的是false布尔值
        //将右侧变量里面的false值，向左交给var2变量进行存储
        boolean var2 = var1;
        System.out.println(var2);   //false

    }
}
```



#### 5.2.3 注意事项

- 如果创建多个变量，那么变量之间的名称不可以重复，在同一个大括号范围内，变量的名字不可以相同。 

- 对于float和long类型来说，字母后缀F和L不要丢掉。
- 如果使用byte或者short类型的变量，那么右侧的数据值不能超过左侧类型的数据范围。
- 没有进行赋值的变量，不能直接使用
- 可以通过一个语句来创建多个变量，但是一般情况下不推荐这么写

练习：

```java
public class Demo03VariableNotice {
    public static void main(String[] args) {
        int num1 = 10;  //创建了一个新的变量，名叫num1
        //int num1 = 20;  //有创建了另一个新的变量，名字也叫num1,错误！

        int num2;   //定义了一个变量，但是没有进行赋值
        //System.out.println(num2);   //直接使用打印输出就是错误的

        //System.out.println(num3);   //在创造变量之前，不能使用这个变量
        int num3 = 500;
        System.out.println(num3);   //500

        {
            int num4 = 60;
            System.out.println(num4);   //60
        }
        //System.out.println(num4);   //已经超出了大括号的范围，超出了作用域，变量不能再使用了

        //同时创建了三个全部都是int类型的变量
        int a,b,c;
        a = 10;
        b = 20;
        c = 30;
        System.out.println(a);  //10
        System.out.println(b);  //20
        System.out.println(c);  //30

        //同时创建三个int变量，并且同时各自赋值
        int x = 100, y = 200, z = 300;
        System.out.println(x);  //100
        System.out.println(y);  //200
        System.out.println(z);  //300

    }
}
```

