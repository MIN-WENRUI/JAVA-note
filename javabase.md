# Java概述

🚩快速学习方法

java历史

java特点

Sublime

🚩java运行机制

🚩JDK

转义字符

🚩java开发规范

java API

## java開発場面

java開発場面１ーSSM

spring（轻量级的容器框架）

springMVC（分层的Web开发框架）

MyBatis（持久化框架）

java開発場面２ーAndroid核心コード

Java開発場面３ービークデータhadoop

## java応用領域

1、企業層応用

主に複雑的な大手企業のソフトウエアシステム、各種タイプのウェブサイト。応用領域は金融、通信、交通、ネットショッピング、など。

２、Andoridプラットフォーム応用

３、移動領域

組み込みシステム　POS機　自動車インタラクション　

プログラミング：ある操作を実行したり、問題を解決したりするために、コンピュータが書いた命令文の集合体。

## javaの特徴

1、java语言是面向对象的（oop）

２、Java的跨平台性（JVM实现）

一个编译好的.class文件可以在多个平台下运行。

３、Java是解释型语言

编译型：c/c++   解释型：javascript PHP java

区別：解释型需要解释器来执行

4、java语言是强壮的，java的强类型机制、异常处理，垃圾的自动收集等是java程序健壮性的重要保证。

## java的开发工具

ediplus notepad++

sublime Text

IDEA

eclipse

## java的运行机制和运行过程

核心机制 虚拟机 JVM（java virtual machine）

1）jvm是一个虚拟计算机，具有指令集并使用不同的储存区域。负责执行指令，管理数据，内存，寄存器，包含在JDK中。

2）对于不同的平台，有不同的虚拟机。

3）java虚拟机机制屏蔽来底层运行平台的差别，实现了“一次编译，到处运行”

Test.java----编译-----Test.class

### JDK JRE

Java Development Kit 

JDK=JRE+java开发工具

JRE=JVM+JAVA核心类库

JDK=JVM+JAVA SE标准类库+开发工具集

运行开发好的.class文件只需要JRE

## sublime入门

什么是编译

javac Hello.java

1.有了java源文件，通过编译器将其编译成JVM可以识别的字节码文件。

2.在该源文件目录下，通过javac编译工具对Hello.java文件进行编译。

3.如果程序没有错误，没有提示，但在当前目录下会出现一个Hello.class文件，该文件称为字节码关注文件，也可以执行的java的程序。

什么是运行

1，有了可执行的java程序（Hello.class字节码文件）

2，通过运行工具java.exe对字节码文件进行执行，本质就是.class装载到jvm机进行执行。

开发的注意事项

是修改后的Hello.java源文件需要重新编译，生成新的。class文件后，再执行才能生效。

```java
//这是java的快速入门，演示java的开发步骤
//对代码的相关说明
//1.public class Hello 表示Hello是一个类，是一个public公有的类
//2.Hello{}表示一个类的开始和结束
//3.public static void main（String[] args）表示一个主方法，即我们程序的入口
//4.main(){}表示方法的开始和结束
//5.System.out.println("hello,world~");表示输出“hello，world～”到屏幕
//6.;表示语句结束

public class Hello{

	

	//编写一个main方法
	public static void main(String[] args){
		System.out.println("bill is studying java~");
	}
}
```



## java开发的注意事项和细节说明

1，java源文件.java为拓展名。源文件的基本组成部分是类（class），如本类中的Hello类。

2.java应用程序的执行入口是main（）方法。他有固定的书写格式：

`Public static void main(String[] args){...}`

3.java语言严格区分大小写。

4，java方法由一条条语句构成，每个语句以";"结束。

5，大括号都是成对出现，缺一不可。【习惯，先写{}再写代码】

6，一个源文件中最多只能有一个public类。其他的类个数不限。

//编译后每一个类都对应一个.class文件

7，如果源文件包含一个public类，则文件名必须按该类命名！

8，一个源文件中最多只能有一个public类。其他类个数不限，也可以将main方法写在非public类中，然后指定运行非public类，这样入口方法就是非public的mian方法。

## 计算机科学快速高效掌握技术或知识点

需求➡️  看看能否使用传统技术解决➡️引出我们学习的新技术➡️学习基本原理和语法（不考虑细节）➡️快速入门（基本程序，crud）➡️开始研究技术的注意事项，使用细节，使用规范，如何优化=》没有止境，技术魅力。

## java的转义字符

常用的6个转义字符

```java
//演示转义字符的使用
public class ChangeChar{
	//编写一个main方法
	public static void main(String[] args){
//      \t  :一个制表位，实现对齐功能
		System.out.println("北京\t天津\t上海");
//      \n :换行符
		System.out.println("jack\nsmith\nmary");
//      \\ :添加一个\
        System.out.println("macbookpro\\MIN\\WENRUI");
//      \": "
        System.out.println("闵少说\"Mac\"");	
//      \':'
        System.out.println("闵少说\'bookpro\'");
//      \r:一个回车
        System.out.println("闵文锐\r\n无敌");
        System.out.println("书名\t作者\t价格\t销量\n三国\t罗贯中\t120\t1000");

	}
}

```

### 易犯错误

1，找不到文件：源文件名不存在或写错，或者当前路径错误。

2，主类名和文件名不一致：声明为public的主类应与文件名一致，否则编译失败。

3，缺少分号：查看错误出现的行数，在源代码中改错。

4，语法错误：编译器中报告的错误信息。

5，业务逻辑错误，环境错误

## 注释（comment)

用文字解释代码，提高代码的可读性。将自己的思想用注释先整理出来，再用代码去实现。

#### java中注释类型

1，单行注释

2，多行注释

 //单行注释
/* 多行注释

>=可读性很好
>不会被解释器（jvm）执行
>多行注释中不允许嵌套*/

3，文档注释 注释内容可以被JDK提供的工具javadoc所解析，生成一套以网页文件形式所体现的该程序的说明文档，一般写在类。

```java
//文档注释
/**@author minwenrui
 * @version 1.0

*/


public class Comment01{
	public static void main(String[] args){

	}
}
```

## java代码规范

1，类，方法的注释，要以Javadoc的方式来写

2，非javaDoc的注释，往往是给代码的维护者看的，着重告诉读者写法思路，如何修改，注意什么问题。

3，使用tab操作，实现缩进，默认整体向右移动。shift+table整体左移。

4，运算符和“=”两边习惯性的各一加一个空格。eg.2 + 4 = N + M

5，源文件使用utf-8编码

6，行宽不要超过80字符

7，代码编写的**次行风格**和**行尾风格**

## DOS命令

Disk operating System 磁盘操作系统

常用的dos命令

1，查看当前目录dir

2，切换到其他盘下 cd

#   变量

为什么需要变量

## 变量的基本使用

**变量三要素**（类型+名称+值）

变量是程序的基本组成单位，相当于内存中一个数据存储空间的表示。

门牌号➡️房间 变量名➡️变量值

代码和计算机的对应关系

**变量的使用步骤**

```java
public class var01{
	//编写一个main方法
	public static void main(String[] args){

		//声明变量
		int a;
		a = 10 ;
	System.out.println(a);


	//直接赋值
	int a = 60;
	System.out.println(a);
	}
}
```

```java
public class Var02{

	//编写一个main方法
	public static void main(String[] args) {
		 //记录人的信息
		int age = 30;
		double score = 99.8;
		char gender ='女'；
		String name = "minwenrui"
		//输出信息快捷键
		System.out.ptrinln("人的信息如下")；
		System.out.ptrinln("name");
		System.out.ptrinln("age");
		System.out.ptrinln("score");
		System.out.ptrinln("gender");
	}
	}

}
```

int 占4个字节空间 double 占8个字节空间

**变量使用细节**

1，变量表示内存中的一个存储区域

2，该区域有自己的名称和类型

3，变量必须先声明后使用，即有顺序。

4，该区域的数据和值可以在**同一类型**范围内不断变化

5，变量在同一作用域内不能重名

6，**变量=变量名+值+数据类型**变量三要素

**程序中+号的用法**

1，当左右都是数值型时，则做加法运算

2，当左右两边有一方为字符串，则做拼接运算

## 🚩java中的数据类型

![截屏2022-07-18 17.24.33](/Users/minwenrui/Desktop/截屏2022-07-18 17.24.33.png)

八大数据类型

整数型：byte【1】short【2】int【4】long【8】（声明加l）浮点类型float【4】，double【8】

字符型char【2】，存放单个字符‘a'

布尔型boolean【1】，存放true，false

 引用数据类型参考C语言指针

<img src="/Users/minwenrui/Desktop/截屏2022-07-18 17.35.43.png" alt="截屏2022-07-18 17.35.43" style="zoom:200%;" />

**int最为常用** 一个字节=8bit

<img src="/Users/minwenrui/Desktop/截屏2022-07-18 17.48.58.png" alt="截屏2022-07-18 17.48.58" style="zoom:200%;" />

浮点数在机器中的存放形式 浮点数=符号位+指数位+尾数位

**细节**

浮点数的使用陷阱

当我们对运算结果进行相等判断时，要小心

应该是以两个数的差值的绝对值，在某个精度范围进行判断

如果直接查询得到的小数或直接赋值，可以判断相等。

### APi文档的使用

API（Application Programming Interface，应用程序接口）是java提供的基础编程接口

中文在线文档：https://www.matools.com

java语言提供了大量的基础类，因此Oracle公司也为这些基础类提供类相应API文档，用于告诉开发者如何使用这些类，以及这些类里包含的方法。

java类的组织形式

![截屏2022-07-19 16.46.39](/Users/minwenrui/Desktop/截屏2022-07-19 16.46.39.png)

举例说明使用ArrayLIst类有哪些方法

包➡️类➡️方法

直接检索

### **字符类型介绍**

```java
//演示char的基本使用

public class Vardetail{
  
  //编写一个main方法
  public static void main(String[] args){
    char c1 = 'a';
    char c2 = '\t';//\t整体表示
    char c3 = '明';
    char c4 = 99;//字符类型可以直接存放一个数字
    System.out.println(c1);
    System.out.println(c2);
    System.out.println(c3);
    System.out.println(c4);//在java中，char的本质是一个整数，在默认输出时，是unicode码对应的字符；
    //要输出对应的数字，可以(int)对应字符
    char c5 = 'b'+ 1;
    System.out.println((int)c5);//99
    System.out.println(c5);//99->对应的字符->编码表ASCII（规划好）=>c
  }
}
```

快捷键的占用修改

**字符细节**

1,字符常量是用单引号('')括起来的单个字符

例如 char c1 = 'a'

2，java中还允许使用转义字符'\\'来将其后的字符转变为特殊字符型常量。例如 char c3 = '\\n';//'\\n'表示换行字符

3，在java中，char本质是一个整数，在输出时，是unicode码对应的字符。

http://tool.chinaz.com/Tools/Unicode.aspx

4，可以直接给char赋一个整数，然后输出时，会按照对应的unicode字符输出

5，char类型是可以进行运算的，相当于一个整数，因为都有对应的unicode编码

### **字符类型的本质**

1，字符型储存到计算机中，需要将字符对应的码值（整数找出来），比如'a'

储存：'a'-->码值97-->二进制-->存储

读取：二进制=>97--->'a'=>显示

2，字符和码值的对应关系是通过字符编码表决定的（国际规定）

介绍一下字符编码

1，ASCII码表

上世纪六十年代，美国制定了一套字符编码（使用一个字节），对英语字符与二进制之间的关系，做了统一规定。这被称为ASCII码，ASCII一共规定了128个字符的编码，只占用一个字节的后面7位，最前面的一位统一规定为0。

（ 一个字节表示一个128个字符，实际上一个字节可以表示256个字符，只用128个）

缺点：不能表示所有字符

2，Unicode（固定大小的编码 使用两个字节来表示字符，字母和汉字统一都是占用两个字节）

将世界上所有的符号纳入其中。每一个符号都给予一个独一无二的编码，使用Unicode没有乱码问题。

缺点：一个英文字母和一个汉字都占用两个字节，这对于存储空间来说是浪费。

最大字符是65536 2的16次方

**Unicode兼容ASCII**

utf-8（编码表，大小可变的编码，字母使用一个字节，汉字使用三个字节）

gbk（可以表示汉字，而且范围很广，字母使用1个字节，汉字两个字节）

gb2312（可以表示汉字，gb2312<gbk）

Big5 码（繁体中文 台湾 香港）

### 布尔类型：boolean

判断真假的逻辑运算

一般用于程序流程控制

```java
public class Boolean01{

	//编写一个main方法
	public static void main(String[] args) {
		//演示判断成绩是否通过的判断
		//定义一个布尔变量
		boolean isPass = false;
		if(isPass == true){
			System.out.println("テストは合格");
		 
	}else{
		System.out.println("残念ながら、不合格");
		}
	}
}


```

## 基本数据类型的转换

当java程序在进行赋值或者运算时，精度小的类型自动转换为精度大的数据类型。

char➡️int➡️long➡️float➡️double

byte➡️short➡️int➡️long➡️float➡️double

AutoConvert.java

```java
public class AutoConvert{

	//编写一个main方法
	public static void main(String[] args) {
		//演示自动转换
		int num = 'a';
		double d1 = 80;
		System.out.println(num);//97 a字母对应的码值
		System.out.println(d1);//80.0
	}
}


```

### 自动类型转换细节

精度低自动转换成精度高的

```java
public class AutoConvertDetail{

	//编写一个main方法
	public static void main(String[] args) {
		//细节1:有多种类型的数据混合计算时。
		//系统首先自动将所有数据转换成容量最大的那种数据类型，然后进行运算
		int n1 = 10;
		double d1 = n1 + 1.1;
		//float d1 = n1 + 1.1F;//结果类型是float
		//细节2:当我们把精度（容量）大的数据类型赋值给精度小的类型时就会报错，反之就会进行自动类型转换
		//细节3:char short byte 之间无法互相自动转换
		byte b1 = 10;//对，-128-127
		//当把具体的数赋给byte时，1）先判断该数是否在byte范围内，如果是就可以
		int n2 = 1;
		//byte b2 = n2;//如果是变量赋值，直接判断类型
		char c1 = b1;//错误byte不能转成char
		//细节4:byte ，short，char，他们三者之间可以计算，在计算时首先转换提升精度为int类型
		byte b2 = 1;
		short s1 = 1;
		//short s2 = b2 + s1;//输出为int 报错
		int s1 = b2 + s1;
		//boolean类型不参与转换
		//自动提升原则：表达式结果的类型自动提升为操作数中的最大类型
		byte b4 = 1;
		short s3 = 100;
		int num200 =1;
		double num300 = 1.1F;
		double num500 = b4 + s3 + num200 + num300;


	}
}


```

### 强制类型转换

将容量大的数据类型转换为容量小的数据类型使用时要加上强制转换符()，可能会造成精度损失。

```java
public class ForceConvert{

	//编写一个main方法
	public static void main(String[] args) {
		//演示强制类型转换
		int n1 = (int)1.9;
		System.out.println("n1=" + n1);//1 造成精度的损失

		int n2 = 2000;
		byte b1 = (byte)n2;
		System.out.println("b1=" + n1);//1 造成数据溢出

	}
}


```

**细节**

强制转换符号只对最近的操作数有效，往往会使用小括号提升优先级

char类型可以保存int常量值，不能保存int变量值，需要强转

### 基本数据类型与String类型的转换

**在具体的程序开发中经常用到需要String与基本数据类型之间的相互转换**

```java
public class StringToBasic{

	//编写一个main方法
	public static void main(String[] args) {

		//基本数据类型转字符串

		 int n1 = 100;
		 float f1 = 1.1F;
		 double d1 = 4.5;
		 Boolean b1 = true;
		 String s1= n1 + "";
		 String s2 = f1 + "";
		 String s3 = d1 + "";
		 String s4 = b1 + "";
		 System.out.println(s1 + "" + s2 + "" + s3 + "" + s4);
    
    //String->对应的基本数据类型
    String s5 = "123";
    //解读 使用基本数据类型对应的包装类，的相应方法，得到基本数据类型
    int num1 = Integer.parseInt(s5);
    double num2 = Double.parseDouble(s5);
    float num3 = Float.parseFloat(s5);
    long num4 = Long.parseLong(s5);
    byte num5 = Byte.parseByte(s5);
    boolean b = Boolean.parseBoolean("true");
    short num6 = Short.parseshort(s5);
    
    System.out.println (num1);//23
     System.out.println (num2);//123.0
     System.out.println (num3);//123.0
     System.out.println (num4);//123
     System.out.println (num5);//123
     System.out.println (num6);//123
     System.out.println (b);//true
    //怎么把字符串转成字符->含义是指把字符串的第一个数字取到
    System.out println(s5.charAt(0));
    
    }
}


```

1,在将String类型转换成基本数据类型时，要确保String类型能够转成有效数据。比如123可以转成一个整数，但是“hello”字符串无法转成一个整数

2，如果格式不正确，就会抛出异常(Exception)，程序就会终止。

```java
/**
 *演示字符串转基本数据类型
*/
public class StringToBasicDetail{

	//编写一个main方法
	public static void main(String[] args) {
    String str = "123";
    //转成int
    int n1 = Integer.parse(str);
    System.out.println(n1);
  }
}

```

```java
public class H02{

	//编写一个main方法
	public static void main(String[] args) {
    char c1 = '\n';//换行
    char c2 = '\t';//对齐
    char c3 = '\r';//回车
    char c4 = '\\';//添加一个\
    char c5 = '1';//1
    char c6 = '2';//2
    char c7 = '3';//3
    System.out.println(c1);
    System.out.println(c2);
    System.out.println(c3);
    System.out.println(c4);
    System.out.println(c5);
    System.out.println(c6);
    System.out.println(c7);
  }
}
```

```java
public class H03{

	//编写一个main方法
	public static void main(String[] args) {
    String book1 = "天龙八部"；
      String book = "笑傲江湖"；
      System.out.println(book1 + book2);//➕有字符串拼接效果
    
    //性别使用char保存
    char c1 = '男';
    char c2 = '女'；
      System.out.println(c1+c2);//得到男字码值+女字码值
    
    //保存两本书价格
    double price1 = 123.56;
    double price2 = 100.11;
    System.out.println(price1 + price2);//数字相加
    //➕号的用法
      
   
  }
}
```

```java
public class StringToBasic{

	//编写一个main方法
	public static void main(String[] args) {
    /*
     姓名  年龄 成绩 性别 爱好
    xx     xx  xx  xx  xx
    要求：
    1）用变量将名字，年龄，成绩，性别，爱好存储
    2）使用+
    3）添加适当注释
    4）添加转义字符，使用一条语句输出
    
    */
    //姓名
    String name = "jack";
    int age = 20;
    double score = 80.9;
    char gender = '男';
      String hobby = '打篮球';
    System.out.println("姓名\t年龄\t成绩\t性别\t爱好\n" + name + "\t" + age + "\t" + score + "\t" + gender + "\t" + hobby);
     
   
  }
}
```

# 运算符

运算符是一种特殊的符号，用以表示数据的运算，赋值和比较。

## 1，算术运算符

对数值类型的变量进行运算的，在java中使用非常多。

![截屏2022-07-29 01.30.42](/Users/minwenrui/Desktop/截屏2022-07-29 01.30.42.png)

Arithmicoprater （算术运算符）

```java
/**
*演示算数运算符的使用
*/
public class ArithmeticOperater{

	//编写一个main方法
	public static void main(String[] args){
		//使用
		System.out.println(10 / 4);//从数学来看2.5，java中2保留整数
		System.out.println(10.0 / 4);//2.5
		//注释快捷键ctrl+/，再次输入ctrl+/取消
		double d = 10 / 4;//double高精度
		System.out.println(d);//2.0

		//%取模 取余数
		//在java % 的本质 看一个公式a % b = a - a / b * b
		//-10 % 3 = > -10 - (-10) / 3 * 3
		System.out.println(10 % 3 );//1

		System.out.println(-10 % 3);//-1
		System.out.println(10 % -3);//1

		//自增 ++ 的使用
		//如果作为独立语句使用前++ 等于后++
		int i = 10;
		i++;//自增 等价于i = i + 1；
		++i;//自增 等价于i = i + 1；
		System.out.println("i=" + i);//12

		/*
		作为表达式使用
		前++：++i先自增后赋值
		后++：i++先赋值后自增
		*/
		int j = 8;
		//int k = ++j;//等价 j=j+1;k=j;
		int k = j++;//等价 k = j；j=j+1;
		System.out.println("k=" + k + "j=" + j);//9 9


	}
}

```

面试题

Int i= 1;

i=i++;//规则使用临时变量（1）temp=1；（2）i=i+1（3）i=temp 

```java
/**
*演示算数运算符的使用
*/
public class ArithmeticOperaterExercise{

	//编写一个main方法
	public static void main(String[] args){
		//需求：
		//假如还有59天放假， 问：合xx星期零xx天
		//思路分析
		//（1）使用int 变量 days 保存 天数
		//（2）一个星期7天 星期数：days/7 零xx天：days %7

		int days = 59;
		int weeks = days / 7;
		int leftDays = days % 7;
		System.out.println(days + "天 合" + weeks + "星期零" + 
			leftDays + "天");

		//1.需求
		//定义一个变量保存华氏温度，华氏温度转换摄氏温度的公式为
		//：5/9*(a-100)，请求出华氏温度对应的摄氏温度
		//　考虑数学公式和java语言的特性
		//2.思路分析
		//（1）先定义一个double a 变量保存华氏温度
		//（2）根据给出的公司，进行计算即可　
		//（3）将得到的结果保存到double a
		//走代码
		double a = 1039.8;
		double b = 5.0 / 9 * (a - 100);
		System.out.println("华氏温度"+a
			+"对应的摄氏温度="+b);

	}
}
```



## 2，赋值运算符

把某个运算后的值赋给指定的变量

分为两大类

### 基本赋值运算符 =

### 复合赋值运算符  += -= *=  %= /=

a+=b ;等价于a=a+b

```java
/**
*演示赋值运算符的使用
*/
public class AssignOperator{

	//编写一个main方法
	public static void main(String[] args){
		int n1 = 10;
		n1 += 4;//n1 = n1 + 4;
		System.out.println(n1);
		n1 /= 4;//n1 = n1 / 4;

		//复合赋值运算符会进行类型转换
		byte b = 3;
		b += 2;//等价 b =(byte) (b + 2);
		b ++;
  }
}
```

赋值运算符特点

1）运算顺序从右向左 int num = a + b + c

2）赋值运算符的左边 只能是变量，右边可以是变量，表达式，常量值

int num = 20;int num = 78*34-23;int num3 = a;

3)复合赋值运算符等于下面的效果

比如：a+=3；等价于a = a+3；

4）复合赋值运算符会进行类型转换

## 3，关系运算符【比较运算符】

1).关系运算符的结果都是boolean型，也就是要么是true要么是false

2）关系表达式经常用在if结构的条件中或循环结构的条件中

![截屏2022-08-05 16.41.21](/Users/minwenrui/Desktop/截屏2022-08-05 16.41.21.png)

```java
/**
*演示关系运算符的使用
*/
public class RelationalOperator{

	//编写一个main方法
	public static void main(String[] args){
		
		int a = 9;
		int b = 8;
		System.out.println(a > b);
		System.out.println(a >= b);
		System.out.println(a <= b);
		System.out.println(a < b);
		System.out.println(a == b);
		System.out.println(a != b);
		boolean flag = a > b;
		System.out.println("flag="　+　flag);


	}
}
```

3)关系运算符组成的表达式被称为关系表达式。a>b

## 4，逻辑运算符

1)用于连接多个条件多个关系表达式，最终的结果也是boolean值

![截屏2022-08-05 17.20.42](/Users/minwenrui/Desktop/截屏2022-08-05 17.20.42.png)

### 逻辑与 短路与

```java
/**
*演示逻辑运算符的使用
*/
public class LogicOperator{

	//编写一个main方法
	public static void main(String[] args){
		//&& 和 &案例演示
		int age = 50;
		if(age > 20 && age < 90){
			System.out.println("ok1");
		}

		//&逻辑与的使用
		int age = 50;
		if(age > 20 & age < 90){
			System.out.println("ok2");
		}

		//区别
		int a = 4;
		int b = 9;
		//对于&&短路与而言，如果第一个条件为false，后面的条件不再判断
		//对于&逻辑与而言，如果第一个条件为False，后面的条件仍然会判断
		if(a < 1 && ++b < 50){
			System.out.println("ok300");
		}
		System.out.println("a=" + a + "b"+ b);//4 10



	}
}
```

![截屏2022-08-05 17.52.58](/Users/minwenrui/Desktop/截屏2022-08-05 17.52.58.png)

2）在开发中基本使用&&短路与，开发效率高。

### 逻辑或 短路或

![截屏2022-08-05 17.55.41](/Users/minwenrui/Desktop/截屏2022-08-05 17.55.41.png)

```Java
/**
*演示逻辑运算符| ||的使用
*/
public class LogicOperator{

	//编写一个main方法
	public static void main(String[] args){
		//||短路或 和 ｜逻辑或 案例演示
		// ｜｜规则两个条件中只要有一个条件成立，结果为true，否则为False
		int age = 50;
		if(age > 20 || age < 90){
			System.out.println("ok1");
		}

		//&逻辑或的使用
		int age = 50;
		if(age > 20 | age < 90){
			System.out.println("ok2");
		}

		//区别
		//
		int a = 4;
		int b = 9;
		
		if(a > 1 || ++b > 4){
			Syste.out.println("ok300");
		}
		System.out.println("a=" + a + "b"+ b);//4 10



	}
}
```

### 逻辑非 逻辑异或

```java
/**
*！^的使用
*/
public class InverseOperator{

	//编写一个main方法
	public static void main(String[] args){
		
		//!操作是取反 T->F,F->T
		System.out.println(60 > 20);
		System.out.println(!(60 > 20));

		//a^b:叫逻辑异或，当a 和 b不同时，则结果为true；否则为False
		boolean b = (10 > 1) ^ (3 > 5);
		System.out.println("b=" + b);//T
	}
}
```

## 5，位运算符【需要二进制基础】

### **进制转换**

二进制转十进制规则

从右边最低位开始，将每个位上的数提取出来，乘以2的（位数-1）次方，然后求和。

八进制转十进制规则

从右边最低位开始，将每个位上的数提取出来，乘以8的（位数-1）次方然后求和。

十六进制转十进制规则

从右边最低位开始，将每个位上的数提取出来，乘以16的（位数-1）次方，然后求和。

十进制转二进制

将该数不断除以2，直到商为0为止，然后将每步得到的余数倒过来。

十进制转八进制

将该数不断除以8，直到商为0为止，然后将每步得到的余数倒过来。

十进制转16进制

将该数不断除以16，直到商为0为止，然后将每步得到的余数倒过来。

二进制转八进制

从低位开始，将二进制数每三位一组，转成一个八进制数即可。

二进制转十六进制

从低位开始，将二进制数每四位一组，转成一个八进制数即可。

八进制转二进制

将八进制的每一位数，转成对应的一个3位的二进制数即可

十六进制转二进制

将十六进制的每一位，转成对应的4位的一个二进制数即可。

数字1在二进制数中的不同位上代表不同的值，按从左至右的次序，这个值以二倍递增。

### **原码反码补码**

1.二进制的最高位是符号位：0表示正数，1表示负数

2.正数的原码反码补码都一样（三码合一）

3.负数的反码=他的原码符号位不变，其他位取反。

4.负数的补码=他的反码+1，负数的反码=负数的补码 -1

5.0的反码，补码都是0.

6.java没有无符号数，换言之，java中的数都是有符号的。

7.在计算机运算时候，都是以**补码的方式来运算**的

8.**当我们看运算结果的时候，要看他的原码**

**位运算符**

java中有7个位运算（&,|,^,~,>>,<<,和>>>）

分别是按位&，按位或｜，按位异或^，按位取反~.运算规则为

按位与 &： 两位全为1，结果为1，否则为0

按位或｜： 两位有一个为1，结果为1，否则为0

按位异或^： 两位有一个为0，一个为1，结果为1，否则为0

按位取反～： 0变1 1变0

另三个

算术右移>>:低位溢出，符号位不变，并用符号位补溢出的高位

算术左移<<:符号位不变低位补0

逻辑右移>>>也叫无符号右移，运算规则是低位溢出，高位补0

```java
//位运算
public class BitOperator{

	//编写一个main方法
	public static void main(String[] args){
    System.out.println(2&3);//2
    System.out.println(~-2);//
  }
}
    
```



## 6，三元运算符（Ternary）

基本语法：（本质是if--else语句）

条件表达式？表达式1:表达式2；

运算规则：

1.如果条件表达式为true，运算后的结果是表达式1；

2.如果条件表达式为False，运算后的结果是表达式2；

```java
//三元运算符的使用
public class TernaryOperator{

	//编写一个main方法
	public static void main(String[] args){
    
    int a = 10;
    int b = 99;
    //解读
    //1.a>b为False
    //2.返回b--，先返回b的值，然后再b-1
    //3.返回的结果是99
    int result = a > b ? a++:b--;
    System.out.println("result="+result);
    System.out.println("a="+ a);
    System.out.println("b="+ b);
    
  }
}
```

```java
//三元运算符细节

public class TernaryOperaterDetail{
  
  //编写一个main方法
  public static void main(String[] args){
    //表达式1和表达式2要为可以赋给接收变量的类型（或可以自动转换）
    int a = 3;
    int b = 8;
    int c = a > b ? a : b;
    double d = a > b ? a : b + 3;//可以 满足自动转换
    
  }
}
```

```java
public class TernaryOperaterDetail{
  
  //编写一个main方法
  public static void main(String[] args){
    //案例：实现三个数的最大值
    int n1 = 55;
    int n2 = 33;
    int n3 = 123;
    //思路
    //1.先得到n1 n2中的最大数，保存到max1
    //2.然后求出Max1和n3中的最大数，保存到max2
    
    int max1 = n1 > n2 ? n1 : n2;
    int max2 = max1 > n3 ? max1 : n3;
    System.out.println("MAX="+ max2);
    
    //使用一条语句实现
    int max = (n1 > n2 ? n1 : n2) >n3 ?
              (n1 > n2 ? n1 : n2):n3;
    System.out.println("最大数=" + max);
      
  }
}
```

## 运算符优先级

![截屏2022-08-18 15.20.38](/Users/minwenrui/Desktop/截屏2022-08-18 15.20.38.png)

1.运算符有不同的优先级，所谓优先级就是表达式运算中的运算顺序。如右表，上一行运算符总优于下一行

2.只有单目运算符，赋值运算符；是从右往左运算的。

1）（）{}等

2）单目运算 ++ --

3）算术运算符

4）位移运算符

5）比较运算符

6）逻辑运算符

7）三元运算符

8）赋值运算符



## 标识符的命名规则和规范

标识符概念：

1.java中对各种变量，方法和类等命名时使用的字符称为标识符

2.凡是自己可以起名字的地方都称为标识符 int num1 = 90

**标识符的命名规则**

1.由26个英文字母大小写，0～9，_$组成

2.数字不能开头

3.不能使用关键字和保留字 goto

4.java中严格区分大小写，长度没有限制。

5.标识符不能包含空格。

**标识符命名规范**

1.包名：多单词组成时所有字母都小写com.hsp

2.类名，接口名：多单词组成时，所有单词的首字母都大写 TankShotGame

3.变量名，方法名：多单词组成时，第一个单词首字母小写，第二个单词开始每个单词首字母大写【小驼峰 驼峰法】tankShotGame

4.常量名：所有单词都大写。多单词时每个单词用下划线连接 TAX_RATE

5.类 包接口需要遵守规范

**关键字**

java底层专门用途的字符串

特点：所有字母都小写

**保留字**

可能会用到的底层字符串

## 键盘输入语句

在编程中，需要接收用户输入的数据，就可以使用键盘输入语句来获取。(要使用一个类必须引入他所在的包)

input.java，需要一个扫描器（对象），就是Scanner

1）导入该类所在的包，java.til.*

2）创建该类的对象（声明变量）

3）调用里面的功能

```java
import java.util.Scaner;//表示把java.util的下Scanner类导入
public class input{
  
  //编写一个main方法
  public static void main(String[] args){
    //演示接收用户的输入
    //步骤
    //Scanner类表示简单文本扫描器，在java.util包
    //1.引入/导入Scanner类所在的包
    //2.创建Scanner对象
    Scanner myscanner = new Scanner(System.in);
    //3.接收用户的输入
    System.out.println("请输入名字");
    //当程序执行到next方法时，会等待用户的输入
    String name = myscanner.next();//接收用户的输入
    System.out.println("请输入年龄");
    String age = myscanner.nextInt();//接收用户的输入
    System.out.println("请输入薪水");
    String sal = myscanner.nextDouble();//接收用户的输入
    System.out.println("人的信息如下:");
    System.out.println("名字="+name +"年龄="+age+"薪水="+sal)
    
      
    
  }
}
```

## 練習

-10.5%3=

//当a%b中a是小数时，公式=a-(int)a/b*b

//-10.5%3=-10.5-(-10)/3*3=-10.5+9=-1.5

//注意：有小数参与的运算，得到的结果是近似值

```
int i=66;
System.out.println(++i+i);//先自增后相加134
```

int num1 = (int)"18";//❌String类型强制转换基本类型应该 Integer.parselnt("18");

int num2=18.0;//❌ 类型不匹配

double num  = 3d;//对

double num4 =8；//ok 自动转换

int i =48;char ch =i+1;//❌int >char

byte b = 19；short s =b+2//❌

```
String str ="18.8";//字符串可否转成double
double d1 = Double.parseDouble(str);

char c1='韩'；
String str2= c1 +"";

```

# 程序控制结构

程序的流程控制决定程序如何执行 主要分为三大流程控制语句

## 顺序

程序从上到下逐行地执行，中间没有任何的判断和跳转。

（先定义后使用）

## 分支（if else switch）

让程序有选择的执行，分支控制有三种

### 1）单分支

基本语法

```java
if(条件表达式){
  执行代码块：（多条语句）
}
```

说明：当条件表达式为ture时，就会执行{}内地代码。如果为flase，就不执行。特别说明，如果{}内只有一条语句，则可以不用加{}.

```java
//if的快速入门
import java.util.Scanner;//导入
public class If01{
  //编写一个main主方法
  public static void main(String[] args){
    //1.接收输入的年龄，应该定义一个Sacnner对象
    //2.把年龄保存到一个变量int age
    //3.使用if判断，输出对应信息
    
    Scanner myScanner = new Scanner(System.in);
    System.out.println("请输入年龄");
      int age = myScanner.nextInt();
    if(age > 18){
      System.out.println("年龄大于18，负刑事责任");
        System.out.println("程序继续...");
    }
   }

}
```

![](/Users/minwenrui/Desktop/截屏2022-08-26 15.06.27.png)

#### 流程图

![截屏2022-08-26 15.12.33](/Users/minwenrui/Desktop/截屏2022-08-26 15.12.33.png)

### 双分支

基本语法

```java
if（条件表达式）{
  执行代码块1
}
else{
  执行代码块2
}
```

```java
//if-else的快速入门
import java.util.Scanner;
public class If01{
  //编写一个main主方法
  public static void main(String[] args){
    Scanner myScanner = new Scanner(System.in);
    System.out.println("年齢を入力してください");
    int age = myScanner.nextInt();
    if(age > 18){
      System.out.println("年龄大于18.逮捕されました");
      }else{
        System.out.println("未成年不负刑事责任");
      }
    System.out.println("继续")
}
}
```

#### 流程图

![截屏2022-08-26 16.04.22](/Users/minwenrui/Desktop/截屏2022-08-26 16.04.22.png)

```java
//单分支和双分支的练习
public class If01{
  //编写一个main主方法
  public static void main(String[] args){
    //编写程序，声明2个double型变量并赋值
    //判断第一个数大于10.0，且第二个数小于20.0，打印两数之和
    
    double d1 = 34.5;
    double d2 = 2.6;
    if(d1 > 10.0 && d2 < 20.0){
      System.out.println("两数和="+(d1 + d2));
    }
    
    //定义两个变量int，判断两者的和
    //是否能被3整除又能被5整除
    
    int num1 = 15;
    int num2 = 30;
    int sum = num1 + num2;
    if(sum % 3 == 0 && sum % 5 == 0){
      System.out.println("既能被3整除又能被5整除");
    }else{
      System.out.println("不能整除");
    }
    
    //判断一个年份是否为闰年，闰年的条件时复合下面二者之一
    //1）年份能被4整除，但不能被100整除；2）能被400整除
    int year = 2022;
    if (year % 4 == 0 && year % 100 != 0|| year % 400 == 0){
      System.out.println(year + "是闰年");
    }else{
      System.out.println(year + "不是闰年");
    }
    
    
    
  }    
  }
```

### 多分支

```java
if(条件表达式1){
  执行代码块1；
}
else if（条件表达式2){
  执行代码块2
}
.......
  else{
    执行代码块n;
  }
```

实现多个业务的处理

![截屏2022-08-26 18.22.10](/Users/minwenrui/Desktop/截屏2022-08-26 18.22.10.png)

1.当条件表达式1成立时，即执行代码块1.

2.如果条件表达式1不成立，才去判断表达式2是否成立

3.如果表达式2成立，就执行代码块2

4.以此类推，如果所有表达式都不成立

5.则执行else的代码块（只有一个执行入口）

特别说明：

1）多分支可以没有else ，如果所有的条件表达式都不成立则一个执行入口都没有。

2）如果有else，所有的条件表达式都不成立，则默认执行else代码块。

```java
//分支练习
import java.util.Scanner;
public class If01{
  //编写一个main主方法
  public static void main(String[] args){
    Scanner myScanner = new Scanner(System.in);
    System.out.println("信用ポイント1-100入力してください:");//接收输入
    int grade = myScanner.nextInt();
    //先对输入的信用分进行一个范围内的有效判断1-100否则提示输入错误
  if(grade >= 1 && grade <= 100){


    //四种情况
    if(grade == 100){
      System.out.println("信用極めて良い");
    }else if(grade > 80 && grade <= 99){
      System.out.println("信用優秀");
    }else if(grade >=60 && grade <= 80){
      System.out.println("信用一般");
    }else{
      System.out.println("信用不合格");
    }
  }else{
      System.out.println("信用分需要在1-100，请重新输入：）");
    }
    
  }
}
  
```

### 嵌套分支

在一个分支结构中又完整的嵌套了另一个完整的分支结构，里面的分支的结构称为内层分支；外面的分支结构称为外层分支。（**嵌套最好不要超过3层**可读性差）

基本语法

```java
if(){
  if(){
    //if-else....
  }else{
    //if else
  }
}
```

```java
import java.util.Scanner;
public class If01{
  //编写一个main主方法
  public static void main(String[] args){
    /*
    参加歌手比赛，如果成绩大于8.0进入决赛
    否则提示淘汰。并且根据性别提示进入男子组或女子组。
    输入成绩和性别，进行判断和输出信息
    */
    //1.创建Scanner对象，接收用户输入
    //2.接收成绩保存到double score
    //3.使用if-else双分支判断 根据初赛成绩大于8.0判断进入决赛或淘汰
    //4.如果进入决赛，再接收char gender，使用if-else输出信息
    Scanner myScanner = new Scanner(System.in);
    System.out.println("成績入力してください");
    double score = myScanner.nextDouble();
    if(score > 8.0){
      System.out.println("性別入力してください");
      char gender = myScanner.next().charAt(0);//字符串转成字符char把字符串的第一个字符得到
      if(gender == '男'){
        System.out.println("进入男子组");
      }else if(gender == '女'){
        System.out.println("进入女子组");
      }else{
        System.out.println("性别输入错误");
      }
    }else{
      System.out.println("あなたは淘汰しました");
    }
  }
}
```

出票系统：根据淡旺季的月份和年龄，打印票价

```java
import java.util.Scanner;//表示把java.util下的Scanner类导入
/**
 * @Description
 * @Author:Bill.MIN
 * @Date:2022/08/28 14:30
 */

public class Ticket{
  //编写一个main主方法
  public static void main(String[] args){
    /*
    出票系统：根据淡旺季的月份和年龄，打印票价
    4-10旺季：
    成人（18-60）:60
    儿童（<18）:30
    老人（>60）:1/3
    淡季：
    成人：40
    其他：20
    */
    Scanner myscanner = new Scanner(System.in);
    System.out.println("===チケットシステム===");
    System.out.println("月と年齢を入力してください：");
    int month = myscanner.nextInt();
    int age = myscanner.nextInt();

    if (month >= 4 && month <= 10) {
      System.out.println("今は人気季節です");
      if(age < 18 && age >0){
        System.out.println("子供のチケット半額:"+30);
      }
      if (age >=18 && age <= 60) {
        System.out.println("正常の価格" + 60);
      }
      if (age > 60 && age < 150){
        System.out.println("高齢者の価格" + 20);
      }else{
        System.out.println("正常年齢入力してください");
      }

    }
    if((month >=1 && month < 4) || (month > 10 && month <= 12)){
       System.out.println("今はイベント季節です");

      if(age >= 18 && age <= 60){
        System.out.println("正常の価格" + 40);
      }
      if((age > 0 && age < 18) || (age > 60)){
        System.out.println("イベント価格" + 20);
      }
      else{
        System.out.println("正常年齢入力してください");
      }
    }

  }
}
```

### Switch分支结构

```java
//基本语法
 switch(表达式){
   case 常量1://当...
   语句块1;
   break;
   case 常量2://当...
   语句块2;
   break;
   case 常量n://当...
   语句块n;
   break;
   default:
     default语句块;
   break;
  }
```

1.switch关键字，表示switch分支

2.表达式对应一个值

3.case常量1:当表达式的值等于常量1就执行语句块1

4.break：表示退出switch

5.如果与case常量都不匹配就执行default语句块。

![截屏2022-08-28 19.05.50](/Users/minwenrui/Desktop/截屏2022-08-28 19.05.50.png)

```java
public class Switch01{
  /*
  请编写一个程序，该程序可以接收一个字符，比如a,b,c,d,e,f,g
  a表示星期一，b表示星期二
  根据用户的数入显示相应的信息，要求使用switch语句完成
  */
  //创建一个Scanner对象
  //使用switch来完成匹配并输出对应信息
  
  Scanner myscanner = new Scanner(System.in);
  System.out.println("请输入一个字符（a-g）");
  char c1 = myScanner.next().charAt(0);//把接收到的字符串转成一个字符，也就是说选取第一个字符
  //Java中只要有值返回都可以称为一个表达式
  switch(c1){
    case 'a':
      System.out.println("今日は月曜日");
      break;
    case 'b':
      System.out.println("今日は火曜日");
      break;
    case 'c':
      System.out.println("今日は水曜日");
      break;
    default:
      System.out.println("入力無効");
      break;//可有可无
      
  }
  System .out.println("退出switch，继续执行")
}
```

#### switch细节

```java
public class Switchdetail{
  public static void main(String[] args){
    //细节1 表达式数据类型，应和case常量类型一致
    //或者是可以自动转换成可以相互比较的类型，比如输入的是字符，常量是int
    
    //细节2 switch表达式的返回值必须是：（int，short byte，char，enum，String）
    
    //细节3 case子句中的值必须是常量或常量表达式(1,'a'),而不能是变量
    
    //细节4 default子句是可选的
    //如果没有default子句，又没有匹配任何常量则没有任何输出
    
    //细节5 break用来执行完一个case分支后使程序跳出switch语句块；
    //如果没有break，程序会执行到switch结尾
    char c = 'a';
    switch(c){
      case'a'
        System.out.println("ok1");
        break;
      case "hello":
        System.out.println("ok2");
        break;
      default:
        System.out.println("ok3");
        
    }
  }
}
```

Exercise

```java
import java.util.Scanner;
public class SwitchExercise{
  public static void main(String[] args){
    //使用switch把小写类型的
    //char型转换成大写（键盘输入）。只转换a->A,b->B.其他的输出“other”

    //创建Scanner对象
    Scanner myScanner = new Scanner(System.in);
    System.out.println("a-e入力してください");
    char c1 = myScanner.next().charAt(0);
    switch(c1){
      case'a':
        System.out.println("A");
        break;
      case'b':
        System.out.println("B");
        break;
      case'c':
        System.out.println("C");
        break;
      case'd':
        System.out.println("D");
        break;
      case'e':
        System.out.println("E");
        break;
      default:
        System.out.println("入力無効です");
    }
    
    //对学生成绩大于60分的，输出合格。低于60
    //输出不合格（成绩不能大于100），提示成绩/60
    //进行一个转换 :编程思想
    // 如果成绩在[60,100],int(成绩/60)=1
    // 如果成绩在[0,60),int（成绩/60）=0

    //代码实现
    Scanner sc = new Scanner(System.in);
    System.out.println("テストの点数入力してください");
    double score = myScanner.nextDouble();
    if(score >= 60 && score <= 100){
    switch((int)(score / 60)){
      case 0:
        System.out.println("不合格");
        break;
      case 1:
        System.out.println("合格");
        break;

    }
  }else{
    System.out.println("入力成績は0-100");
  }

  //根据用于指定月份
  //打印该月份所属的季节
  //345春季，678夏季，91011秋季，1212冬季
  //使用穿透

  //创建Scanner对象，接收用户输入
  //使用int month接收
  //使用switch匹配，穿透来完成

  Scanner sca = new Scanner(System.in);
  System.out.println("月を入力してください");
  int month = myScanner.nextInt();
  switch(month){
    case 3:
    case 4:
    case 5:
      System.out.println("这是春季");
      break;
    case 6:
    case 7:
    case 8:
      System.out.println("这是夏季");
      break;
    case 9:
    case 10:
    case 11:
      System.out.println("这是秋季");
      break;
    case 12:
    case 1:
    case 2:
      System.out.println("这是冬季");
      break;
    default:
      System.out.println("入力無効です");

 
    }
  }

  }

```

Switch和if的比较

1.如果判断的具体数值并不多，而且符合byte,short,int,char,enum[枚举]，String这六种类型。虽然两个语句都可以使用，建议使用switch语句。

2.其他情况：对区间判断，对结果为boolean类型判断，使用if。if的使用范围更广。

## 🚩循环（for，while，do while）

### for

可以让代码循环的运行

```java
public class For01{
  
 pubilc static void main(String[] args){
    for(int i = 1;i <= 10;i ++){
      System.out.println("亀田けんのミンです");
    }
  }
}
```

基本语法

```java
for(循环变量初始化；循环条件；循环变量迭代){
  循环操作（可以多条语句);
}
```

1,for关键字，表示循环控制

2，for有四要素1）循环变量初始化2）循环条件3）循环操作4）循环变量迭代

3，循环操作，这里可以有多条语句，也就是我们要循环执行的代码

4，如果循环操作中只有一条语句，可以省略{}，建议不省略

![截屏2022-08-30 18.12.27](/Users/minwenrui/Desktop/截屏2022-08-30 18.12.27.png)

```java
//演示for的使用细节
public class ForDetail{
  
 pubilc static void main(String[] args){
   //for(;循环判断条件;)
   //中的初始化和变量迭代可以写到其他地方，但两边的分号不能省略
    int i = 1
    for(;i <= 10;){
      System.out.println("亀田けんのミンです");
      i ++
    }
    System.out.println("i = "+ i);//11
    //补充
    for(";;"){//表示一个无限循环死循环
      System.out.println("ok");
    }
   //
   //循环初始值可以有多条初始化语句，但要求类型一样，并且中间用逗号隔开
   //循环变量迭代也可以有多条变量迭代语句，中间用逗号隔开
   //使用内存分析法
   int count = 3;
   for(int i = 0,j = 0; i < count;i ++,j+=2){
     System.out.println("i=" + i + "j=" + j);//
   }
  }
}
```

**两个重要的编程思想**

```java
public class ForExercise{
  public static void main(String[] args){
    //打印1～100之间所有是9的倍数的整数，统计个数及总和
    //两个编程思想：
    //1.化繁为简：即将复杂的需求，拆解成简单的需求，逐步完成
    //2.先死后活：先考虑固定的值，然后转成可以灵活变化的值
    //化繁为简
    //1）完成输出1-100的值
    //2）在输出到过程中，进行过滤，只输出9的倍数 i% 9
    //3）统计个数 定义一个变量 int cout = 0；当条件满足时 cout++
    //4）求总和，定义一个变量int sum = 0；当条件满足时累积sum += i
    //先死后活
    //为适应更好的需求，把范围开始和结束的值做出变量
    int start = 1;
    int end = 100;
    int count = 0;//定义一个统计倍数个数的变量
    int sum =0;//总和
    int t = 9;
    for(int i = start;i <= end;i++){
      if(i % t == 0){
        System.out.println("i=" + i);
        count++;
        sum += i;
      }
    }
    System.out.println("count=" + count);
    System.out.println("sum=" + sum);
  }
}
```

```java
public class ForExercise2{
  public static void main(String[] args){
    
    //完成表达式的输出
    int n = 5
    for(int i = 0;i <= n;i++){
      System.out.println(i"+"+ (n-i)+"="+n);
    }
  }
}
```

### While

基本语法

```java
循环变量初始化;
while(循环条件){
  
  循环体语句；
  循环变量迭代;
}
```

与for相同也有四要素，只是位置不同

![截屏2022-08-30 18.12.27](/Users/minwenrui/Desktop/截屏2022-08-30 18.12.27.png)

```java
public class While1{
  public static void main(String[] args){
    int i = 1;//循环变量初始化
    while(i <= 10){//循环条件
      System.out.println("亀田けんのミンです");//执行语句
      i++;//循环变量迭代
    }
  }
}
```

```java
public class WhileExercise{
  public static void main(String[] args){
//打印1-100之间所有能被3整除的数
//化繁为简，先死后活
    int i = 1;
    int end = 100;
    int canshu = 3;
    while(i <= end){
      if (i % canshu == 0){
      System.out.println("i="+ i);
      }
      i++;//自增在if循环外
    }
    
    //打印40-200之间所有的偶数
    int j = 40;
    while(j <= 200){
      if(j % 2 == 0){
      System.out.println("i=" + j);
      }
      j++;
    }
  }
}
```

### dowhile

基本语法

```java
循环变量的初始化
  do{
      循环体语句
      循环变量迭代
  }while(循环条件);
```

1,dowhile是关键字

2，也有循环四要素，只是位置不同

3，先执行后判断，也就是说至少执行一次

4，最后有一个分号

5，while和dowhile的区别

whlie问还不还钱 再打一顿

dowhile先打一遍再问还不还钱（狠人）

![截屏2022-08-31 15.47.44](/Users/minwenrui/Desktop/截屏2022-08-31 15.47.44.png)

```java
public class WhileExercise{
  public static void main(String[] args){
    int i = 1;//循环变量初始化
    do{
      System.out.println("亀田研のMINです");//执行循环语句
      i++;//循环变量迭代
    }While(i <= 10);
    System .out.println("退出dowhlie继续执行..");//继续执行其他程序
    
  }
}
```

練習

```java
public class WhileExercise{
  public static void main(String[] args){
    //打印1-100
    //计算1-100的和
    //统计1-200之间能被5整除但不能被3整除的个数
    //如果李三不还钱，则老韩一直使出五连鞭，直到李三说出还钱为止
    int i = 1;
    int sum = 0;
    do{
      sum = sum + i;
      i++;
    }while(i <= 100);
    System.out.println("总和是" + sum);

    int j = 1;
    int count = 0;
    do{
      if(j % 5 == 0 && j % 3 != 0) {
        System.out.println("j =" + j);
        count++;
      }
      j++;
    
    }while(j <= 200 );
    System.out.println("输出个数" + count);
    
  }
}
```

```java
import java.util.Scanner;
public class WhileExercise{
  public static void main(String[] args){
    
    //如果赵思雨不还钱，则老闵一直使出五连鞭，直到赵思雨说出还钱为止
    Scanner myScanner = new Scanner(System.in);
    char answer = ' ';
    do{
      System.out.println("暴打老胖");
      System.out.println("赵思雨还钱吗? Y/N");
      answer = myScanner.next().charAt(0);
      System.out.println("她的回答是" + answer);
    }while(answer != 'Y');//判断条件

    
  }
}
```

多重循环练习

```java
/**
 *@Author:Bill.MIN
 *@Date:2022/08/31 19:00
 */
import java.util.Scanner;
public class MULExercise{

  public static void main(String[] args){
    //统计三个班的成绩情况，每个班有5名同学
    //求出各个班的平均分和所有班级的平均分【学生成绩从键盘输入】
    //统计三个班及格情况，每个班有5名同学
    
    //
    Scanner myscanner = new Scanner(System.in);
    double totalsum = 0;//累积所有学生分数
    int passnum = 0;//累积及格人数
    int classnum = 3;//班级个数
    int stunum = 5;//学生人数
    for(int j = 1;j <= classnum;j++){
      double sum = 0;
       for(int i = 1;i <= stunum;i++){
       System.out.println("请输入第" + j + "个班第"+ i +"个学生的成绩");
       double score = myscanner.nextDouble();//接收成绩
        if(score >= 60.0){//当有一个成绩及格时 passnum++
          passnum++;
        }
       sum += score;//累积分数
       System.out.println("第"+ j +"个班第" + i +"个学生的成绩为" + score);
      }
      System.out.println("sum =" + sum + "这个班级的平均分是" + (sum / 5));
      totalsum += sum;//总体分数
    }
    System.out.println("三个班平均分为" + (totalsum / 15));
    System.out.println("及格人数为" + passnum);
  }
}
```

打印99乘法表

```java

```

打印空心金字塔

```java
/**
 *@Author:Bill.MIN
 *@Date:2022/08/31 19:00
 */
public class Stars{

  public static void main(String[] args){
    /*
        *
       *  *
      *    *
     ********
     
     思路分析
     化繁为简
     1.先打印一个矩形
     2.打印半个金字塔
     3.打印整个金字塔
     *    //2*层数 -1
    ***
   *****
  *******
 ********* 
     4.打印空心金字塔
     *    //2*层数 -1 当前行的第一个和最后一个位置*
    * *
   *   *
  *     *
 ********* 
      先死后活
      层数做成变量 int totallevel = 5
     
     */
    //技术到位可以直接写出代码
    int totallevel = 5;
    for(int i = 1;i <= totallevel;i++){//i表示层数
      //在输出*之前还要输出空格
      for(int k = 1;k <= totallevel - i;k++){
        System.out.print(" ");
      }
      
      //控制打印每层的*个数
      for(int j = 1;j <= 2 * i - 1;j++){
        //当前行的第一个和最后一个位置*,最后一层全部*
        if(j == 1 || j == 2 * i - 1 || i == totallevel){
            System.out.print("*");
        }else{
          System.out.print(" ");
        }
      }
      //每打印一行后换行 println代表换行
      System.out.print("\n");
    }
    
  }
}
```

空心棱形

### break

跳转控制语句

随机生成1～100个数，直到生成97个数，一共用了几次

提示使用(int)(Math.random)

```java
public class Stars{

  public static void main(String[] args){
    for(int i = 0;i <= 10;i++){
      System.out.println((int)Math.random()* 100 + 1);
    }
    
  }
}
```

基本语法

{.....

break;

......

}

![](/Users/minwenrui/Desktop/截屏2022-09-07 18.36.06.png)

```java
public class Break01{

  public static void main(String[] args){
    for(int i =0;i < =10;i++){
      if(i == 3){
        break;//break直接退出
      }
      System.out.println("i=" + i);//0.1.2
    }
    
  }
}
```

break细节注意事项

1.break语句出现在多层嵌套语句块中时，可以通过标签指明要终止的是哪一层的语句块

2.lable1：{

   lable2:    {

   lable3:       {

   break lable2;

}

1)break语句可以指定退出哪层

2）label1是标签，名称由程序猿制定

3）break后指定到哪个lable就退出到哪里

4）在实际开发中，建议尽量不使用标签（降低可读性）

5）如果没有指定break，默认退出最近的循环体。

```java
public class BreakDetail{

  public static void main(String[] args){
    label:
    for(int j = 0;j < 4;j++){//外层循环
      label2:
      for(int i = 0;i < 10;i++){//内层循环
        if(i == 2){
          break label1;//break label2
        }
        System.out.println("i =" + i);
      }
    }
    }
}
```

```java
/**
 *@Author:Bill.MIN
 *@Date:2022/08/31 19:00
 */
public class BreakExercise{

  public static void main(String[] args){
    //1-100以内的数求和，求出当和第一次大于20的当前数【for + break】
    
    //1.循环1-100，求和sum
    //2.当sum > 20时，记录下当前数，然后break
    //3.在for循环外部，定义变量

    int sum = 0;
    
    //注意i的作用范围在for{}
    for(int i = 1;i <= 100;i ++){
      sum = sum + i;
      if(sum > 20){
        System.out.println("和>20时 i =" + i);
        break;
      }
    }
    //System.out.println("当前数=" + i);

  }
}
```

```java
/**
 *@Author:Bill.MIN
 *@Date:2022/08/31 19:00
 */
import java.util.Scanner;
public class BreakExercise{

  public static void main(String[] args){
    //实现登陆验证，有三次机会，如果用户名为“丁真”，密码“666”提示登录成功
    //否则提示还有几次机会，使用for + break完成

    //1，创建Scanner对象s接收用户输入
    //2，定义String name；String password；保存用户名和密码
    //3，循环登陆3次，如果满足条件就提前退出
    //4，定义一个变量 int chance 记录还有几次登陆机会
    Scanner myScanner = new Scanner(System.in);
    String name = "";
    String password = "";
    int chance = 3;//登陆一次减少一次
    for(int i = 1;i <= 3;i++){
      System.out.println("请输入名字");
      name = myScanner.next();
      System.out.println("请输入密码");
      password = myScanner.next();
      //比较输入的名字和密码是否正确
      //补充说明字符串的内容比较使用方法equals
      if("丁真".equals(name) && "666".equals(password)){
         System.out.println("恭喜你，登录成功");
         break;
      }

      chance--;
      System.out.println("你还有" + chance + "次机会");
    }


  }
}
```

## continue

1）continue语句用于结束本次循环，继续执行下一次循环

2）continue语句出现在多层嵌套的循环体语句时，可以通过标签指明要跳过的是哪一层循环

![截屏2022-09-07 20.55.35](/Users/minwenrui/Desktop/截屏2022-09-07 20.55.35.png)

```java
public class Continue{

  public static void main(String[] args){
    int i = 1;
    while(i <= 4){
      i++;
      if(i == 2){
        continue;
      }
      System.out.println("i =" + i);
    }
    

  }
}
```

细节

```java
public class Continue{

  public static void main(String[] args){
    label1:
    for(int j = 0;j < 4;j++){
      label2:
      for(int i = 0;i < 10;i++){
        if(i == 2){
          //看看输出什么值并分析
          continue;
       }
       System.out.println("i =" + i);//输出四次0～9
      }
    }
    
  }
}
```

## return

return使用在方法，表示跳出所在方法。

```java
public class Continue{

  public static void main(String[] args){
    for(int i = 1;i <= 5;i++){
      
      if(i == 3){
        System.out.println("みんぶんえい" + i);
        //break; //亀田研　亀田研　みんぶんえい３ go on
        //continue;亀田研　亀田研　みんぶんえい３ 亀田研　亀田研 go on
        return;//当return用在方法时，表示跳出方法，如果使用在main方法，表示直接退出程序 亀田研　亀田研　みんぶんえい３
      }
      System.out.println("亀田研");
    }
    System.out.println("go on");
  }
}
```

练习

```java
/**
 * @Author:Bill.MIN
 * @Date:2022/9/08 16:00
 * 
 */
public class H301{

     public static void main(String[] args){
     /*
     实现如下功能
     某人有100000元，每经过一次路口，需要缴费，规则如下
     1）当现金>50000时，每次交5%
     2）当现金<=50000时，每次交1000
     编程计算该人可以经过多少次路口，要求使用while break完成

     1.


     */
      double money = 100000;//还有多少钱
      int count = 0;//累积过的路口
      while(true){
        if(money >50000){
          money *= 0.95;
          count++;
        }else if(money >= 1000 && money <= 50000){
          money -= 1000;
          count++;
        }else{
          break;
        }
      }
      System.out.println("可以过" + count + "个路口");
    

    }
}
```

```java
/**
 * @Author:Bill.MIN
 * @Date:2022/9/08 16:00
 * 
 */
import java.util.Scanner;
public class H301{

     public static void main(String[] args){
      //实现判断一个整数，属于哪个范围：大于0；小于0；等于0
      Scanner myscanner = new Scanner(System.in);
      System.out.println("请输入个整数");
      int n = myscanner.nextInt();

      if(n > 0){
        System.out.println("大于0");
      }else if(n < 0){

        System.out.println("小于0");

      }else{
        System.out.println("等于0");
      }

    

    }
}
```

```java
/**
 * @Author:Bill.MIN
 * @Date:2022/9/08 16:00
 * 
 */
import java.util.Scanner;
public class H301{

     public static void main(String[] args){
      //判断一个年份是否为闰年
      //普通年份能被4整除，且不能被100整除的，是闰年。（ 如2004年就是闰年）
      //世纪年份能被400整除的是闰年。（ 如2000年是闰年，1900年不是闰年）
      //对于数值很大的年份，这年如果能被3200整除，并且还能被172800整除的才是闰年。

      Scanner myscanner = new Scanner(System.in);
      System.out.println("输入一个年份");
      int year = myscanner.nextInt();
      if(year % 4 == 0 && year % 100 != 0 || year % 100 == 0){
        System.out.println("该年份是闰年");
      }else if(year % 3200 == 0 && year % 172800 == 0){
        System.out.println("该年份是闰年");
      }else{
        System.out.println("该年份不是闰年");
      }
    

    }
}
```

```java
/**
 * @Author:Bill.MIN
 * @Date:2022/9/08 16:00
 * 
 */
import java.util.Scanner;
public class H301{

     public static void main(String[] args){
      //判断一个整数是否为水仙花数，所谓水仙花数是指一个3位数，
      //其各个位上数字的立方和等于其本身。例如 153 = 1*1*1 + 3*3*3 + 5*5*5
      
      /*
      先得到n的各个位的数字；使用if判断他们的立方和是否相等即可
      n的百位 = n/100；
      n的十位 = n % 100 /10
      n的个位 = n % 10
      判断
      */
      Scanner myscanner = new Scanner(System.in);
      System.out.println("请输入数字");
      int n = myscanner.nextInt();
      int n1 = n /100;
      int n2 = n % 100 /10;
      int n3 = n %10;
      if(n1 * n1 * n1 + n2 * n2 *n2 + n3 * n3* n3 == n){
        System.out.println("是水仙花数");
      }else{
        System.out.println("不是水仙花数");
      }

    }
}
```

```java
/**
 * @Author:Bill.MIN
 * @Date:2022/9/08 16:00
 * 
 */
import java.util.Scanner;
public class H301{

     public static void main(String[] args){
      //输出1-100之间不能被5整除的数，每5个一行
      /*
      使用计数器int count 统计输出的个数 count % 5 =0就说明输出5个
      换行即可
      */
      int count = 0;//统计输出的个数
      for(int i = 1;i <= 100;i++){
        if(i % 5 != 0){
          count++;
          System.out.print(i + "\t");

          if(count % 5 == 0){
            System.out.println();
          }

        }
      }

    }
}
```

```java
/**
 * @Author:Bill.MIN
 * @Date:2022/9/08 16:00
 * 
 */

public class H301{
  public static void main(String[] args){
    //输出小写的a-z以及大写的Z-A
    //a-z的ASCII编码
    //char的本质是一个整数，在输出时，是unicode码对应的整数
    //char类型可以比较大小

    for(char c1 = 'a';c1 <= 'z';c1++){
      System.out.print(c1 + " ");
    }
    System.out.println("\t");
    for(char c1 = 'Z';c1 >= 'A';c1--){
      System.out.print(c1 + " ");
    }
    }

}
```

```java
/**
 * @Author:Bill.MIN
 * @Date:2022/9/08 16:00
 * 
 */

public class H301{
  public static void main(String[] args){
    //求出1-1/2+1/3-1/4...1/100的和
    /*
    共有100个数，分子为1，分母1-100
    分母为奇数前面是+，偶数时-
    */

    double sum = 0;
    for(int i = 1;i <= 100;i++){
      if(i % 2 != 0){
        sum += 1.0/i;
      }else{
        sum -= 1.0/i;
      }

    }
    System.out.println("sum" + sum);

  }
}
```

```java
/**
 * @Author:Bill.MIN
 * @Date:2022/9/08 16:00
 * 
 */

public class H301{
  public static void main(String[] args){
    //求1+(1+2)+(1+2+3)+....+(1+2+3+4+...+100)的结果
    /*
    共有百项相加
    每一项的数字都在逐渐增加
    双层循环
    */
    int sum = 0;
    for(int i = 1;i <= 100;i++){//i可以表示是第几项，同时当前项最后一个数
      for(int j = 1;j <= i;j++){
        sum += j;
      }
    
    }
    System.out.println(sum);
  }
}
```

# 数组排序和查找

Array

数组可以存放多个同一类型的数据，数组也是一种数据类型，是引用类型。(即一组同一类型的数据)

## 数组

```java
public class Array01{
  public static void main(String[] args){
    //定义一个数组
    //double【】表示是double类型的数组，数组名hens
    //{}表示数组内的值/元素。依次表示数组的第几个元素
    double[] hens = {3,5,1,3.4,2,50};
    //遍历数组得到数组所有元素的和，使用for
    //1.我们可以通过hens【下标】来访问数组的元素
    //  下标是从0开始编号的比如第一个元素是hens【0】
    //2.通过for就可以循环的访问 元素的值
    //3。使用一个变量totalWeight将各个元素累积
    //可以通过数组名.leigth得到数组的长度
    System.out.println("数组长度" + hens.length);
    double totalWeight = 0;
    for(int i = 0;i < 6;i++){
      System.out.println("第" +(i+1) +"元素的值=" + hens[i]);
      totalWeight += hen[i];
    }
    System.out.println("总体重=" + totalWeight + "平均体重" + (totalWeight/6))
    
  }
}
```

### 使用方式1-动态初始化

数组定义

数据类型 数组名【】 = new 数据类型【大小】

int  a[] = new int[5];创建了一个数组，名字a，存放5个int

说明：这是定义数组的一种方法。

数组的访问。a[2]//访问数组第三个数

```java
import java.util.Scanner;
public class Array02{
  public static void main(String[] args){
    //演示数据类型 数组名[] = new 数据类型[大小]
    //循环输入5个成绩，保存到double数组并输出
    
    //步骤
    //1.创建一个double数组大小5
    
    double scores[] = new double[5];
    //2.循环输入
    Scanner myScanner = new Scanner(System.in);
    for( int i = 0;i < scores.length; i++){
      System.out.println("请输入第"+(i + 1)+"个元素的值");
      scores[i] = myScanner.nextDouble();
      
    }
    //输出，遍历数组
    System.out.println("当前数组的元素的情况如下");
     for( int i = 0;i < scores.length; i++){
      System.out.println("第"+(i +1)+"个元素的值" + scores[i]);
    }
      
  }
}
```

### 使用方式2-动态初始化

先声明数组

语法：数据类型 数组名[];也可以 数据类型[] 数组名;

Int a[];或者 int[] a;

创建数组

语法 ：数组名 = new 数据类型[大小];

a = new int[10];

### 使用方式3-静态初始化

语法：数据类型 数组名[]={元素值，元素值...}

### 注意事项

```java
public class Array02{
  public static void main(String[] args){
    //1.数组是多个相同类型数据的组合，实现对这些数据的统一管理
      int[] arr1 = {1,2,3,60,1.1};
      double[] arr2 = {2,3.3};//自动类型转换
    //2.数组的元素可以是任何数据类型，包括基础类型和引用类型，但不能混用
    //3.数组创建后如果没有赋值，有默认值
    //int 0,short 0,byte 0,long 0
    //double 0.0 float 0.0 char \u0000
    //boolean false String null
    //4.使用数组的步骤1.声明数组并开辟空间2.给数组的各个元素赋值3使用数组
    //5.数组的下标从0开始的
    //6.数组的下标必须在指定的范围内使用 否则报下标越界异常
    //数组属于引用类型，本质是对象(object)
     
  }
}
```

练习

```java
public class Array02{
  public static void main(String[] args){
    /*创建一个char类型的26个元素的数组，分别放置A-Z
    使用for循环访问所有元素并打印出来
    提示：char类型数据运算'A'+2 -> 'C'
    
    1.定义一个数组char [] chars = new char[26]
    2.因为 'A' + 1 = 'B' for来赋值
    3.使用for循环访问所有元素
    */
    char[] chars = new char[26];
    for( int i = 0;i < chars.length;i++){
      //chars 是char[]
      //chars[i]是char
      chars[i] = (char)('A' + i);//需要强制转换
    }
    //循环输出
    System.out.println("chars数组");
    for( int i = 0;i < chars.length;i++){
      System.out.print(chars[i] + "");
    }
    
    
  }
}
```

```java
public class Array02{
  public static void main(String[] args){
   //请求出一个数组int[]的最大值{4,-1,9,10,23},并得到对应的下标
   //
   //int[] arr = {4,-1,9,10,23};
   //假定 max = arr[0],maxIndex=0
   //从下标1开始遍历arr，如果max<当前元素 false
   //max = 当前元素；maxIndex = 当前元素的下标
   //当遍历这个数组arr后，max为真正最大值
    
    int[] arr = {4,-1,9,10,23};
    int max = arr[0];
    int maxIndex = 0;
    
    for(int i = 1;i < arr.length;i++){
      
      if(max < arr[i]){
        max = arr[i];
        maxIndex = i;
      }
    }
    System.out.println("max=" + max +"maxIndex=" + maxIndex);
  }
}
```

```java
public class Array01{
  public static void main(String[] args){
    //定义一个数组
   
     double[] arr = {3.3,5,7,9,10}
     double sum = 0;
    for(i = 0;i < arr.length;i++){
      sum += arr[i];
    }
    System.out.println("数组和" + sum + "平均值" + (sum/5));
    
  }
}
```

数组赋值机制

1.基本数据类型赋值，这个值就是具体的数据，而且互相不影响。

```java
public class Array01{
  public static void main(String[] args){
   //基本数据类型赋值,赋值方式是值拷贝
    int n1 = 10;
    int n2 = n1;
    
    n2 = 90;
    
    //数组在默认情况下是引用传递，赋的值是地址，赋值方式为引用赋值
    //是一个地址，arr2变化会影响到arr1
    int[] arr1 = {1,2,3};
    int[] arr2 = arr1;
    arr2[0] = 10;
    
    //arr1的值
    for(int i = 0;i < arr.length;i++){
      System.out.println(arr1[i]);
    }
    
    
  }
}
```

![截屏2022-09-14 19.41.03](/Users/minwenrui/Desktop/截屏2022-09-14 19.41.03.png)

数组的拷贝

```java
public class ArrayCopy{
  public static void main(String[] args){
   //将int[] arr1 = {10,20,30}拷贝到arr2数组，
   //要求数据空间是独立的
    
    int [] arr1 = {10,20,30};
    
    //创建一个新的数组arr2,开辟一个新的数据空间
    
    int[] arr2 = new int[arr1.length];
    //遍历arr1,把每个元素拷贝到对应元素的位置
    for(int i = 0;i < arr1.length;i++){
      arr2[i] = arr1[i];
    }
    arr2[0] = 100;
    
    System.out.println("arr1的元素");
    for(int i = 0;i < arr1.length;i++){
      System.out.println(arr1[i]);//10,20,30
    }
    
    System.out.println("arr2的元素");
    for(int i = 0;i < arr2.length;i++){
      System.out.println(arr2[i]);//100,20,30
    }
  }
}
```

数组反转

把数组的内容反转

```java
public class ArrayReverse{
  public static void main(String[] args){
   int[] arr = {11,22,33,44,55,66};
    //arr[0]和arr[5]进行交换
    //以此类推
    //一共需要交换3次=arr.length/2
    //每次交换时对应的下标是arr[i] arr[arr.length-1-i]
    //代码
    int temp = 0;
    int len = arr.length;
    for( int i = 0;i < arr.length / 2;i++){
     temp = arr[arr.length -1- i];
      arr[len -1 -i] = arr[i];
      arr[i] = temp;
    }
    System.out.println("输出反转后数组");
    for(int i = 0;i < arr.length;i++){
      System.out.println(arr[i])
    }
  }
}
```

```java
public class ArrayReverse{
  public static void main(String[] args){
    int[] arr = {11,22,33,44,55,66};
     //创建一个相同大小新的数组arr2
     //逆序遍历arr1，将每个元素拷贝到arr2的元素中(顺序拷贝)
    
    int [] arrr2 = new int[arrlength];
    //逆序遍历 arr 增加一个循环变量
    for(int i = arr.length -1,j=0;i >= 0;i--,j++){
      arr2[j] = arr[i];
    }
    //当for循环结束，arr2就是一个逆序数组{66,55,44,33,22,11}
    //让arr指向arr2数据空间时，此时arr原来的数据空间就没有变量引用，会被当作垃圾销毁
    arr = arr2;
    
    //shuchu
    for(int i = 0;i < arr.length;i++){
      System.out.println(arr[i]);
    }
  }
}
```

数组添加（扩容）

```java
import java.util.Scanner;
public class ArrayAdd{
  public static void main(String[] args){
    /*
    要求：实现动态的给数组添加元素效果，实现对数组的扩容
    1.原始数组使用静态分配 int[] arr = {1,2,3}
    2.增加元素4，直接放在数组的最后 arr = {1,2,3,4}
    3.用户可以通过如下方法决定是否继续添加，添加成功，是否继续
    
    定义初始数组 int[] arr ={1,2,3}
    
    */
    Scanner myscanner = new Scanner(System.in);
    int[] arr = {1,2,3};
    do{
      
      int[] arrNew = new int[arr.length + 1];
      for(int i = 0;i < arr.length;i++){//遍历arr数组，依次将arr元素拷贝到arr数组
      arrNew[i] =arr[i];
      
      }
      System.out.println("请输入要添加的元素");
      int addnum = myscanner.nextInt();
      //把4赋给新数组的最后一元素
      arrNew[arrNew.length - 1] = addnum;
      //让arr指向arrnew
      arr = arrNew;
      //shuchu
      System.out.println("arr扩容后的情况");
      for(int i = 0;i < arr.length;i++){
        System.out.print(arr[i] + "\t");
      }
      System.out.println("是否继续添加 y/n");
      char key = myscanner.next().charAt(0);
      if( key == 'n'){
        break;
      }
    }while(true);
    System.out.println("退出");
  
}
}
```

数组缩减

```java
import java.util.Scanner;
public class ArrayReduce{
  public static void main(String[] args){
    /*
    
    */
    Scanner myscanner = new Scanner(System.in);
    int[] arr = {1,2,3,4,5};
    do{
      
      int[] arrNew = new int[arr.length - 1];
      for(int i = 0;i < arr.length -1;i++){//遍历arr数组，依次将arr元素拷贝到arr数组
      arrNew[i] =arr[i];
      
      }
      System.out.println("请输入要缩减的元素");
      int Reducenum = myscanner.nextInt();
      //把4赋给新数组的最后一元素
      arrNew[arrNew.length - 1] = Reducenum;
      //让arr指向arrnew
      arr = arrNew;
      //shuchu
      System.out.println("arr扩容后的情况");
      for(int i = 0;i < arr.length;i++){
        System.out.print(arr[i] + "\t");
      }
      System.out.println("是否继续缩减 y/n");
      char key = myscanner.next().charAt(0);
      if( arr.length < 2){
        break;
      }
      System.out.println("不能再缩减")
    }while(true);
    System.out.println("退出");
  
}
}
```

## 排序

排序是将多个数据，依指定的顺序进行排列的过程

排序的分类：

1.内部排序：

指将需要处理的所有数据都加载到内部存储器中进行排列。包括（交换式排序法，选择式排序法和插入式排序法）

2.外部排序法

数据量过大，无法全部都加载到内存中，需要借助外部存储进行排序包括（合并式排序和直接合并式排序）

**冒泡排序(Bubble Sorting)**

基本思想：通过对待排序序列从后向前（下标较大的元素开始），依次比较相邻元素的值，若发现逆序则交换，使值较大的元素逐渐从前移向后部，就像水底下的气泡逐渐向上冒。

<img src="/Users/m/Desktop/截屏2022-09-16 18.06.51.png" alt="截屏2022-09-16 18.06.51" style="zoom:50%;" />

```java
public class BubbleSort{
  public static void main(String[] args){
    int[] arr = {24,69,80,57,13};
    int temp = 0;
    for(int j = 0;j < 4;j++){//四次比较
      if(arr[j] > arr[j + 1]){
        temp = arr[j];
        arr[j] = arr[j + 1];
        arr[j + 1] = temp;
      }
      
    }
    System.out.println("第一轮");
    for(int j = 0;j < arr.length;j++){
      System.out.print(arr[j] + "\t");
    }
    for(int j = 0;j < 3;j++){//三次比较
      if(arr[j] > arr[j + 1]){
        temp = arr[j];
        arr[j] = arr[j + 1];
        arr[j + 1] = temp;
      }
      
    }
    System.out.println("\n第二轮");
    for(int j = 0;j < arr.length;j++){
      System.out.print(arr[j] + "\t");
    }
    for(int j = 0;j < 2;j++){//二次比较
      if(arr[j] > arr[j + 1]){
        temp = arr[j];
        arr[j] = arr[j + 1];
        arr[j + 1] = temp;
      }
      
    }
    System.out.println("\n第三轮");
    for(int j = 0;j < arr.length;j++){
      System.out.print(arr[j] + "\t");
    }
    for(int j = 0;j < 1;j++){//一次比较
      if(arr[j] > arr[j + 1]){
        temp = arr[j];
        arr[j] = arr[j + 1];
        arr[j + 1] = temp;
      }
      
    }
    System.out.println("\n第四轮");
    for(int j = 0;j < arr.length;j++){
      System.out.print(arr[j] + "\t");
    }
   
  
  }
}
```

```java
public class BubbleSort{
  public static void main(String[] args){
    int[] arr = {24,69,80,57,13};
    int temp = 0;//用于交换的辅助变量
    for(int i = 0;i < arr.length - 1;i++){//多轮排序使用外层循环包起来即可
       for(int j = 0;j < arr.length - 1 - i;j++){//四次比较
        if(arr[j] > arr[j + 1]){//如果前面的数大于后面的数就交换
          temp = arr[j];
          arr[j] = arr[j + 1];
          arr[j + 1] = temp;
        }
      
    }
    System.out.println("\n第" + (i + 1) + "轮");
    for(int j = 0;j < arr.length;j++){
      System.out.print(arr[j] + "\t");
    }
      
    }
    }
}
```

总结冒泡排序特点

1.共有5个元素

2.一共进行4轮排列。可以看成外层循环

3.每一轮排序可以确定一个数的位置，比如第一轮排序确定最大数，与此类推

4.当进行比较时如果前面的数大于后面的数就交换

5.每轮比较在减少4 3 2 1

## 查找

在java中，常用的查找有两种

1.顺序查找

```java
import java.util.Scanner;
public class SeqSearch{
  public static void main(String[] args){
    /*
    有一个数列白 金 紫 青猜数游戏
    从键盘任意输入一个名称，判断数列中是否包含此名称
    要求：如果找到了就提示找到，并给出下标
    
    1.定义一个字符串数组
    2.接受用户输入，遍历数组，逐一比较
    */
    
    String[] names = {"白","金","紫","青"};
    Scanner myScanner = new Scanner(System.in);
    
    System.out.println("请输入名字");
    String findName = myScanner.next();
   
    int index = -1;//插入索引 看i是否循环
    for(int i = 0;i < names.length;i++){
      //比较字符串 ，如果找到名字就是当前元素
      if(findName.equals(names[i])){
        System.out.println("恭喜你找到" + findName);
        System.out.println("下标为=" + i);
        index = i;//把i保存到index
        break;
      }
    }
    
    if(index == -1){
      System.out.println("没有找到");
    }
    
    
    
  }
}
```

2.二分查找

## 多维数组（DimensionalArray）

二维数组

例如开发一个五子棋游戏，棋盘需要二维数组表示

```java
public class SeqSearch{
  public static void main(String[] args){
      /*请用二维数组输出如下图形
         0 0 0 0 0 0
         0 0 1 0 0 0
         0 2 0 3 0 0
         0 0 0 0 0 0
         */
int [][] arr = { {0, 0, 0, 0, 0, 0},
                 {0, 0, 1, 0, 0, 0},
                 {0, 2, 0, 3, 0, 0},
                 {0, 0, 0, 0, 0, 0} };
      //原来一维数组的每个元素是一个一维数组
      System.out.pritnln("二维数组的元素个数" + arr.length);
      //如果需要访问第（i+ 1）个一维数组的 第J + 1个值 arr[i][j];(从0开始编号)
      System.out.println("第3个一维数组第四个值" + arr[2][3]);
      
      //输出图形
      
      for(int i = 0;i < arr.length;i++){//遍历二维数组的每个元素
          for(int j = 0;j < arr[i].length;j++){
              System.out.print(arr[i][j] + " ");//输出一维数组
          }
          System.out.println();
        }
   }
}
```

动态初始化

1）语法：类型[] []数组名 = new类型[大小] [大小]

int a[][] = new int[2] [3]

2）二维数组在内存中存在的形式

```java
public class SeqSearch{
  public static void main(String[] args){
     int arr[][] = new int[2][3];
      int arr[][];
      arr = new int[2][3];
      
      
      for(int i = 0;i < arr.length;i++){
          for(int j = 0;j < arr[i].length;j++){
              System.out.print(arr[i][j] + " ");
          }
          System.out.println();
      }
  }
}
```

<img src="/Users/m/Desktop/截屏2022-09-21 17.24.51.png" alt="截屏2022-09-21 17.24.51" style="zoom: 50%;" />

动态初始化使用方式3-列数不确定

```java
public class SeqSearch{
  public static void main(String[] args){
      /*
      共有三个一维数组，每个一维数组的元素都是不确定的
      */
      int[][] arr = new int[3][];//创建二维数组，还没开空间
      for(int i = 0;i < arr.length;i++){
          arr[i] = new int[i + 1];//给每个元素开空间
          //遍历一维数组，给每个元素赋值
          for(int j = 0; j < arr[i].length;j++){
              arr[i][j] = i + 1;//赋值
          }
      }
      //遍历arr输出
      for(int i = 0;i < arr.length;i++){
         for(int j = 0;j < arr[i].length;j++){
             System.out.print(arr[i][j] + " ");
         }
         System.out.println();
      }
  }
}
```

遍历二维数组

```java
public class SeqSearch{
  public static void main(String[] args){
      /*
      遍历二维数组，并将各个值累计到int sum
      */
      
      int arr[][] = {{4,6},{1,4,5,7},{-2}};
      int sum = 0;
      for(int i  = 0;i < arr.length;i++){
          for(int j = 0;j < arr[i].length;j++){
              sum  = sum + arr[i][j]
          }
      }
      System.out.println("sum" + sum);
  }
}
```

二维数组打印杨辉三角

```java
public class YangHui{
  public static void main(String[] args){
      /*
      前提：每行端点与结尾的数为1.
（与上图中的n不同，这里第一行定义为n=1）
1.每个数等于它上方两数之和。
2.每行数字左右对称，由1开始逐渐变大。
3.第n行的数字有n项。
4.前n行共[(1+n)n]/2 个数。
5.第n行的m个数可表示为 C(n-1，m-1)，即为从n-1个不同元素中取m-1个元素的组合数。
6.第n行的第m个数和第n-m+1个数相等 ，为组合数性质之一。
7.每个数字等于上一行的左右两个数字之和。可用此性质写出整个杨辉三角。即第n+1行的第i个数等于第n行的第i-1个数和第i个数之和，这也是组合数的性质之一。即 C(n+1,i)=C(n,i)+C(n,i-1)。
8.(a+b)n的展开式中的各项系数依次对应杨辉三角的第(n+1)行中的每一项。
      
      */
      int[][] yanghui = new int[10][];
      for(int i = 0;i < yanghui.length;i++){//遍历杨辉的一维元素
          //给每个一维数组开辟空间
          yanghui[i] = new int[i + 1];
          //给每个一维数组赋值
          for(int j = 0;j < yanghui[i].length;j++){
              //每一行第一个和最后一个元素都是1
              if(j == 0||j == yanghui[i].length - 1){
                  yanghui[i][j] = 1;
              }else{
                  yanghui[i][j] = yanghui[i-1][j] + yanghui[i-1][j-1];
              }
          }
          
      }
      //输出杨辉三角
      for(int i = 0;i < yanghui.length;i++){
          for(int j = 0;j < yanghui[i].length;j++){
              System.out.print(yanghui[i][j] + "\t");
          }
          System.out.println();
      }
      
  }
}
```

二维数组使用细节

1.一维数组的声明方式: int[] x或者int x[]

2.二维数组声明:int []  [] y int[] y [] int y[] []

3.二维数组实际上由多个一维数组组成，它的各个一维数组的长度可以相同，也可以不同

map[] [] = {{1,2},{3,4,5}},列数不等的二维数组

```java
public class H4{
  public static void main(String[] args){
      /*
      已知有一个升序数组，要求插入一个元素，该数组顺序依然是是升序
      
      1.先确定添加的数插入那个索引
      2.扩容
      */
      
      //先定义原数组
      int[] arr = {10,12,45,90};
      int insertNum = 23;
      int index = -1;
      //遍历arr数组，如果insertNum <= arr[i],说明i就是插入位置
      //使用index 保留 index = i;
      //若遍历完成不成立 index = arr.length 即最后
      
      for(int i = 0;i < arr.length;i++){
          if(insertNum <= arr[i]){
              index = i;
              break;
          }
      }
      //判断index值
      if(index ==  -1){
          index = arr.length
      }
      System.out.println("index =" + index);
      //扩容
      int[] arrNew = new int[arr.length + 1];
      //将arr元素拷贝到arrNew
      
      for(int i = 0,j = 0;i < arrNew.length;i++){
          if(i != index){
              arrNew[i] = arr[j];
              j++;
          }else{
              arrNew[i] = insertNum;
          }
      }
      //让arr指向arrNew，原来的数组成为垃圾被销毁
      arr = arrNew;
      
      System.out.println("输出新数组");
      for(int i = 0;i < arr.length;i++){
          System.out.println(arr[i] + "\t");
      }
     
  }
}
```

```java
/**
*@Author:Bill.Min
*/
public class H5{
  public static void main(String[] args){
     //随机生成10个整数（1-100）保存到数组，并倒序打印以及求平均值，最大值及其下标，并查找里面是否有8
      int[] arr = new int[10];
      
      for(int i = 0;i < arr.length;i++){
          arr[i] = (int)(Math.random() * 100) + 1;
      }
      System.out.println("元素");
      for(int i = 0;i < arr.length;i++){
          System.out.println(arr[i] + "\t");
      }
      for(int i = arr.length - 1;i >= 0;i--){
          System.out.println(arr[i] + "\t");
      }
      
      //平均值，求最大值和最大值下标
      double sum = 0;
      int max = arr[0];
      int maxIndex = 0;
      for(int i = 1;i < arr.length;i++){
          
          sum += arr[i];
          if(max < arr[i]){
              max = arr[i];
              maxIndex = i;
          }
          
      }
      System.out.println("max =" + max + "maxIndex =" + maxIndex);
      System.out.println("average" + (sum / arr.length));
      
      //查找8
      int findNum = 8;
      int index = -1;
      for(int i = 0;i < arr.length;i++){
          if(findNum == arr[i]){
              System.out.println("找到" + findNum + "下标" + i);
              index = i;
              break;
          }
      }
      if(index == -1){
          System.out.println("没有找到");
      }
  }
}
```

```java
public class BubbleSort{
  public static void main(String[] args){
      //冒泡排序
    int[] arr = {24,69,80,57,13};
    int temp = 0;//用于交换的辅助变量
    for(int i = 0;i < arr.length - 1;i++){//多轮排序使用外层循环包起来即可
       for(int j = 0;j < arr.length - 1 - i;j++){//四次比较
        if(arr[j] > arr[j + 1]){//如果前面的数大于后面的数就交换
          temp = arr[j];
          arr[j] = arr[j + 1];
          arr[j + 1] = temp;
        }
      
    }
    System.out.println("\n第" + (i + 1) + "轮");
    for(int j = 0;j < arr.length;j++){
      System.out.print(arr[j] + "\t");
    }
      
    }
    }
}
```

# 面向对象

## 类与对象

```java
public class object{
  public static void main(String[] args){
      //单独变量解决
      String catName1 = "白ちゃん";
      int catAge1 = 3;
      String catColor1 = "白い";
          
      String catName2 = "花ちゃん";
      int catAge2 = 100;
      String catColor2 = "赤い";
      
      //数组 数据类型无法体现 下标获取信息 造成变量名字内容对应关系不明确
      String[] cat1 = {"白ちゃん","白い","3"};
      String[] cat2 = {"花ちゃん","赤い","100"};
      
      //使用oop面向对象解决
      //实例化一只猫
      //cat1就是对象
      Cat cat1 = new Cat();//创建一只猫；把创建的猫赋给cat1
      cat1.name = "白ちゃん";
      cat1.age = "3";
      cat1.color = "白い";
      Cat cat2 = new Cat();//创建一只猫；把创建的猫赋给cat２
      cat2.name = "花ちゃん"
      cat2.age = "100";
      cat2.color = "赤い";
      
      //访问对象属性
      System.out.pritnln("白ちゃんの情報" + cat1.name + cat1.age + cat1.color);
      System.out.pritnln("花ちゃん" + cat2.name + cat2.age + cat2.color);
      
          
    }
}
 //面向对象
      //定义一个猫类Cat -> 自定义数据类型
      class Cat{
          //属性
          String name;//名字
          int age;//年龄
          String color;//颜色
          //行为
      }
```

**对象在内存中的存在形式**

![截屏2022-09-27 14.26.21](assets/%E6%88%AA%E5%B1%8F2022-09-27%2014.26.21.png)

属性/成员变量

1.成员变量 = 属性 = field

2.属性是类的一个组成部分，一般是基本数据类型，也可以是引用类型(对象，数组)

属性注意细节

```java
public class PropertiesDetail{
  public static void main(String[] args){
      //创建person对象
      //p1是对象名（对象引用）
      //new Person()创建的对象空间是真正对象
      Person p1 = new Person();
      
      //对象的属性如果不赋值，遵守数组规则：
      //int 0,short 0,byte 0,long 0,float 0.0,double 0.0,char \u000,boolean null
      System.out.println("\n当前这个人的信息");
      System.out.println("age" + p1.age + "name" + p1.name 
                         + "sal=" + p1.sal + "isPass" + p1.isPass);
      
          
    }
}
class Person{
    int age;
    String name;
    double sal;
    boolean isPass;
} 
```

**类与对象内存分配机制**

1.栈：一般存放基本数据类型(局部变量)

2.堆：存放对象(数组等)

3.方法区：常量池(字符串等)，类的加载信息

```java
public class object3{
  public static void main(String[] args){
      
      Person p1 = new Person();
      p1.age = 10;
      p1.name = "亀田";
      Person p2 = p1;
      p1.age = 80;
      System.out.println(p2.age);//80
    }
}
class Person{
    int age;
    String name;
    
} 
```

![截屏2022-09-27 14.26.21](assets/%E6%88%AA%E5%B1%8F2022-09-27%2014.26.21.png)

对象创建流程

1.先加载person类信息

2.在堆中分配空间，进行默认初始化，

3.把地址赋给p，p指向对象

4.进行指定初始化 

## 成员方法传参机制

在某些情况下，我们需要定义成员方法。比如人类除了一些属性以外还有一些行为，定义这些行为需要用到成员方法才能完成。

```java
public class Method{
  public static void main(String[] args){
      //方法调用，不调用不输出
      //先创建对象，后调用
      Person p1 = new Person();
      p1.speak();//调用方法
    
    }
}
class Person{
    String name;
    int age;
    //方法
    //添加speak 成员方法，输出"良良い人ね”
    /*
    public表示方法公开
    void表示方法没有返回值
    speak():speak方法名 ()形参列表
    {}方法体写要执行的代码
    
    */
    public void speak(){
        System.out.println("良い人ね");
    }
    
} 
```























重载

可变参数

作用域

构造器

this







