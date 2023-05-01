# 知的ソフトウエア創成　Kameda Lab
# Java概述
学习笔记部分摘录自韩顺平JAVA课程笔记

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

# 面向对象(object oriented)

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

### 属性/成员变量

1.成员变量 = 属性 = field =字段

2.属性是类的一个组成部分，一般是基本数据类型，也可以是引用类型(对象，数组)

### 属性注意细节

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

### 创建对象的访问属性

1.先声明后创建

2.直接创建 Cat cat = newCat();

### **类与对象内存分配机制**

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

###对象创建流程

1.先加载person类信息

2.在堆中分配空间，进行默认初始化，

3.把地址赋给p，p指向对象

4.进行指定初始化 

##成员方法

###成员方法

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

###方法的调用机制

1.当程序执行到方法时，就会开辟一个独立的空间（栈）

2.当方法执行完毕，或者执行到return语句时，就会返回

3.返回到调用方法的地方

4.返回后，继续执行方法后面的代码

5.当main方法(栈)执行完毕后，整个程序退出

<img src="assets/%E6%88%AA%E5%B1%8F2022-09-29%2013.37.46.png" alt="截屏2022-09-29 13.37.46" style="zoom:50%;" />

###方法的妙用

```java
public class Method02{
  public static void main(String[] args){
      
      //请遍历一个数组，输出数组的各个元素值
      int [][] map = {{0,0,1},{1,1,1},{1,1,3}};
      
      Mytools tool = new Mytools();//创建tool对象
      
      //遍历map数组
     /* for(int i = 0;i < map.length;i++){
          for(int j = 0;j < map[i].length;j++){
              System.out.pritnln(map[i][j] + "");
          }
          System.out.println();
      }
      */
      tool.printArr(map);
      //当要求再次遍历时
      /*for(int i = 0;i < map.length;i++){
          for(int j = 0;j < map[i].length;j++){
              System.out.pritnln(map[i][j] + "");
          }
          System.out.println();
      }*/
      tool.printArr(map);
      
    }    
} 
//把输出的功能，写到一个类的方法中，调用即可
class Mytools{
    //
    public void printArr(int[][] map){
        System.out.println("======")
        for(int i = 0;i < map.length;i++){
          for(int j = 0;j < map[i].length;j++){
              System.out.pritnln(map[i][j] + "\t");
          }
          System.out.println();
      }
    }
}
/*
提高代码的复用性
可以将实现的细节封装起来，然后供其他用户来调用即可
得以关注业务逻辑
*/
```

###成员方法的定义

```java
public(访问修饰符) 返回数据类型 方法名 (形参列表) {//方法体
   语句;
   return 返回值;
}
1.形参列表：表示成员方法的输入 call(int n),getSum(int num1,int num2)
2.返回数据类型：表示成员方法的输出，void代表没有返回值
3.方法主体：实现功能的代码块
4.return语句不是必须的
```

###方法使用细节

####**访问修饰符**

(作用时控制 方法使用的范围)可不写【有四种：public，protected，默认，private】

返回数据类型

1.一个方法最多有一个返回值，如果有多个返回值则返回数组

2.返回类型可以为任意类型，包括基本类型或引用类型（数组，对象）

```java
public class MethodDetail{
  public static void main(String[] args){
      //1.一个方法最多有一个返回值
      AA a = new AA();
      int[] res = a.getSumAndSub(1,4);
      System.out.pritnln("和" + res[0]);
      System.out.pritnln("差" + res[1]);
    }
}
class AA{
    public int[] getSumAndSub(int n1,int n2){
        
        int[] resArr = new int[2];//创建一个数组
        resArr[0] = n1 + n2;
        resArr[1] = n1 - n2;
        return resArr;
    }
    
    //3.如果方法要求有返回数据类型，则方法体中最后的执行语句必须为return值；
    //而且要求返回值类型必须和return的值类型一致或兼容
    
    public double f1() {
        double d1 = 1.1 * 3;
        int n = 100;
        return n;//int -> double ok 兼容
    }
    //如果方法时void，则方法中可以没有return语句，或者只写return
    //关于方法名：符合驼峰命名法，见名知义
    public void f2() {
        System.out.println("hello1");
        System.out.println("hello1");
        int n = 10;
        return;//可不写
    }
}
```

####**形参列表**

1.一个方法可以有0个参数，也可以有多个参数，中间用逗号间隔 getSum(int n1,int n2)

2.参数类型可以为任意类型，包含基本类型或引用类型，比如printArr（int [] [] map)

3.调用带参数的方法时，一定对应着参数列表传入相同类型或兼容类型的参数

4.方法定义时的参数称为形式参数，简称形参；方法调用时传入的参数称为实际参数，简称实参

实参和形参的类型要一致或兼容。个数和顺序必须一致。

####方法体

里面写完成功的具体语句，可以为输入，输出，变量，运算，分支，循环，方法调用，但里面不能再定义方法；即方法不能嵌套定义

####方法调用细节

1.同一个类中的方法调用：直接调用即可。比如print(参数)；

```java
public class MethodDetail02{
    public static void main(String[] args){
        A a = new A();
        a.sayok();
        a.m1();
    }
}
class A{
    
    public void print(int n){
        System.out.println("print()方法调用 n =" + n);
    }
    public void sayok(){
        print(10);
        System.out.println("继续执行");
    }
    //跨类中的方法A调用B类方法：需要通过对象名调用
    public void m1(){
        //创建B对象,然后再调用方法即可
        System.out.println("m1() 方法被调用")
        B b = new B();
        b.hi();
        
        System.out.println("m1方法继续执行");
    }
}
class B {
    public void hi(){
        System.out.println("B类中的 hi()被执行");
    }
}
```

2.跨类中的方法A调用B类方法：需要通过对象名调用。比如对象名。方法名(参数)

3.特别说明：跨类的方法调用和方法修饰符相关。

###方法练习

类定义：待完善

```java
public class MethodExercise01{
    public static void main(String[] args){
      AA  a = new AA();
        if (a.isOdd(1)){//多用这个语法
            System.out.println("是一个奇数");
        }else{
            System.out.println("是一个偶数");
        }
        a.print(4,4,&);
        
    }
}
//编写一个类AA，有一个方法：判断一个数是奇数ood还是偶数，返回boolean
class AA{
    //1.方法的返回类型 boolean
    //2.方法的名字 isOdd
    //3.方法的形参
    //4.方法体，判断
    
    public boolean isOdd(int num){
        if(num % 2 != 0){
            return true;
        }else{
            return false;
        }
        
        //return  num % 2 != 0 ? true;false;
        
        //return num % 2 != 0;
    }
    
    //根据行列字符打印 对应行数和列数 的字符
    //比如 行4 列4 字符#打印对应效果
    
    //思路
    //1.方法的返回类型 void
    //2.方法的名字 print
    //3.方法的形参（int row,int col,char c)
    //4.方法体，判断
    public void print(int row,int col,char c){
        for(int i = 0;i < row;i++){//输出每一行
            for(int j = 0;j < col;j++){
                System.out.print(c);
            }
            System.out.println();
        }
    }

 **成员方法的传参机制**
```

## **成员方法的传参机制**

###基本数据类型的传参机制

```java
public class MethodParameter{
    public static void main(String[] args){
        int a = 10;
        int b = 20;
        
        AA obj = new AA();//创建AA对象 obj
        a.swap(a,b);//调用swap方法
        
        System.out.println("a =" + a + "b =" + b);//？
      
    }
}
class AA{
    
    public void swap(int a,int b){
        
        System.out.pritnln("\na和b交换前的值\na =" + a + "\tb =" + b);
        //完成了a与b的交换
        int tmp = a;
        a = b;
        b = tmp;
        System.out.pritnln("\na和b交换后的值\na =" + a + "\tb =" + b);
    }
}
//基本数据类型，传递的是值拷贝，形参的任何变化不影响实参
```

###引用数据类型的传参机制

```java
public class MethodParameter02{
    public static void main(String[] args){
        
        B b = new B();
        int[] arr = {1,2,3};
        b.test100(arr);//调用方法在内存中产生新的栈
        System.ut.println("main方法的数组")
        for(int i = 0;i < arr.length;i++){
            System.out.print(arr[i] + "\t");
        }
        System.out.println();
        
        //
        Person p = new Person();
        p.name = "jack";
        p.age = 10;
        
        b.test200(p);
        System.out.println("main的p.age" + p.age);//10
    }
}
class Person{
    String name;
    int age;
}
class B{
    //B类中编写一个方法test100
    //可以接收一个数组，在方法中修改该数组，原来数组是否变化
    public void test200(Person p){
        //p.age = 10000;//修改对象属性
        //p = null;
        p = new Person();
        p.name = "tom";
        p.age = 99;
        
    }
    
    public void test100(int[] arr){
        arr[0] = 200;//修改元素
        //遍历数组
        System.out.println("test100数组");
        for(int i = 0;i < arr.length;i++){
            System.out.print(arr[i] + "\t");
        }
        System.out.println();
    }
   
}
//引用类型传递的是地址，可以通过形参影响实参

```

###克隆对象

```java
public class MethodParameter02{
    public static void main(String[] args){
       Person p = new Person();
       p.name = "min";
       p.age = 100;
       
        MyTools tools  = new MyTools();
        Person p2 = tools.copyPerson(p);
        
        System.out.println("p的属性 age=" + p.age+ "名字 =" + p.name);
        System.out.println("p2的属性 age=" + p2.age+ "名字 =" + p2.name);
        //同对象比较
        System.out.println(p == p2);//false
       
    }
}
class Person{
    String name;
    int age;
}
class MyTools{
    //编写一个方法copyPerson，可以复制一个Person对象，返回复制的对象。克隆对象
    //注意要求得到新对象和原来对象是两个独立的对象，只是属性相同
    
    //1.方法的返回类型 Person
    //2.方法的名字 copyPerson
    //3.方法的形参（Person p)
    //4.方法体 创建一个新对象，并复制属性返回即可
    
    public Person copyPerson(Person p){
        //创建一个新对象
        Person p2 = new Person();
        p2.name = p.name;
        p2.age = p.age;
        
        return p2;
    }
}
```

##方法递归调用

递归就是自己调用自己，每次调用时传入不同的变量。递归有助于解决复杂问题，同时使代码简洁。

(自认为是方法调用的嵌套)

```java
public class Recursion01{
    public static void main(String[] args){
       T  t1 = new T();
       t1.test(4);//
       int res = t1.factorial(5);
        System.out.println("res =" + res);
    }
}

class T{
    //分析
    public void test(int n){
        if (n > 2){
            test(n - 1);
        }else{
        System.out.println("n=" + n);//2,3,4
        }
    }
    public int factorial(int n){//阶层
        if(n == 1){
            return 1;
        }else{
            return factorial(n - 1) * n;
        }
    }
}
```

<img src="assets/%E6%88%AA%E5%B1%8F2022-09-30%2017.35.53.png" alt="截屏2022-09-30 17.35.53" style="zoom: 67%;" />

###递归的重要规则

1.执行一个方法时，就创建一个新的受保护的独立空间（栈空间）

2.方法的局部变量是独立的，不会相互影响，比如n变量

3.如果方法中使用的是引用数据类型（比如数组对象），就会共享该引用类型的数据

4.递归必须向退出递归的条件逼近，否则就是无限递归，出现StackoverflowError，死🐢了

5.当一个方法执行完毕，或者遇到return，就会返回，遵守谁调用，就将结果返回给谁，同时当方法执行完毕或者返回时，该方法也就执行完毕。

###递归斐波那契与猴子吃桃

```java
public class RecursionExercise01{
    public static void main(String[] args){
       T t1 = new T();
       int n = -1;
       int res = t1.fibonacci(n);
       if(res != -1){
       System.out.println("当n ="+ n + "对应的斐波那契数"  + res);
       }else{
           System.out.println("请输入大于等于1的数" );
       }
       //桃
       int day = 1;
       int peachNum = t1.peach(day);
       if(peachNum != -1){
           System.out.println("第" + day + "天有" + peachNum + "个桃子" );
       }
    }
}
class T{
    /*
    请用递归的方式求出斐波那契数1，1，2，3，5，8，13.。。。给一个整数n，求出n对应的fobionacci数是多少
    
    1. 当n = 1 斐波那契数 1
    2. 当n = 2 斐波那契数 1
    3. 当n >= 3 斐波那契数 前两数的和
    4. 递归
    */
    public int fibonacci(int n) {
        if(n >= 1){
           if(n == 1|| n == 2){
                return 1;
            }else{
                return fibonacci(n - 1) + fibonacci(n - 2);
            }
        }else{
            System.out.println("要求输入 n >= 1的整数");
            return -1;
        }
    }
    /*
    猴子吃桃问题：有一堆桃子猴子第一天吃其中的一半，并再多吃了一个
    以后每天以此类推。当到第十天时，想再吃发现只剩一个。问最初有多少个桃子
    
    1.day = 10，有1个
    2.day = 9，有 (day10 + 1) * 2 = 4
    3.day = 8，有 (day9 + 1) * 2 = 10
    4.递归
    */
    public int peach(int day){
        if (day == 10){
            return 1;
        }else if(day >= 1 && day <= 10){
            return (peach(day + 1) + 1) * 2;
        }else{
            System.out.println("输入天数在1-10");
            return -1;
        }
    }
}
```

###老鼠出迷宫

```java
public class MiGong{
    public static void main(String[] args){
       /*
       1.创建迷宫。用二维数组表示
       2.先规定map数组的元素值 0:可以走 1:障碍物
       */
       int [][] map = new int[8][7];
       //3.将最上和最下一行全设置为1
        for (int i = 0;i < 7;i++){
            map[0][i] = 1;
            map[7][i] = 1;
        }
        //4.将最右面的一列和最左面的一列设置为1
        for (int i = 0;i < 8;i++){
            map[i][0] = 1;
            map[i][6] = 1;
        }
        map[3][1] = 1;
        map[3][2] = 1;
        map[2][2] = 1;//测试回溯
        //map[2][1] = 1;
        //map[2][2] = 1;
        //map[1][2] = 1;
        //输出当前地图
        System.out.println("当前地图");
        for(int i = 0;i < map.length;i++){
            for(int j = 0;j < map[i].length;j++){
                System.out.print(map[i][j] + " ");
            }
            System.out.println();
        }
        T t1 = new T();
        t1.findWay2(map,1,1);
        
        System.out.println("\n找路的情况如下");
        
        for(int i = 0;i < map.length;i++){
            for(int j = 0;j < map[i].length;j++){
                System.out.print(map[i][j] + " ");
            }
            System.out.println();
        }
    }
}
class T{
    //使用递归回溯思想
    //1.findWay专门解决出迷宫
    //2.找到返回true 否则 False
    //3.map二维数组表示迷宫
    //4.i，j是老鼠位置，初始化位置（1，1）
    //5.因为递归找路，先规定map数组值的意义
    // 0表示可以走 1 表示障碍物 2表示可以走3 表示走过 是死路
    //6.map[6][5] = 2表示可以结束，否则继续
    //7.先确定老鼠找路的策略下 -》 右-〉上-》左
    
    public boolean findWay(int [][] map,int i,int j){
        
        if(map[6][5] == 2){//说明已经找到
            return true;
        }else{
            if(map[i][j] == 0){//当前位置是0可以走
                map[i][j] = 2;//假定可以走通
                //使用策略确定是否真的可以走通
                //下 右 上 左
                if(findWay(map,i + 1,j)){//下
                    return true;
                }else if(findWay(map,i,j + 1)){//右
                    return true;
                }else if(findWay(map,i-1,j)){//上
                    return true;
                }else if(findWay(map,i,j-1)){//左
                    return true;
                }else{
                    map[i][j] = 3;
                    return false;
                }
            }else{
                return false;
            }
        }
    }
    //修改走路策略，看路径是否变化
    //上右下左
    public boolean findWay2(int [][] map,int i,int j){
        
        if(map[6][5] == 2){//说明已经找到
            return true;
        }else{
            if(map[i][j] == 0){//当前位置是0可以走
                map[i][j] = 2;//假定可以走通
                //使用策略确定是否真的可以走通
                //下 右 上 左
                if(findWay2(map,i - 1,j)){//下
                    return true;
                }else if(findWay2(map,i,j + 1)){//右
                    return true;
                }else if(findWay2(map,i+1,j)){//上
                    return true;
                }else if(findWay2(map,i,j-1)){//左
                    return true;
                }else{
                    map[i][j] = 3;
                    return false;
                }
            }else{
                return false;
            }
        }
    }
    
}

//拓展：最短路径问题
//1.穷举法
//2.图 佛洛依德
```

###汉诺塔

```java
public class HanoiTower{
    public static void main(String[] args){
      Tower tower = new Tower();
      tower.move(5,'A','B','C');
    }
}
class Tower{
    //num表示要移动的个数
    public void move(int num,char a,char b,char c){//a,b,c,表示塔
        //如果只有一个盘
        if(num == 1){
            System.out.println(a + "->" + c);
        }else{
            //如果有多个盘，可以看成两个，最底下的盘和上面所有盘
            //1.先移动上面所有的盘到b 借助c
            move(num -1 ,a,c,b);
           System.out.println(a + "->" + c);
           //再把b塔所有的盘移动到c借助a
           move(num -1,b,a,c);
        }
    }
}


```

###八皇后

```java
public class HanoiTower{
    public static void main(String[] args){
     
    }
}
class Tower{
    
}



```

## 方法重载(overload)

java中允许同一个类中多个同名方法到存在，但要求形参列表不一致

比如：System.out.println();out是PrintStream类型 //字段 = 属性

###重载的好处

: 减轻了起名记名的麻烦

```java
public class OverLoad01{
    public static void main(String[] args){
      System.out.println(100);
      System.out.print("hello world");
      System.out.print('h');
      System.out.print(1.1);
      System.out.print(true);
     
    }
}
```

```java
public class OverLoad01{
    public static void main(String[] args){
       MyCalculator mc = new MyCalculator();
       System.out.println(mc.calculate(1,2));
       System.out.println(mc.calculate(1.1,2));
    }
}

class MyCalculator{
    //下面四个calculate方法构成了重载
    
    public int calculate(int n1,int n2){
        return n1 + n2;
    }
    
    public double calculte(int n1 ,double n2){
        return n1 + n2;
    }
    public double calculate(double n1,int n2){
        System.out.println("被调用")
        return n1 + n2;
    }
    public double calculate(int n1,int n2,int n3){
        return n1 + n2+ n3;
}
    
/*OverLoad的注意事项及细节
1.方法名必须相同
2.形参列表：必须不同（形参的类型个数与顺序，至少有一样不同，参数名无要求）
3.返回类型无要求
*/
```

###练习

```java
public class OverLoadExercise{
    public static void main(String[] args){
       Methods method = new Methods();
       method.m(10);//100
       mothod.m(10.10);
       method.m("皆んなさん、おはよう！");
       
       //
        System.out.println(method.max(10,24));//24
        System.out.println(method.max(10.0,24.0));//24.0
        System.out.println(method.max(10.0,24.0,89.0));//89.0
    }
}
/*
编写程序，类methods中定义三个重载方法并调用方法名为m
三个方法分别接收一个int参数，一个字符串参数。分别执行平方运算并输出结果
相乘并输出结果，输出字符串信息。在主类mian（）方法中分别用参数区别调用三个方法
*/
class Methods{
   /*
   定义三个重载方法max(),第一个方法，返回两个int中的最大值
   第二个方法，返回两个double中的最大值
   第三个方法，返回三个double中的最大值，并分别调用三个方法
   */
    public int max(int n1,int n2){
        return n1 > n2?n1 : n2;
    }
    public double max(double n1,double n2){
        return n1 > n2?n1 : n2;
    }
    public double max(double n1,double n2,double n3){
        double max1 = n1 > n2 ? n1 : n2;
        return max1 > n3 ? max1 : n3;
    }
    public void m(int n){
        System.out.println("平方和"  + (n*n));
    }
    
    public void m(int n1,int n2){
        System.out.println("相乘"  + (n1*n2));
    }
    public void m(String str){
        System.out.println("传入str="  + str);
    }
}    
```

## 可变参数

java允许将同一个类中多个同名同功能但参数个数不同的方法，封装成一个方法。就可以通过可变参数来实现。

###基本语法

访问修饰符 返回类型 方法名（数据类型...形参名）{

}

```java
public class VarParameter01{
    public static void main(String[] args){
       HspMethod m = new HspMethod();
       System.out.println(m.sum(1,5,100));
    }
}
class HspMethod{
    public int sum(int n1,int n2){
        return n1 + n2;
    }
    
    //将三个方法名相同，功能相同，参数个数不同 使用可变参数优化
    //1.int ...表示接受的是可变参数，类型是int，即可以接受多个int
    //2.使用可变参数时，可以当作数组来使用，即nums可以当作数组
    //3.遍历nums求和即可
    public int sum(int...nums){
        //System.out.pritnln("接收参数个数"  + nums.lenght);
        int res = 0;
        for(int i = 0;i < nums.length;i++){
        res += nums[i];    
        }
        return res;
    }
}
/*
细节
1.可变参数的实参可以是0个或任意多个
2.可变参数的实参可以是数组
3.可变参数的本质就是数组

4.可变参数可以和普通类型的参数一起放在形参列表，但必须保证可变参数在最后
5.一个形参列表中只能出现一个可变参数
*/
public class VarParameterDetail{
    public static void main(String[] args){
       int[] arr = {1,2,3};//可变参数的实参可以是数组
       T t1 = new T();
       t1.f1(arr);
    }
}
class T{
    public void f1(int...nums){
        System.out.println("长度 =" + num.length);
        
        //可变参数可以和普通类型的参数一起放在形参列表，但必须保证可变参数在最后
     public void f2(String str,int...nums){
        System.out.println("长度 =" + num.length);
    }
}
```

###练习

```java
public class VarParameterExercise{
    public static void main(String[] args){
       HspMethod hm = new HspMethod();
       System.out.println(hm.showScore("みんさん",49,89));
       System.out.println(hm.showScore("みんさん",78,89.9,67,77,99));
    }
}
class HspMethod{
    /*
    有三个方法，分别实现返回姓名和两门课成绩
    返回姓名和三门课的成绩，返回姓名和五门课的成绩
    封装成一个可变参数的方法
    */
    public String showScore(String name,double...scores){
        double totalScore = 0;
        for(int i = 0;i < score.length;i++){
            totalScore += scores[i];
        }
        return name + "有" + score.length + "成绩" + totalScore;
    }
}
```

## **作用域**

###基本使用

1.在Java中，主要的变量就是属性（成员变量）和局部变量。

2.我们说的局部变量一般是指成员方法中定义的变量

3.Java中的作用域分类

全局变量：也就是属性，作用域作为整个类体

局部变量：除了属性之外的其他变量，作用域为定义它的代码块中

4.全局变量可以不赋值直接使用，因为他有默认值，局部变量必须赋值后才能使用

```java
public class VarScope{
    public static void main(String[] args){
       
    }
}
class Cat{
    //全局变量：也就是属性，作用域为整个类体 Cat类：cry eat等方法使用属性
    //属性在定义时可以直接赋值
    int age = 10;
    
    public void cry(){
        int n = 10;
        String name = "jack";
        System.out.println("在此方法中使用属性age" + age);
    }
    public void eat(){
        int n = 10;
        String name = "jack";
        System.out.println(age);
    }
}
```

###细节

```java
public class VarScopeDetail{
    public static void main(String[] args){
       Person p1 = new Person();
       p1.say();//局部的name 在调用执行结束后死亡
       //属性name仍然可以使用
        
       T t1 = new T();
       t1.test();
       t1.test2(p);
    }
}

class T{
    public void test(){//全局变量/属性：可以被本类使用，或其他类使用(通过对象调用)
        Person p1 = new Person();
        System.out.println(p1.name);//jack
    }
    public void test2(Person p){
        System.out.println(p.name);//jack
}
class Person{
    String name = "jack";
    //1.属性和局部变量可以重名，访问时遵循就近原则
    
    public void say(){
        String name = "king";
        System.out.println("say() name" + name);
    }
    //2.在同一个作用域中，比如在同一个成员方法中，两个局部变量不能重名
     public void hi(){
        String address = "beijing";
        String address = "shanghai";
    }
    //3.属性的生命周期较长，伴随着对象的创建而创建死亡而死亡。局部变量的生命周期较短，伴随代码块的执行创建，伴随代码块的结束而死亡。即在一次执行方法中
    
    /*4.作用域范围不同
     属性：可以被本类使用
     局部变量：只能在本类中的方法使用
    */
    
    //属性可以加修饰符
}
```

## 构造器（Constructor）

是类的一种特殊方法，主要作用是完成新对象的初始化

1）方法名与类名相同

2）没有返回值

3）在创建对象时，系统会自动调用该类的构造器完成对象的初始化

```java
[修饰符] 方法名(形参列表){
    方法体;
}
/*
构造器的修饰符可以默认
构造器没有返回值
方法名和类名必须一样
参数列表和成员方法一样的规则
构造器的调用由系统完成
*/
```

```java
public class Constructor01{
    public static void main(String[] args){
     //new 一个对象时，直接通过构造器指定名字与年龄
     Person p1 = new Person("亀田",62);
     System.out.println("p1对象" + p1.name + p1.age);//亀田　62
    }
}
class Person{
    String name;
    int age;
    //1.构造器无void，没有返回值
    //2.与类名相同
    //3.构造器的形参列表规则与成员方法相同
    public Person(String pNmae,int pAge){
        System.out.println("构造器被调用，完成对象属性的初始化");
        name = pName;
        age = pAge;
    }
}
```

```java
public class ConstructorDetail{
    public static void main(String[] args){
         Person p1 = new Person("亀田",62);
         Person p2 = new Person("亀田");
        //1.一个类可以定义多个不同的构造器，即构造器重载
        
        Dog d1 = new Dog();//使用的是默认的无参构造器
    }
}
class Dog{
    //如果程序员没有定义构造器，系统会自动给类生成一个默认的无参构造器
    //反编译工具javap指令 jdk提供的 对给定的class文件进行反编译
    /*
    Dog(){
    
    }
    */
    //
    public Dog(String dName){
        
    }
    Dog(){//显示定义之后才能用(继承)
    
    }
}
class Person{
    String name;
    int age;
    //第一个构造器
    public Person(String pNmae,int pAge){
        name = pName;
        age = pAge;
    }
    //第二个构造器 只指定人名
     public Person(String pNmae){
        name = pName;
    }
}
```

###练习

```java
public class ConstructorDetail{
    public static void main(String[] args){
        Person p1 = new Person();
         System.out.println("p1信息" + p1.name + p1.age);//name null 18
        
        Person p2 = new Person("kameda",62);
         System.out.println("p2信息" + p2.name + p2.age);
    }
}
/*
在前面定义的Person类中添加两个构造器
第一个无参构造器：设置所有人的age属性为18
第二个带pName和pAge两个参数：使得每次创建Person对象 的同时初始化对象的age属性值和name属性值
分别使用不同的构造器创建对象
*/
class Person{
    String name;
    int age;
    //第一个无参构造器：设置所有人的age属性为18
    public Person(){
        age = 18;
    }
    //第二个带pName和pAge两个参数
    public Person(String pName,int pAge){
        name = pName;
        age = pAge;
    }

```

##对象创建流程分析

```java
class Person{
    int age = 90:
    String name;
    Person(String n,int a){
        name = n;
        age = a;
    }
}
Person p = new Perosn("小倩"，20);
```

1.加载Person类信息(Person.class).只会加载一次

2.在堆中分配空间地址

3.完成对象初始化

1）默认初始化age =0 name = null

2）显示初始化age = 90 name = null

3）构造器初始化 age = 20 name = 小倩

4.对象在堆中的地址返回给p

## this关键字

```java
public class This01{
    public static void main(String[] args){
       Dog d1 = new Dog("わんちゃん",3);
       System.out.println(d1.hashCode);
       d1.info();
       Dog d2 = new Dog("わんわん",2);
       d2.info();
    }
}
class Dog{
    String name;
    int age;
    public Dog (String name,int age){
        //this.name就是当前对象的属性
        this.name = name;
        this.age = age;
        System.out.println(this.hashCode);
    }
    public void info(){//成员方法输出属性信息
       System.out.println(this.hashCode);
       System.out.println(name + "\t" + age + "\t");
    }
    
}
```

###this解决变量命名问题

this关键字的理解:简单来说，哪个对象调用，this就代表哪个对象

<img src="assets/%E6%88%AA%E5%B1%8F2022-10-06%2016.50.08.png" alt="截屏2022-10-06 16.50.08" style="zoom:50%;" />

```java
public class ThisDetail{
    public static void main(String[] args){
        T t1 = new T();
        t1.f2();
        
    }
}
class T{
    String name;
    int num = 100;
    /*
    1.this关键字可以用来访问本类的属性，方法，构造器
    2.this用于区分当前类的属性和局部变量
    3.访问成员方法的语法this.方法名(参数列表);
    4.访问构造器语法：this(参数列表)；注意只能在构造器中使用
    (即只能在构造器中调用构造器);注意：如果有访问构造器语法 必须放在第一条语句
    5.this不能在类定义的外部使用，只能在类定义的方法中使用
    */
    public T(){
        System.out.println("T()构造器");
        this("jack",100);
    }
    public T(String name,int age){
        System.out.println("T(String name，int age)构造器");
    }
    //this关键字可以用来访问本类的属性
    public void f3(){
        String name = "billMin";
        System.out.println("name" + name + "num" + num);
        System.out.println("name" + this.name + "num" + this.num);
    }
    //细节：访问成员方法的语法：this.方法名（参数列表）
    public void f1(){
        System.out.println("f1方法");
    }
    public void f2(){
        System.out.println("f2方法");
        //调用本类f1
        //1种
        f1();
        //2种
        this.f1();
    }
    
}
```

###练习

```java
public class TestPerson{
    public static void main(String[] args){
       Perosn p1 = new Person("mary",20);
       Perosn p1 = new Person("smith",20);
       System.out.println(p1.compareTo(p2));//比较结果
    }
}
class Person{
    String name;
    int age;
    //构造器
    public Person(String name,int age){
        this.name = name;
        this.age = age;
    }
    //compareTo比较方法
    public boolean compareTo(Person p){
        /*
        if(this.name.equals(p.name) && this.age == p.age){
            return true;
        }else{
            return false;
        }
        */
        return this.name.equals(p.name) && this.age == p.age;
    }
}
```

##面向对象基础的练习

```java
public class H01{
    public static void main(String[] args){
        A01 a = new A01();
        double[] arr = {};
        Double res = a.max(arr);
        if(res != null){
            System.out.println("arr的最大值=" + res);
        }else{
            System.out.println("入力エラーでです!");
        }
    }
}
class A01{
    public double max(double[] arr){
        
        if(arr != null && arr.length > 0);{//保证arr中最少有一个元素
           
            double max = arr[0];//假定第一个值就是最大值
            for(int i =1;i < arr.length;i++){
               if(max < arr[i]){
                   max = arr[i];
                }
            }
             return max;
        }else{
            return null;
        }
    }
}
/*
编写类A01，定义方法max，实现求某个double数组的最大值，并返回
先逻辑书写，再考虑代码的健壮性
*/
```

```java
public class H02{
    public static void main(String[] args){
        String[] strs = {"jack","tom","mary","kamada"};
        A02 a = new A02();
        int index = a.find("kameda",strs);
        System.out.println(index);
    }
}
class A02{
    public int find(String findstr,String[] strs){
        for(int i =0;i < strs.length;i++){
            if(findStr.equals(strs[i])){
                return i;
            }else{
                return -1;
            }
        }
    }
}
/*
编写类A02，定义方法find，实现查找某字符串是否在字符串数组中，
并返回索引，如果找不到返回-1
*/

```

```java
public class H03{
    public static void main(String[] args){
       Book b = new book("夏の音楽祭",8000);
       b.info();
       book.updatePrice();
       book.info();
    }
}
class Book{
    String name;
    double price;
    public Book(String name,double price){
        this.name = name;
        this.price = price;
    }
    public void updatePrice(){
        //如果方法中没有局部变量：price，this。price = price
        if(this.price > 150){
            this.price = 150;
        }else if(this.price > 100){
            this.price = 100;
        }
    }
    //显示书籍 的情况
    public void info(){
        System.out.println("书名" + this.name + "价格" + this.price);
    }
}
/*
编写类Book，定义方法updatePrise，实现更改某本书的价格
具体：如果价格>150,则更改为150，如果价格》100更改为100，否则不变
*/
```

```java
public class H04{
    public static void main(String[] args){
       int[] oldArr = {10,30,50};
       A03 a = new A03();
       int newArr = a.copyArr(oldArr);
       //遍历新 的验证
        System.out.println("新数组")
       for(int i =0;i < newArr.length;i++){
           System.out.print(newArr[i] + "\t");
       }
    }
}
class A03{
    public int[] copyArr(int[] oldArr){
        //在堆中，创建一个长度为oldArr.length数组
        int[] newArr = new int[oldArr.length];
        //遍历旧数组，将元素拷贝到新数组
        for(int i = 0;i < oldArr.length;i++){
            newArr[i] = oldArr[i];
        }
        return newArr;
    }
}
/*
编写类A03，实现数组的复制功能copyArr，输入旧数组，返回一个新数组，元素与旧数组一样
*/
```

```java
public class H05{
    public static void main(String[] args){
       Circle circle = new Circle(5);
       System.out.println(circle.area());
       System.out.println(circle.len());
    }
}
/*
定义一个圆类Circle，定义半径，提供显示圆周长功能的方法，提供显示圆面积的方法
*/
class Circle{
    double radius;
    public Circle(double radius){
        this.radius = radius;
    }
    
    public double area(){
        return Math.PI * radius * radius;
    }
    
    public double len(){
        return 2 * Math.PI * radius;
    }
}
```

```java
public class H06{
    public static void main(String[] args){
        Cale cale= new Cale(2,0);
        System.out.println(cale.sum());
        System.out.println(cale.minus());
        System.out.println(cale.mul());
        Double divRes = cale.div();
        if(dives != null){
           System.out.println(divres); 
        }
        
    }
}
/*
编程创建一个Cale计算类，在其中定义2个变量表示两个操作数
定义四个方法实现求和，差，乘，商(要求除数为0的话要提示)并创建两个对象，分别测试
*/
class Cale{
    double num1;
    double num2;
    public Cale(double num1,double num2){
        this.num1 = num1;
        this.num2 = num2;
    }
    //和
    public double sum(){
        return num1 + num2;
    }
    //差
    public double minus(){
        return num1 - num2;
    }
    //乘
    public double mul(){
        return num1 * num2;
    }
    //除
    public Double div(){
        if(num2 == 0){
            System.out.println("除数不能为0");
            return null;
        }else{
            return num1 / num2;
        }
        
    }
}
```

```java
public class H07{
    public static void main(String[] args){
        Dog dog = new Dog("tom","yellow",7);
        dog.show();
    }
}
/*
设计一个Dog类，有名字，颜色，和年龄属性，定义输出方法show()显示信息，并创建对象，进行测试
*/
class Dog{
  String name;
  String color;
  int age;
  public Dog(String name,String color,int age){
      this.name = name;
      this.color = color;
      this.age = age;
  }
    public void show(){
        System.out.println("显示信息");
        System.out.println(this.name + "\t" + this.age + "\t" + this.color);
    }
}
```

```java
public class Test{
    int count = 9;//属性
    public void count1(){//Test类的成员方法
        count = 10;
        System.out.println("count1" + count);
    }
    public void count2(){//Test类的成员方法
       System.out.println("count1" + count++);
    }
    //任何一个类都有main方法
    public static void main(String[] args){
        /*
        1.new Test()匿名对象 使用后不能再使用
        2.new Test().count1()创建好匿名对象后就调用count1()
        
        */
        new Test().count1();
        
        Test t1 = new Test();
        t1.count2();
        t1.count2();
    }
}
```

```java
public class H09{
    public static void main(String[] args){
       Music music = new Music("笑傲江湖"，300);
       mucis.play();
       System.out.println(music.getInfo());
    }
}
/*
定义music类。里面有音乐名name，音乐时长times属性
并有播放play功能和返回本身属性信息的功能方法getInfo
*/
class Music{
    String name;
    int times;
    public Music(String name,int times){
        this.name = name;
        this.times = times;
    }
    public void play(){
        System.out.println("音乐"  + name + "播放时长" + times);
    }
    public String getInfo(){
        return "音乐"  + name + "播放时长" + times;
    }
}
```

```java
public class H11{
    public static void main(String[] args){
      
    }
}
/*
在测试方法中，调用method方法，代码如下，编译正确，试写出method方法的定义形式
调用语句为System.out.println(method(10.0,20.0),100));
反推定义形式
public double method(double d1,doubl2 d2)
*/
```

```java
public class H12{
    public static void main(String[] args){
      
    }
}
/*
创建一个Employee类
属性有(名字，性别，年龄，职位，薪水)，提供三个构造方法，可以初始化
1.(名字，性别，年龄，职位，薪水)。
2.(名字，性别，年龄)3.(职位，薪水)要求充分复用构造器
*/
class Employee{
    String name;
    char gender;
    int age;
    String job;
    double sal;
    //因为要求可以复用构造器，先写属性少的构造器
    public Employee(String job,double sal){
        this.job = job;
        this.sal = sal;
    }
    public Employee(String name,char gender,int age){
        this.name = name;
        this.gender = gender;
        this.age = age;
    }
    public Employee(String name,char gender,int age,String job,double sal){
        this(name,gender,age);
        this.job = job;
        this.sal = sal;
    }
}
```

```java
public class H13{
    public static void main(String[] args){
      Circle c = new Circle();
      PassObject op = new PassObject;
      op.printAreas(c,5);
    }
}
/*
题目要求
1.定义一个Circle类，包含一个double型的radius属性代表圆的半径，findArea()方法返回圆 的面积
2.定义一个类PassObject，在类中定义一个方法printArea(),该方法的定义如下：
public void printAreas(Circle c ,int times)
3.在printAreas方法中打印输出1到times之间的每个整数半径值，以及对应的面积。
例如times为5，则输出半径1，2，3，4，5以及对应的圆面积
4.在main方法中调用printAreas()方法，调用完毕后输出当前半径。程序运行输出结果如图所示
*/
class Circle{
    double radius;
    //public Circle(radius){
        //this.radius = radius;
    //}
    public double findArea(){
        return Math.PI * radius * radius;
    }
    public void setRadius(double radius){//添加方法setRadius，修改对象半径值
        this.radius = radius;
    }
 
}
class PassObject{
    public void printAreas(Circle c ,int times){
        System.out.println("radius\tarea");
        for(int i = 1;i <= times;i++){//输出1到times之间的每个整数半径值
            c.setRadius(i);//修改半径值
            System.out.println((double)i + "\t" + c.findArea());
        }
    }
}
```

```java
import java.util.Random;
import java.util.Scanner;
/*
请编写一个猜拳的游戏
有个人Tom 对象，设计他的成员变量. 成员方法, 可以电脑猜拳. 电脑每次都会随机生成 0, 1, 2
0 表示 石头 1 表示剪刀 2 表示 布
并要可以显示 Tom的输赢次数（清单）, 假定 玩三次.
 */
// 测试类,主类
public class test {
 
    // 测试
    public static void main(String[] args) {
        // 创建一个玩家对象
        Tom t = new Tom();
        // 用来记录最后输赢的次数
        int isWinCount = 0;
 
        // 创建一个二维数组，用来接收局数，Tom出拳情况以及电脑出拳情况
        int[][] arr1 = new int[3][3];
        int j = 0;
 
        // 创建一个一维数组，用来接收输赢情况
        String[] arr2 = new String[3];
 
        Scanner scanner = new Scanner(System.in);
        for (int i = 0; i < 3; i++) {   //比赛3次
            System.out.println("请输入你要出的拳（0-拳头，1-剪刀，2-布）：");
            int num = scanner.nextInt();
            t.setTomGuessNum(num);
            int tomGuess = t.getTomGuessNum();
            arr1[i][j + 1] = tomGuess;//出的情况汇总的二维表格中
 
            // 获取电脑出的拳
            int comGuess = t.computerNum();
            arr1[i][j + 2] = comGuess;
 
            // 将玩家猜的拳与电脑做比较
            String isWin = t.vsComputer();
            arr2[i] = isWin;
            arr1[i][j] = t.count;
 
            // 对每一局的情况进行输出
            System.out.println("=========================================");
            System.out.println("局数\t玩家的出拳\t电脑的出拳\t输赢情况");
            System.out.println(t.count + "\t" + tomGuess + "\t\t" + comGuess + "\t\t" + t.vsComputer());
            System.out.println("=========================================");
            System.out.println("\n\n");
            isWinCount = t.winCount(isWin);
        }
        scanner.close();//关闭扫描器，它一直在占用资源，因此使用完毕后要关闭
 
        // 对游戏的最终结果进行输出（二维表格）
        System.out.println("局数\t玩家的出拳\t电脑的出拳\t\t输赢情况");
        for (int a = 0; a < arr1.length; a++) {
            for (int b = 0; b < arr1[a].length; b++) {
                System.out.print(arr1[a][b] + "\t\t\t");
            }
 
            System.out.print(arr2[a]);
            System.out.println();
        }
        System.out.println("你赢了" + isWinCount + "次");
    }
 
}
 
// Tom类
class Tom {     // 核心代码
    // 玩家出拳的类型
    int tomGuessNum; //0,1,2
    // 电脑出拳的类型
    int comGuessNum; //0,1,2
    // 玩家赢的次数
    int winCountNum;
    // 比赛的次数
    int count = 1;   //一共比赛3次
 
 
    public void showInfo() {//默认构造器可以省略
        //....
    }
 
    /**
     * 电脑随机生成猜拳的数字的方法
     * @return
     */
    public int computerNum() {
        Random r = new Random();
        comGuessNum = r.nextInt(3);      // 方法 返回 0-2的随机数
        // System.out.println(comGuessNum);
        return comGuessNum;
    }
 
    /**
     * 设置玩家猜拳的数字的方法
     * @param tomGuessNum
     */
    public void setTomGuessNum(int tomGuessNum) {
        if (tomGuessNum > 2 || tomGuessNum < 0) {
            //抛出一个异常, 李同学会写，没有处理
            throw new IllegalArgumentException("数字输入错误");//抛出的异常表示向方法传递了一个不合法的参数
        }
        this.tomGuessNum = tomGuessNum;
    }
 
    public int getTomGuessNum() {
        return tomGuessNum;
    }
 
    /**
     * 比较猜拳的结果
     * @return 玩家赢返回true，否则返回false
     */
    public String vsComputer() {
        //比较巧
        if (tomGuessNum == 0 && comGuessNum == 1) {
            return "你赢了";
        } else if (tomGuessNum == 1 && comGuessNum == 2) {
            return "你赢了";
        } else if (tomGuessNum == 2 && comGuessNum == 0) {
            return "你赢了";
        } else if (tomGuessNum == comGuessNum){
            return "平手";
        } else {
            return "你输了";
        }
    }
 
    /**
     * 记录玩家赢的次数
     * @return
     */
    public int winCount(String s) {
        count++;    //控制玩的次数
        if (s.equals("你赢了")) {     //统计赢的次数
            winCountNum++;
        }
        return winCountNum;
    }
 
}
```

# 面向对象中级

##包

###包的三大作用

1.区分相同名字的类

2.当类很多时，可以很好的管理类【看javaAPI文档】

3.控制访问范围

###包的基本语法

```java
package com.kamedaken.edu
    说明：
    1.package关键字，表示打包
    2.com.kamedaken.edu：表示包名
```

###包的本质分析

包的本质就是创建不同的文件夹/目录保存类文件

![截屏2022-10-13 14.50.52](assets/%E6%88%AA%E5%B1%8F2022-10-13%2014.50.52.png)

###包的命名规则

只能包含数字，字母，小圆点，但不能使用数字开头，不能是关键字保留字

命名规范

一般是小写字母+小圆点

com.公司名.项目名.业务模块名 比如：com.sina.crm.utils com.sina.crm.order

一个包下,包含很多的类,java 中

###常用的包:

1) java.lang.* //lang 包是基本包，默认引入，不需要再引入.

2) java.util.* //util 包，系统提供的工具包, 工具类，使用 Scanner //网络包，网络开发

3) java.net.*//网络包 网络开发

4)  java.awt.*//工具类

    

###如何引入包

1.package的作用是声明当前类所在的包，需要放在类的最上面，一个类中最多只有一句package

2.import指令位置放在package的下面，在类定义面前，可以有多句没有顺序要求

##访问修饰符

java 提供四种访问控制修饰符号，用于控制方法和属性(成员变量)的访问权限

\1) 公开级别:用public修饰,对外公开
 \2) 受保护级别:用protected修饰,对子类和同一个包中的类公开
 \3) 默认级别:没有修饰符号,向同一个包的类公开.
 \4) 私有级别:用private修饰,只有类本身可以访问,不对外公开

###4种访问修饰符的访问范围

![截屏2022-10-13 15.54.23](assets/%E6%88%AA%E5%B1%8F2022-10-13%2015.54.23.png)

###注意事项与细节

1.修饰符可以用来修饰类中的属性，成员变量以及类

2.只有默认和public才能修饰类！，并遵循上述访问权限的特点

3.子类的访问权限和继承有关

4.成员方法的访问规则和属性完全一样

##🚩面向对象的三大特征



面向对象编程有三大特征：封装，继承和多态

###封装(encapsulation)

就是把抽象出的数据【属性】和对数据操作【方法】封装在一起，数据被保护在内部，

程序的其他部分只有通过被授权的操作【方法】，才能对数据进行操作。

####封装的理解和好处

1.隐藏实现细节：方法【连接数据库】<-- 调用（传入参数）

2.可以对数据进行验证，保证安全合理

####封装的实现步骤

1.将属性进行私有化private【不能直接修改属性】

2.提供一个公共的 public set方法，用于对属性判断并赋值

```java
public void setXXX(类型 参数名){//xxx 表示某个属性
    //加入数据验证的业务逻辑
    属性 = 参数名；
}
```

3.提供一个公共的(public )get方法，用于获取属性的值

```java
public 数据类型 getXXX(){
    return xx;
}
```

```java
package com.kamadaken.pkg.encap;

import java.sql.SQLOutput;

public class Encapsulation01 {
    public static void main(String[] args) {
        //使用快捷键 需要先配置主类
        //需要先使用鼠标点击，之后可用
        Person person = new Person();
        person.setName("");
        person.setAge(300);
        person.setSalary(30000);
        System.out.println(person.info());
    }
}
/*
那么在 java 中如何实现这种类似的控制呢?
请大家看一个小程序(com.hspedu.encap: Encapsulation01.java),
不能随便查看人的年龄,工资等隐私，并对设置的年龄进行合理的验证。
年龄合理就设置，否则给默认 年龄, 必须在 1-120, 年龄， 工资不能直接查看
， name 的长度在 2-6 字符 之间
*/

class Person{
    public String name;
    private int age;
    private double salary;

    //set和get方法快捷键
    //根据要求完善


    public String getName() {
        return name;
    }

    public void setName(String name) {
        //加入对数据对校验
        if(name.length() >= 2 && name.length() <= 6){
            this.name = name;
        }else{
            System.out.println("名字长度不对，默认名字");
            this.name = "无名人";
        }
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        //判断
        if(age >= 1 && age <= 120){
            this.age = age;
        }else{
            System.out.println("你设置到年龄不对，默认年龄18");
            this.age = 18;
        }
    }

    public double getSalary() {
        //可以增加对当前对象的权限判断
        return salary;
    }

    public void setSalary(double salary) {
        this.salary = salary;
    }
    //写一个方法返回属性信息
    public String info(){
        return "名字" + name + "年龄" + age + "工资" + salary;
    }
}

```

```java
package com.kamadaken.pkg.encap;
/**
 * 创建程序,在其中定义两个类:Account 和 AccountTest 类体会 Java 的封装性。
 * Account 类要求具有属性:姓名(长度为 2 位 3 位或 4 位)、余额(必须>20)、
 * 密码(必须是六位), 如果不满足，则给出提示信息，并给默认值(程序员自己定)
 * 通过 setXxx 的方法给 Account 的属性赋值。
 * 在 AccountTest 中测试
 */
public class Account {
//为了封装将3个属性设置为private
    private String name;
    private double balance;
    private String pwd;

    //提供两个构造器
    public Account() {

    }
    public Account(String name, double balance, String pwd) {
        this.setName(name);
        this.setBalance(balance);
        this.setPwd(pwd);
    }



    public String getName() {
        return name;
    }

    public void setName(String name) {
        if(name.length() >= 2 && name.length() <= 4) {
            this.name = name;
        }else{
            System.out.println("姓名要求234位，默认值为kameda");
            this.name = "kameda";
        }
    }

    public double getBalance() {
        return balance;
    }

    public void setBalance(double balance) {
        if(balance > 20) {
            this.balance = balance;
        }else{
            System.out.println("余额大于20，默认为0");
        }
    }

    public String getPwd() {
        return pwd;
    }

    public void setPwd(String pwd) {
        if(pwd.length() == 6) {
            this.pwd = pwd;
        }else{
            System.out.println("密码六位，默认是六个0");
            this.pwd = "000000";
        }
    }
    //显示账号信息
    public void showInfo(){
        //可以增加权限校验
        System.out.println("账号信息" + name + "余额" + balance + "密码" + pwd);
    }
}

```

###继承

继承可以解决代码复用,让我们的编程更加靠近人类思维.当多个类存在相同的属性(变量)和方法时,可以从这些类中 抽象出父类,在父类中定义这些相同的属性和方法，所有的子类不需要重新定义这些属性和方法，只需要通过 extends 来 声明继承父类即可。画出继承的示意图

<img src="assets/%E6%88%AA%E5%B1%8F2022-10-14%2015.28.04.png" alt="截屏2022-10-14 15.28.04" style="zoom:67%;" />

####继承基本语法

```java
class 子类 extends 父类{
    1.子类就会自动拥有父类定义的属性和方法
    2.父类又叫超类，基类
    3.子类又叫派生类
}
```

####继承给编码带来的便利

1) 代码的复用性提高了

2) 代码的扩展性和维护性提高了

####继承的深入讨论

**因为子类要继承父类的属性与方法，就必须完成父类的初始化**

1. 子类继承了所有的属性和方法，非私有的属性和方法可以在子类直接访问, 但是私有属性和方法不能在子类直接访 问，要通过父类提供公共的方法去访问
2. 子类必须调用父类的构造器，完成父类的初始化
3.  当创建子类对象时，不管使用子类的哪个构造器，默认情况下总会去调用父类的无参构造器，如果父类没有提供无参构造器，则必须在子类的构造器中用 super 去指定使用父类的哪个构造器完成对父类的初始化工作，否则，编译不会通过(怎么理解。) [举例说明]
4. 如果希望指定去调用父类的某个构造器，则显式的调用一下 : super(参数列表)
5. super 在使用时，必须放在构造器第一行(super 只能在构造器中使用)
6.  super() 和 this() 都只能放在构造器第一行，因此这两个方法不能共存在一个构造器
7. java 所有类都是 Object 类的子类, Object 是所有类的基类.
8. 父类构造器的调用不限于直接父类!将一直往上追溯直到Object类(顶级父类)
9. 子类最多只能继承一个父类(指直接继承)，即java中是**单继承机制**。思考:如何让A类继承B类和C类? 【A 继承 B， B继承C】
10. 不能滥用继承，子类和父类之间必须满足 is-a 的逻辑关系。

#### 继承的本质分析（重要）

继承的本周就是建立一种查找关系

![截屏2022-10-18 19.36.36](assets/%E6%88%AA%E5%B1%8F2022-10-18%2019.36.36.png)

#### 继承课堂练习

### SUPER关键字

#### 基本介绍

super代表父类的引用，用于访问父类的属性，方法，构造器。

#### 基本语法

```java
1.访问父类的属性，但不能访问父类的private属性
    super.属性名
2.访问父类的方法，不能访问父类的private方法
    super.方法名(参数列表)；
3.访问父类的构造器
    super(参数列表);只能放在构造器的第一句，只能出现一句
```

#### super给编程带来的便利和细节

1.调用父类构造器的好处(分工明确，父类属性由父类初始化，子类属性由子类初始化)

2.当子类中有和父类中的成员（属性和方法）重名时，为了访问父类的成员，必须通过super。如果没有重名，使用super，this，直接访问是一样的效果

3.super的访问不限于直接父类，如果爷爷类和本类中有同名的成员，必须通过super去访问爷爷类的成员；

如果多个基类中有同名的成员，使用super访问遵循就近原则。当然也需要访问权限的相关规则。 

#### super和this的比较

![截屏2022-10-20 17.12.24](assets/%E6%88%AA%E5%B1%8F2022-10-20%2017.12.24.png)

### 方法重写/覆盖

简单的说：方法覆盖就是子类有一个方法，和父类的某个方法的名称，返回类型，参数一样，那么就说子类这个方法覆盖了父类的方法

####注意事项及使用细节

1.子类的方法的形参列表，方法名称，要和父类方法的形参列表，方法名称完全一样

2.子类方法的返回类型要和父类方法的返回类型一样，或者父类返回类型的子类。

例如父类的返回类型是Object，子类的返回类型是String

3.子类方法不能缩小父类方法的访问权限

#### 重写与重载的比较

![截屏2022-10-20 20.56.16](assets/%E6%88%AA%E5%B1%8F2022-10-20%2020.56.16.png)

### 多态

方法或对象具有多种形态。是面向对象的第三大特征，多态是建立在封装和继承基础之上的。

#### 方法的多态

重写或重载就体现多态

```java
package com.kamadaken.pkg.poly_;

public class PloyMethod {
    public static void main(String[] args) {
        //方法重载体现多态
        A a = new A();
        System.out.println(a.sum(10, 20));
        System.out.println(a.sum(10, 20, 30));
        //通过传入不同参数，就会调用sum方法，就体现多态

        //方法重写体现多态
        B b = new B();
        a.say();
        b.say();


    }

}

class B {
    public void say() {
        System.out.println("B say()方法被调用。。。");
    }
}

class A extends B {
    public int sum(int n1, int n2) {
        return n1 + n2;
    }

    public int sum(int n1, int n2, int n3) {
        return n1 + n2 + n3;
    }

    public void say() {
        System.out.println("A say()方法被调用。。。");
    }
}
```

#### 对象的多态（核心 困难）

1）一个对象的编译类型和运行类型可以不一致

2）编译类型在定义对象时，就确定了不能改变

3）运行类型是可以变化的

4）编译类型看定义时=号 的左边，运行类型看= 号的右边

访问对象属性时看编译类型

z调用方法按运行类型查找方法

#### 快速入门

```java
package com.kamadaken.pkg.poly_;

public class Poly01 {
    public static void main(String[] args) {
        Master tom = new Master("Tom");
        Dog dog = new Dog("Dahuang");
        Bone bone = new Bone("bone");
        tom.feed(dog,bone);

        Cat cat = new Cat("Jerry");
        Fish fish = new Fish("サーモン");
        System.out.println("==========");
        tom.feed(cat,fish);

        Pig pig = new Pig("pig");
        Rice rice = new Rice("rice");
        System.out.println("=========");
        tom.feed(pig,rice);
        
    }
}
package com.kamadaken.pkg.poly_;

public class Animal {
    private String name;

    public Animal(String name) {
        this.name = name;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }
}
package com.kamadaken.pkg.poly_;

public class Food {
    private String name;

    public Food(String name) {
        this.name = name;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }
}
package com.kamadaken.pkg.poly_;

public class Master {
    private String name;

    public Master(String name) {
        this.name = name;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    //使用多态机制，可以统一的管理主人喂食到问题
    //animal编译类型是Animal,可以指向Animal子类的对象

    public void feed(Animal animal,Food food){
        System.out.println("主人" + name + "给" + animal.getName() + "吃" + food.getName());

    }


    //主人给小狗喂骨头

//    public void feed(Dog dog, Bone bone) {
//        System.out.println("主人" + name + "给" + dog.getName() + "吃" + bone.getName());
//    }
//    //给小猫吃黄花鱼
//    public void feed(Cat cat,Fish fish){
//        System.out.println("主人" + name + "给" + cat.getName() + "吃" + fish.getName());
//    }
}
package com.kamadaken.pkg.poly_;

public class Dog extends Animal{
    public Dog(String name) {
        super(name);
    }
}
package com.kamadaken.pkg.poly_;

public class Cat extends Animal{
    public Cat(String name) {
        super(name);
    }
}
package com.kamadaken.pkg.poly_;



public class Pig extends Animal {
    public Pig(String name) {
        super(name);
    }
}
package com.kamadaken.pkg.poly_;

public class Bone extends Food{
    public Bone(String name) {
        super(name);
    }
}
package com.kamadaken.pkg.poly_;

public class Fish extends Food {
    public Fish(String name) {
        super(name);
    }
}
package com.kamadaken.pkg.poly_;

public class Rice extends Food {
    public Rice(String name) {
        super(name);
    }
}
```

#### 多态的注意事项与细节讨论

多态的**前提**是：两个对象存在继承关系。

##### 多态的向上转型

1.本质：父类的引用指向了子类的对象。

2.语法：父类类型 引用名 = new子类类型（）；

3.特点：

```
可以调用父类的所有成员（需要遵守访问权限）
但是不能调用子类的特有成员
因为在编译阶段，能调用那些成员，是由编译类型决定的
最终运行效果看子类（运行类型）的具体实现，即调用方法时，按照子类开始查找方法
然后调用，规则与方法的调用规则一致
```

##### 多态的向下转型

语法：子类类型 引用名 = （子类类型)**父类引用**；

只能强转父类的引用，但不能强转父类的对象

要求父类的引用必须指向的是当前目标的对象

当向下转型时，可以调用子类类型中所有成员

#####instanceOf比较操作符

用于判断对象的运行类型是否为XX类型或XX类型的子类型

#### 练习

![截屏2022-10-22 14.22.02](assets/%E6%88%AA%E5%B1%8F2022-10-22%2014.22.02.png)

<img src="assets/%E6%88%AA%E5%B1%8F2022-10-22%2014.23.44.png" alt="截屏2022-10-22 14.23.44" style="zoom:67%;" />

#### 🚩java的动态绑定机制

```java
package com.kamadaken.pkg.poly_.dynamic_;

public class DynamicBinding {
    public static void main(String[] args) {
        //a的编译类型A，运行类型B
        A a = new B();//向上转型
        System.out.println(a.sum());
        System.out.println(a.sum1());

    }
}

class A {//父类
    public int i = 10;
    /*动态绑定机制：
    1 当调用对象方法的时候，该方法会和对象的内存地址/运行类型绑定
    2 当调用对象属性时，没有动态绑定机制，哪里声明哪里使用
     */
    public int sum() {
        return getI() + 10;
    }

    public int sum1() {
        return i + 10;
    }

    public int getI() {
        return i;
    }

}

class B extends A {
    public int i = 20;

    //    public int sum(){
//        return i+ 20;
//    }
    public int getI() {
        return i;
    }
//    public int sum1(){
//        return i + 10;
//    }
}
```

#### 多态的应用

#####多态数组

```java
package com.kamadaken.pkg.poly_.polyarr_;


 public class PolyArray {
    public static void main(String[] args) {
        //应用实例：现有一个继承结构如下：要求创建一个Person对象
        //2个Student 对象和2个teacher对象，统一放在数组中，并调用每个对象say方法
        Perosn[] persons = new Perosn[5];
        persons[0] = new Perosn("jack", 20);
        persons[1] = new Student("MIN", 24, 100);
        persons[2] = new Student("smith", 30, 45);
        persons[3] = new Teacher("scott", 40, 25000);
        persons[4] = new Teacher("Kameda", 62, 1500000);

        //循环遍历多态数组，调用say
        for (int i = 0; i < persons.length; i++) {
            //person[i] 编译类型是 Person ,运行类型是是根据实际情况有 JVM 来判断
            System.out.println(persons[i].say());// 动态绑定机制
            //使用类型判断 + 向下转型.
            if (persons[i] instanceof Student) {
                ((Student) persons[i]).study();

            } else if (persons[i] instanceof Teacher) {
                ((Teacher) persons[i]).teach();

            } else {
                System.out.println("类型有误");
            }
         }
     }
}
package com.kamadaken.pkg.poly_.polyarr_;

public class Perosn {
    private String name;
    private int age;

    public Perosn(String name, int age) {
        this.name = name;
        this.age = age;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    public String say() {
        return name + "\t" + age;
    }
}
package com.kamadaken.pkg.poly_.polyarr_;

public class Teacher extends Perosn {
    private double salary;

    public Teacher(String name, int age, double salary) {
        super(name, age);
        this.salary = salary;
    }

    public double getSalary() {
        return salary;
    }

    public void setSalary(double salary) {
        this.salary = salary;
    }

    //重写父类say方法
    public String say(){
        return super.say() + "salary=" + salary;
    }
    //特有方法
    public void teach(){
        System.out.println("老师" + getName() + "正在授课");
    }
}
package com.kamadaken.pkg.poly_.polyarr_;

import com.kamadaken.pkg.super_.A;

public class Student extends Perosn{
    private double score;

    public Student(String name, int age, double score) {
        super(name, age);
        this.score = score;
    }

    public double getScore() {
        return score;
    }

    public void setScore(double score) {
        this.score = score;
    }

    //重写父类的say方法
    public String say(){
        return  super.say() +"score="+ score;
    }
    //特有方法
    public void study(){
        System.out.println("学生" + getName() + "正在上课");
    }
}
```

#####多态参数

```java
package com.kamadaken.pkg.poly_.polyparameter;

public class PloyParameter {
    public static void main(String[] args) {
        Worker tom = new Worker("tom", 45000);
        Manager min = new Manager("min", 999999, 99999);
        PloyParameter ployParameter = new PloyParameter();
        ployParameter.showEmpAnnual(min);

        ployParameter.testWork(tom);



    }
    //实现获取任何员工对象的年工资,并在 main 方法中调用该方法 [e.getAnnual()]
    public void showEmpAnnual(Employee e){
        System.out.println(e.getAnnual());
    }
    //添加一个方法，testWork,如果是普通员工，则调用 work 方法，
    // 如果是经理，则调用 manage 方法
    public void testWork(Employee e){
        if(e instanceof Worker){
            ((Worker) e).work();

        } else if (e instanceof Manager) {
            ((Manager) e).manage();
        }else{
            System.out.println("null");
        }
    }
}

package com.kamadaken.pkg.poly_.polyparameter;

public class Employee {
    private String name;
    private double salary;

    public Employee(String name, double salary) {
        this.name = name;
        this.salary = salary;
    }

    //得到年工资的方法
    public double getAnnual(){
        return 12 * salary;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public double getSalary() {
        return salary;
    }

    public void setSalary(double salary) {
        this.salary = salary;
    }


}
package com.kamadaken.pkg.poly_.polyparameter;

public class Manager extends  Employee{
    private double bonus;

    public Manager(String name, double salary, double bonus) {
        super(name, salary);
        this.bonus = bonus;
    }

    public double getBonus() {
        return bonus;
    }

    public void setBonus(double bonus) {
        this.bonus = bonus;
    }

    public void manage(){
        System.out.println("manager" + getName() + "is managing");
    }
    //重写获取年金的方法

    @Override
    public double getAnnual() {
        return super.getAnnual() + bonus;
    }
}
package com.kamadaken.pkg.poly_.polyparameter;

public class Worker extends Employee {
    public Worker(String name, double salary) {
        super(name, salary);
    }

    public void work() {
        System.out.println("staff " + getName() + " is working");
    }

    public double getAnnual(){
        return super.getAnnual();
    }
}
```

#### Object类详解

##### equals方法

== 与equals 的对比

==是一个比较运算符

1.==：既可以判断基本类型，又可以判断引用类型

2.==：如果判断基本类型，判断的是值是否相等

3.==：如果判断的是引用类型，判断的是地址是否相等，即指向的是否是同一个对象

4.equals：是Object类中的方法，只能判断引用类型

5.默认判断的是地址是否相等，子类中往往重写该方法，用于判断内容是否相等。

```java
package com.kamadaken.pkg.poly_.object_;

public class Equals01 {
    public static void main(String[] args) {
        A a = new A();

        "hello".equals("abc");
        //equals方法的源码
        /*
        //
        public boolean equals(Object anObject) {
        if (this == anObject) {//如果是同一个对象
            return true;
        }
        if (anObject instanceof String) {//判断类型是否相等
            String anotherString = (String)anObject;//向下转型
            int n = value.length;
            if (n == anotherString.value.length) {
                char v1[] = value;
                char v2[] = anotherString.value;
                int i = 0;
                while (n-- != 0) {//一个个比较字符
                    if (v1[i] != v2[i])
                        return false;
                    i++;
                }
                return true;
            }
        }
        return false;
    }
         */

        /*Object 的 equals 方法默认就是对象的地址是否相同
        public boolean equals(Object obj) {
        return (this == obj);
    }

         */

        Integer integer = new Integer(5);

        /*
        public boolean equals(Object obj) {
        if (obj instanceof Integer) {
            return value == ((Integer)obj).intValue();
        }
        return false;
    }
         */
   }
}
class A{

}

```

练习

```java
package com.kamadaken.pkg.poly_.object_;

public class EqualsExercise01 {
    public static void main(String[] args) {
        Person person1 = new Person("min", 24, 'M');
        Person person2 = new Person("min", 24, 'M');
        System.out.println(person1.equals(person2));
    }
}
class Person{
    private String name;
    private int age;
    private char gender;

    public boolean equals(Object obj){
        if(this == obj){
            return true;
        }
        if(obj instanceof Person){
            Person p =(Person) obj;
            return this.name.equals(p.name)&&this.age == p.age&&this.gender== p.gender;
        }
        return false;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    public char getGender() {
        return gender;
    }

    public void setGender(char gender) {
        this.gender = gender;
    }

    public Person(String name, int age, char gender) {
        this.name = name;
        this.age = age;
        this.gender = gender;
    }
}

```

#####hashCode方法

1) 提高具有哈希结构的容器的效率!
2) 两个引用，如果指向的是同一个对象，则哈希值肯定是一样的!
3) 两个引用，如果指向的是不同对象，则哈希值是不一样的
4) 哈希值主要根据地址号来的!，不能完全将哈希值等价于地址。

##### toString方法

基本介绍

1. 默认返回:全类名+@+哈希值的十六进制，【查看 Object 的 toString 方法】 子类往往重写 toString 方法，用于返回对象的属性信息

2. 重写toString方法，打印对象或拼接对象时，都会自动调用该对象的toString形式.

3. 当直接输出一个对象时，toString 方法会被默认的调用, 比如 System.out.println(monster); 就会默认调用

    monster.toString()

```java 
package com.kamadaken.pkg.poly_.object_;

public class ToString_ {
    public static void main(String[] args) {
        /* toString方法的源码
        public String toString() {
        return getClass().getName() + "@" + Integer.toHexString(hashCode());
    }
         */
        Monster monster = new Monster("小妖怪", "巡山", 280000);
        System.out.println(monster.toString());


        System.out.println(monster);//输出对象会默认调用toString
    }

}
class Monster{
    private String name;
    private String job;
    private double sal;

    public Monster(String name, String job, double sal) {
        this.name = name;
        this.job = job;
        this.sal = sal;
    }
    //重写toString方法，输出对象属性
//    快捷键


    @Override
    public String toString() {//默认重写后输出对象的属性
        return "Monster{" +
                "name='" + name + '\'' +
                ", job='" + job + '\'' +
                ", sal=" + sal +
                '}';
    }
}

```

##### finalize 方法

1. 当对象被回收时，系统自动调用该对象的finalize方法。子类可以重写该方法，做一些释放资源的操作【演示】

2.  什么时候被回收:当某个对象没有任何引用时，则jvm就认为这个对象是一个垃圾对象，就会使用垃圾回收机制来 销毁该对象，在销毁该对象前，会先调用 finalize 方法。

3. 垃圾回收机制的调用，是由系统来决定(即有自己的GC算法),也可以通过System.gc()主动触发垃圾回收机制，测试:Car [name]

    

```java
package com.kamadaken.pkg.poly_.object_;

public class Finalize_ {
    public static void main(String[] args) {
        Car bmw = new Car("BMW");
        bmw = null;//car成为垃圾对象，垃圾回收机制(销毁)对象，
        // 在销毁前会调用该对象的finalize方法
        //这时，可以在finalize中写自己的业务逻辑（比如释放资源，或者打开的文件流）
        System.gc();//主动调用垃圾回收器
        System.out.println("程序退出");
    }
}
class Car{
    private String name;

    public Car(String name){
        this.name = name;
    }
    //重写
    @Override
    protected void finalize() throws Throwable {
        System.out.println("销毁汽车" + name);
        System.out.println("释放资源");
    }
}

```

#### 断点调试

1.断电调试是指在程序的某一行设置一个断点，调试时，程序运行到这一行时就会停住，然后就可以一步一步向下调试，调试过程中可以看各个变量当前的值，出错的话，调试到出错的代码行即显示错误停下，进而分析找到BUG。

2.断点调试是程序员必须掌握的技能

3.断点调试也能帮助查看底层源码的执行过程，提高编程水平

```java
package com.kamadaken.pkg.debug_;
//debug对象创建过程，加深对调试对理解
public class DebugExercise {
    public static void main(String[] args) {
        //创建对象流程
        //1)加载Person类信息
        //2)初始化 2。1默认初始化，2。2显示初始化，2。3构造器初始化
        //3）返回对象地址
        Person jack = new Person("jack", 24);
        System.out.println(jack);
    }
}
class Person{
    private String name;
    private int age;

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    @Override
    public String toString() {
        return "Person{" +
                "name='" + name + '\'' +
                ", age=" + age +
                '}';
    }
}
```

1.使用断点调试的方法，追踪下一个对象 的创建过程。

2.查看动态绑定机制如何工作

![截屏2022-10-27 18.04.12](assets/%E6%88%AA%E5%B1%8F2022-10-27%2018.04.12.png)

#### 项目零钱通

开发 零钱通项目 , 可以完成收益入账，消费，查看明细，退出系统等功能.

```java
package com.kamadaken.pkg.smallchange.oop;

public class SmallChangeSysApp {
    public static void main(String[] args) {
        
        new SmallChangeSysoop().mainMenu();
    }
}

package com.kamadaken.pkg.smallchange.oop;

import java.text.SimpleDateFormat;
import java.util.Date;
import java.util.Scanner;

/**
 * 该类是完成零钱通各个功能的分类
 * 使用oop
 * 各个功能对象一个方法
 */
public class SmallChangeSysoop {
    //属性

    //1.定义相关变量
    boolean loop = true;
    Scanner scanner = new Scanner(System.in);
    String key = "";

    //2。1）收益入账和消费2）使用对象 3）String拼接

    String details = "------零钱通明细-------";

    //3.
    //定义新的变量
    //功能驱动代码
    double money = 0;
    double balance = 0;
    Date date = null;//引入java.util
    SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd HH:mm");
    //4。定义新变量保存消费的原因
    String note = "";
    public  void mainMenu() {
        do {
            System.out.println("\n=======选择零钱通菜单=======");
            System.out.println("\t\t\t1 零钱通明细");
            System.out.println("\t\t\t2 收益入账");
            System.out.println("\t\t\t3 消费");
            System.out.println("\t\t\t4 退出");

            System.out.print("请选择1-4");
            key = scanner.next();

            //使用switch分支控制
            switch (key) {
                case "1":
                   this.detail();
                    break;
                case "2":
                    this.income();
                    break;
                case "3":
                    this.pay();
                    break;
                case "4":
                   this.exit();
                    break;

                default:
                    System.out.println("选择有误请重新选择");


            }


        } while (loop);
    }

    //完成零钱通明细
    public void detail(){
        System.out.println(details);

    }
    //收益入账
    public void income(){
        System.out.println("收益入账金额：");
        money = scanner.nextDouble();
        //money的值范围校验
        if (money <= 0){
            System.out.println("收益范围需要大于0");
            return;//退出方法
        }
        balance += money;
        //拼接收益入账信息到details
        date = new Date();//获取当前日前

        details += "\n收益入账\t+" + money + "\t" + sdf.format(date) + "\t" + balance;

    }
    public void pay(){
        System.out.println("消费金额");
        money = scanner.nextDouble();
        if (money <= 0||money >balance){
            System.out.println("消费金额0" + balance);
            return;
        }
        System.out.println("消费说明：");
        note = scanner.next();
        balance -= money;
        //接收信息
        details += "\n" + note + "\t" + money + "\t" + sdf.format(date) + "\t" + balance;

    }
    public void exit(){
        String choice = "";
        while (true) {
            System.out.println("你确定退出？ y/n");
            choice = scanner.next();
            if ("y".equals(choice) || "n".equals(choice)) {
                break;

            }
        }
        if (choice.equals("y")) {
            loop = false;
        }

     }
}
```

####练习

```java
package com.kamadaken.pkg.homework;

import javax.imageio.plugins.jpeg.JPEGImageReadParam;

public class Homework01 {
    public static void main(String[] args) {
        Person[] people = new Person[5];
        people[0] = new Person("kameda", 62, "java工程师");
        people[1] = new Person("MINWEN", 24, "HCI工程师");
        people[2] = new Person("OK", 99, "java工程师");
        people[3] = new Person("kaunkyoku", 27, "SAP工程师");
        people[4] = new Person("Wei", 32, "アルゴリズム工程师");
        System.out.println("排序前输出");
        for (int i = 0; i < people.length; i++) {
            System.out.println(people[i]);

        }
        Person tmp = null;
        for (int i = 0; i < people.length-1; i++) {
            for (int j = 0; j < people.length - 1 - i; j++) {
                if (people[j].getAge() > people[j+1].getAge()){
                    tmp = people[j];
                    people[j] =people[j+1];
                    people[j+1] =tmp;
                }
            }

        }
        System.out.println("排序后");
        for (int i = 0; i < people.length; i++) {
            System.out.println(people[i]);

        }
    }
    /*
     定义一个Person类按age从小到大排序
    */


}
class Person{
    private String name;
    private int age;
    private String Job;

    public Person(String name, int age, String job) {
        this.name = name;
        this.age = age;
        Job = job;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    public String getJob() {
        return Job;
    }

    public void setJob(String job) {
        Job = job;
    }

    @Override
    public String toString() {
        return "Person{" +
                "name='" + name + '\'' +
                ", age=" + age +
                ", Job='" + Job + '\'' +
                '}';
    }
}

```

```java
package com.kamadaken.pkg.homework;

public class Homework03 {
    public static void main(String[] args) {
        Professor professor = new Professor("min", 24, "professor", 30000, 1.3);
        professor.introduce();
    }
}
package com.kamadaken.pkg.homework;
/*
(1)要求有属性 姓名 年龄 职称 基本工资
(2)编写业务方法，introduce(),实现输出一个教师信息
 */
public class Teacher {
    private String name;
    private int age;
    private String post;
    private double salary;
    private double level;

    public Teacher(String name, int age, String post, double salary, double level) {
        this.name = name;
        this.age = age;
        this.post = post;
        this.salary = salary;
        this.level = level;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    public String getPost() {
        return post;
    }

    public void setPost(String post) {
        this.post = post;
    }

    public double getSalary() {
        return salary;
    }

    public void setSalary(double salary) {
        this.salary = salary;
    }

    public double getLevel() {
        return level;
    }

    public void setLevel(double level) {
        this.level = level;
    }
    public void introduce(){
        System.out.println("name: " + name + "age: " + age +
                "post: " + post +"salary: "
        +salary + "level: " + level);
    }
}
package com.kamadaken.pkg.homework;

public class Professor extends Teacher {
    public Professor(String name, int age, String post, double salary, double level) {
        super(name, age, post, salary, level);
    }

    @Override
    public void introduce() {
        System.out.println("教授的信息");
        super.introduce();
    }
}
```

```java
package com.kamadaken.pkg.homework;

public class Homework04 {
    public static void main(String[] args) {
        Manager min = new Manager("min", 50000, 20, 1.2);
        min.setBonus(900000);
        min.printSal();

        Worker Z = new Worker("zhaosiyu", 30000, 20, 1.0);
        Z.printSal();

    }
}
package com.kamadaken.pkg.homework;

public class Employee {
    //属性
    private String name;
    private  double daySal;
    private int workDays;
    private double level;


    public Employee(String name, double daySal, int workDays, double level) {
        this.name = name;
        this.daySal = daySal;
        this.workDays = workDays;
        this.level = level;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public double getDaySal() {
        return daySal;
    }

    public void setDaySal(double daySal) {
        this.daySal = daySal;
    }

    public int getWorkDays() {
        return workDays;
    }

    public void setWorkDays(int workDays) {
        this.workDays = workDays;
    }

    public double getLevel() {
        return level;
    }

    public void setLevel(double level) {
        this.level = level;
    }
    public void printSal(){
        System.out.println(name + "工资： " + daySal*workDays*level);
    }

}
package com.kamadaken.pkg.homework;

public class Manager extends Employee {
    private double bonus;
    //创建Manager对象时，不确定奖金

    public Manager(String name, double daySal, int workDays, double level) {
        super(name, daySal, workDays, level);
    }

    public double getBonus() {
        return bonus;
    }

    public void setBonus(double bonus) {
        this.bonus = bonus;
    }

    @Override
    public void printSal() {
        System.out.println("manager: " + getName() + " " + "salary: " +
                (bonus + getDaySal() * getWorkDays() * getLevel()));
    }
}
package com.kamadaken.pkg.homework;

public class Worker extends Employee{
    public Worker(String name, double daySal, int workDays, double level) {
        super(name, daySal, workDays, level);

    }

    @Override
    public void printSal() {
        super.printSal();
    }
}

```

```java
package com.kamadaken.pkg.homework.Homework05;

public class Homework05 {
    public static void main(String[] args) {
        Worker jack = new Worker("jack", 5000);
        jack.setSalMonth(9);
        jack.printSal();

        Peasent smith = new Peasent("smith", 5000);
        smith.printSal();
        Teacher kameda = new Teacher("Kameda", 90000);
        kameda.setClassDays(240);
        kameda.setClassSal(9000);
        kameda.printSal();

        Scientist min = new Scientist("MIN", 900000);
        min.setBonus(9000);
        min.printSal();
    }
}
package com.kamadaken.pkg.homework.Homework05;

public class Employee {
    private String name;
    private  double sal;
    private int salMonth = 12;

    public Employee(String name, double sal) {
        this.name = name;
        this.sal = sal;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public double getSal() {
        return sal;
    }

    public void setSal(double sal) {
        this.sal = sal;
    }

    public int getSalMonth() {
        return salMonth;
    }

    public void setSalMonth(int salMonth) {
        this.salMonth = salMonth;
    }
    public void printSal(){
        System.out.println(name + "年工资" + (sal*salMonth));
    }
}
package com.kamadaken.pkg.homework.Homework05;

public class Worker extends Employee{
    public Worker(String name, double sal) {
        super(name, sal);
    }

    @Override
    public void printSal() {
        System.out.println("工人");
        super.printSal();
    }
}
package com.kamadaken.pkg.homework.Homework05;

public class Peasent extends Employee{
    public Peasent(String name, double sal) {
        super(name, sal);
    }

    @Override
    public void printSal() {
        super.printSal();
    }
}
package com.kamadaken.pkg.homework.Homework05;

public class Teacher extends Employee{
    private int classDays;
    private double classSal;

    public Teacher(String name, double sal) {
        super(name, sal);
    }

    public int getClassDays() {
        return classDays;
    }

    public void setClassDays(int classDays) {
        this.classDays = classDays;
    }

    public double getClassSal() {
        return classSal;
    }

    public void setClassSal(double classSal) {
        this.classSal = classSal;
    }

    @Override
    public void printSal() {
        System.out.println(getName() + "の年間給料"
                +(getSal()*getSalMonth() + classSal* classDays) );
    }
}
package com.kamadaken.pkg.homework.Homework05;

public class Scientist extends Employee {
    private double bonus;

    public Scientist(String name, double sal) {
        super(name, sal);
    }

    public double getBonus() {
        return bonus;
    }

    public void setBonus(double bonus) {
        this.bonus = bonus;
    }

    @Override
    public void printSal() {
        System.out.println("科学家");
        System.out.println(getName() + "年工资 "
                + getSal() * getSalMonth() + bonus);
    }
}

```

super（父类对象）可以访问父类及以上，除了 private修饰、静态、覆盖的成员

this(对象本身)可以访问自己的所有(非静态)成员，和父类及以上，除了private修饰、静态、覆盖的成员

```java
package com.kamadaken.pkg.homework;

public class Homework07 {

}
    class Test {
        String name = "Rose";

        Test() {
            System.out.println("Test");
        }

        Test(String name) {
            this.name = name;
        }
    }

class Demo extends Test{
        String name = "jack";
        Demo(){
            super();
            System.out.println("Demo");
        }
        Demo(String s){
            super(s);
        }
        public void test(){
            System.out.println(super.name);
            System.out.println(this.name);
        } 

        public static void main(String[] args) {
            new Demo().test();
            new Demo("john").test();

        }
}

```

![截屏2022-10-26 21.16.43](assets/%E6%88%AA%E5%B1%8F2022-10-26%2021.16.43.png)

```java
package com.kamadaken.pkg.homework;

import com.kamadaken.pkg.homework.Homework05.SavingAccount;

public class HomeWork08 {
    public static void main(String[] args) {
//        CheckingAccount checkingAccount = new CheckingAccount(1000);
//        checkingAccount.deposit(10);
//        checkingAccount.withdraw(9);
//        System.out.println(checkingAccount.getBalance());
        SavingAccount savingAccount = new SavingAccount(1000);
        savingAccount.deposit(100);
        savingAccount.deposit(100);
        savingAccount.deposit(100);
        System.out.println(savingAccount.getBalance());
        savingAccount.deposit(100);
        System.out.println(savingAccount.getBalance());

        savingAccount.earnMonthlyInterest();
        System.out.println(savingAccount.getBalance());
        savingAccount.withdraw(100);

    }
}
package com.kamadaken.pkg.homework;

public class BankAccount {
    private double balance;
    public BankAccount(double initialBalance){
        this.balance = initialBalance;
    }
    //chunkan
    public void deposit(double amount){
        balance += amount;
    }
    public void withdraw(double amount){
        balance -= amount;
    }

    public double getBalance() {
        return balance;
    }

    public void setBalance(double balance) {
        this.balance = balance;
    }
}
package com.kamadaken.pkg.homework;

public class CheckingAccount extends BankAccount{
    public CheckingAccount(double initialBalance) {
        super(initialBalance);
    }

    @Override
    public void deposit(double amount) {
        super.deposit(amount-1);
    }

    @Override
    public void withdraw(double amount) {
        super.withdraw(amount+1);
    }
}
package com.kamadaken.pkg.homework.Homework05;

import com.kamadaken.pkg.homework.BankAccount;

public class SavingAccount extends BankAccount {
    private int count = 3;
    private double rate = 0.01;

    public void earnMonthlyInterest() {//每月初，统计上个月信息 同时将count3
        count = 3;
        super.deposit(getBalance() * rate);

    }

    @Override
    public void deposit(double amount) {
        if (count > 0) {
            super.deposit(amount);
        } else {
            super.deposit(amount - 1);
        }
        count--;
    }

    @Override
    public void withdraw(double amount) {
        if (count > 0) {
            super.withdraw(amount);
        } else {
            super.withdraw(amount + 1);
        }
        count--;
    }

    public SavingAccount(double initialBalance) {
        super(initialBalance);
    }

    public int getCount() {
        return count;
    }

    public void setCount(int count) {
        this.count = count;
    }

    public double getRate() {
        return rate;
    }

    public void setRate(double rate) {
        this.rate = rate;
    }
}
```

![截屏2022-10-26 21.33.46](assets/%E6%88%AA%E5%B1%8F2022-10-26%2021.33.46.png)

```java
package com.kamadaken.pkg.homework;

public class Homework10 {
    public static void main(String[] args) {
        Doctor doctor1 = new Doctor("本田真一", 60, "システムエンジニア", 'M', 80000);
        Doctor doctor2 = new Doctor("本田真一", 60, "システムエンジニア", 'M', 80000);

        System.out.println(doctor1.equals(doctor2));

    }
}
package com.kamadaken.pkg.homework;

import com.sun.org.apache.xpath.internal.objects.XObject;

public class Doctor {
    private String name;
    private int age;
    private String job;
    private char gender;
    private double sal;

    public Doctor(String name, int age, String job, char gender, double sal) {
        this.name = name;
        this.age = age;
        this.job = job;
        this.gender = gender;
        this.sal = sal;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    public String getJob() {
        return job;
    }

    public void setJob(String job) {
        this.job = job;
    }

    public char getGender() {
        return gender;
    }

    public void setGender(char gender) {
        this.gender = gender;
    }

    public double getSal() {
        return sal;
    }

    public void setSal(double sal) {
        this.sal = sal;
    }
    public boolean equals(Object obj){
        if(this == obj){
            return true;

        }

        if(!(obj instanceof Doctor)){
            return false;
        }
        //向下转型，因为obj运行类型是Doctor或其子类
        Doctor doctor = (Doctor) obj;
        return this.name.equals(doctor.name) && this.age ==doctor.age&&
                this.gender==doctor.gender&& this.job.equals(doctor.job)
                &&this.sal==doctor.sal;
    }
}
```

![截屏2022-10-27 14.22.48](assets/%E6%88%AA%E5%B1%8F2022-10-27%2014.22.48.png)

```java
//向上转型：父类引用指向子类对象
Person p = new Student();
p.run();
p.eat();
//向下转型：把指向子类对象的父类引用，转成指向子类对象的子类引用
Student s = (Student)p;
s.run();
s.eat();
s.study();
```

![截屏2022-10-27 16.21.00](assets/%E6%88%AA%E5%B1%8F2022-10-27%2016.21.00.png)

```java
package com.kamadaken.pkg.homework.homework13;

public class Homework13 {
    public static void main(String[] args) {
        Student student = new Student("みんさん", 'M', 24, "G2121039");
        student.printInfo();
        System.out.println("----------------");
        Teacher teacher = new Teacher("亀田", 'm', 63, 36);
        teacher.printInfo();

        //定义多态数组，保存两个学生两个老师，要求年龄从高到低排序

        Person[] people = new Person[4];
        people[0]= new Student("jack", 'm',24,"g2121039");
        people[1]= new Student("jack2", 'm',29,"g2121039");
        people[2]= new Teacher("kanada", 'm',56,30);
        people[3]= new Teacher("hosono", 'm',62,34);

        //创建对象
        Homework13 homework13 = new Homework13();
        homework13.bubbleSort(people);

        //输出
        System.out.println("输出排序后");
        for (int i = 0; i < people.length; i++) {
            System.out.println(people[i].toString());
        }
        System.out.println("---------");
        for (int i = 0; i < people.length; i++) {
            homework13.test(people[i]);
        }



    }
    //定义方法，形参为person类型，功能：调用学生的study或教师的teach方法
    //向下转型和类型判断
    public void test(Person p){
        if(p instanceof Student){
            ((Student) p).study();
        } else if (p instanceof Teacher) {
            ((Teacher) p).teach();

        }else {
            System.out.println("入力エラー");
        }
    }
    //排序
    public void bubbleSort(Person[] people){
        Person tmp = null;
        for (int i = 0; i < people.length-1; i++) {
            for (int j = 0; j <people.length-1-i; j++) {
                if (people[j].getAge()<people[j+1].getAge()){
                    tmp = people[j];
                    people[j]= people[j+1];
                    people[j+1] = tmp;
                }

            }
        }
    }

}
package com.kamadaken.pkg.homework.homework13;

public class Person {
    private String name;
    private char gender;
    private int age;

    public Person(String name, char gender, int age) {
        this.name = name;
        this.gender = gender;
        this.age = age;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public char getGender() {
        return gender;
    }

    public void setGender(char gender) {
        this.gender = gender;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    //编写play方法
    public String play() {
        return name + "遊ぼう";
    }

    //    返回信息的方法
    public String basicInfo() {
        return "姓名： " + name + "\n年龄：" + age + "\n性别" + gender;
    }

    @Override
    public String toString() {
        return "Person{" +
                "name='" + name + '\'' +
                ", gender=" + gender +
                ", age=" + age +
                '}';
    }
}
package com.kamadaken.pkg.homework.homework13;

public class Teacher extends Person{
    private String name;
    private char gender;
    private int age;
    private int work_age;

    public Teacher(String name, char gender, int age, int work_age) {
        super(name, gender, age);
        this.work_age = work_age;
    }



    public int getWork_age() {
        return work_age;
    }

    public void setWork_age(int work_age) {
        this.work_age = work_age;
    }
    public void teach(){
        System.out.println("ちゃんと教えて");
    }

    @Override
    public String play() {
        return super.play() + "治癒系知能ローボト";
    }
    public void printInfo(){
        System.out.println("老师信息：\n");
        System.out.println(super.basicInfo());
        System.out.println("働く年間："+ getWork_age());
        this.teach();
        System.out.println(play());
    }

    @Override
    public String toString() {
        return "Teacher{" +
                "work_age=" + work_age +
                '}' + super.toString();
    }
}
package com.kamadaken.pkg.homework.homework13;

public class Student extends Person {
    private String name;
    private char gender;
    private int age;
    private String stu_id;

    //方法

    public Student(String name, char gender, int age, String stu_id) {
        super(name, gender, age);
        this.stu_id = stu_id;
    }


    public String getStu_id() {
        return stu_id;
    }

    public void setStu_id(String stu_id) {
        this.stu_id = stu_id;
    }
    public void study(){
        System.out.println("JAVAの勉強課程を大好き");
    }

    @Override
    public String play() {
        return super.play() + "サーカー";
    }
    public void printInfo(){
        System.out.println("学生信息：\n");
        System.out.println(super.basicInfo());
        System.out.println("学号" + stu_id);
        this.study();
        System.out.println(play());

    }

    @Override
    public String toString() {
        return "Student{" +
                "stu_id='" + stu_id + '\'' +
                '}'+super.toString();
    }
}
```

在使用[构造方法](https://so.csdn.net/so/search?q=构造方法&spm=1001.2101.3001.7020)来完成对象的初始化的时候，子类对象的实例会默认的调用父类的构造方法.即使我们的super关键字是没有写的.

```java
/*
多态：方法或对象具有多种状态，是oop的第三大特征，是建立在封装和继承 的基础上的
1.方法多态
1）重载体现多态2）重写体现多态
2.对象多态
1）对象 的编译类型和运行类型可以不一致，编译类型在定义时就确定不能变化
2）对象 的运行类型是可以变化的，可以通过 getClass() 来查看运行类型
3）编译类型看=号左边 运行类型看=号右边

16.java的动态绑定机制
1.当调用对象方法时，该方法会和对象的运行类型绑定
2.当调用属性时，哪里声明哪里使用
*/
```

### 小项目：实现房屋出租系统

![截屏2022-10-27 20.17.49](assets/%E6%88%AA%E5%B1%8F2022-10-27%2020.17.49.png)

实现功能的三部曲 [明确完成功能->思路分析->代码实现]

```java
package com.kamedaken.houserent;

import com.kamedaken.houserent.domain.House;
import com.kamedaken.houserent.view.HouseView;

public class HouseRentApp {
    public static void main(String[] args) {
        //创建HouseView对象，并显示主菜单，整个程序的入口
        new HouseView().mainMenu();
        System.out.println("==退出系统==");

    }
}

package com.kamedaken.houserent.view;

import com.kamedaken.houserent.HouseRentApp;
import com.kamedaken.houserent.domain.House;
import com.kamedaken.houserent.service.HouseService;
import com.kamedaken.houserent.utils.Utility;
import com.sun.imageio.plugins.wbmp.WBMPImageReader;

/**
 * 1.显示界面
 * 2.接收用户输入
 * 3.调用HouseService完成对房屋信息对各种操作
 */
public class HouseView {
    private boolean loop = true;//控制显示菜单
    private char key = ' ';//接收用户输入
    private HouseService houseService = new HouseService(2);//设置数组的大小为10

    //根据ID修改房屋信息
    public void update() {
        System.out.println("=======修改房屋信息========");
        System.out.println("请选择待修改的房屋编号");
        int updateId = Utility.readInt();
        if (updateId == -1) {
            System.out.println("=======放弃修改========");
            return;
        }

        //根据输入查找对象
        House house = houseService.findById(updateId);
        if (house == null) {
            System.out.println("==========修改信息不存在=========");
            return;
        }
        System.out.print("名前（" + house.getName() + "):");
        String name = Utility.readString(8, "");
        if (!"".equals(name)) {
            house.setName(name);
        }
        System.out.print("电话（" + house.getPhone() + "):");
        String phone = Utility.readString(12, "");
        if (!"".equals(phone)) {
            house.setPhone(phone);
        }
        System.out.print("地址（" + house.getAddress() + "):");
        String address = Utility.readString(18, "");
        if (!"".equals(address)) {
            house.setAddress(address);
        }
        System.out.print("租金（" + house.getPhone() + "):");
        int rent = Utility.readInt(-1);
        if (!"".equals(rent)) {
            house.setRent(rent);
        }
        System.out.print("状态（" + house.getState() + "):");
        String state = Utility.readString(4, "");
        if (!"".equals(state)) {
            house.setState(state);
        }
    }


    //findHouse()接收输入id
    public void findHouse() {
        System.out.println("======查找房屋信息=========");
        System.out.print("请输入要查找的ID：");
        int findId = Utility.readInt();
        //调用方法
        House house = houseService.findById(findId);
        if (house != null) {
            System.out.println(house);
        } else {
            System.out.println("=======查找的信息不存在=========");
        }
    }


    //完成退出确认
    public void exit() {
        char c = Utility.readConfirmSelection();
        if (c == 'Y') {
            loop = false;
        }
    }


    //编写delHouse()接收用户输入
    public void delHouse() {
        System.out.println("======删除房屋信息======");
        System.out.println("请输入待删除房屋的编号(-1退出):");
        int delId = Utility.readInt();
        if (delId == -1) {
            System.out.println("========放弃删除======");
            return;
        } else {
            char choice = Utility.readConfirmSelection();
            if (choice == 'Y') {
                if (houseService.del(delId)) {
                    System.out.println("=====删除房屋信息成功========");
                } else {
                    System.out.println("========房屋编号不存在=======");
                }

            } else {
                System.out.println("========放弃删除======");
            }
        }
    }


    //编写addHouse（） 接收输入，创建House对象 调用add方法
    public void addHouse() {
        System.out.println("=======添加房屋========");
        System.out.println("姓名");
        String name = Utility.readString(8);
        System.out.println("电话：");
        String phone = Utility.readString(12);
        System.out.println("地址");
        String address = Utility.readString(16);
        System.out.println("月租：");
        int rent = Utility.readInt();
        System.out.println("状态：");
        String sate = Utility.readString(3);
        //创建一个新的House对象，注意id是系统分配
        House house = new House(0, name, phone, address, rent, sate);
        if (houseService.add(house)) {
            System.out.println("=======添加成功========");
        } else {
            System.out.println("========运行失败=======");
        }


    }


    //编写listHouse()显示房屋列表
    public void listHouses() {
        System.out.println("======房屋列表========");
        System.out.println("编号\t\t房主\t\t电话\t\t地址\t\t月租\t\t状态");
        House[] houses = houseService.list();
        for (int i = 0; i < houses.length; i++) {
            if (houses[i] == null) {
                break;

            }
            System.out.println(houses[i]);
        }
        System.out.println("=====房屋列表显示完毕=======");
    }

    //显示主菜
    public void mainMenu() {
        do {
            System.out.println("\n========房屋出租系统========");
            System.out.println("\t\t\t1 新 增 房 源");
            System.out.println("\t\t\t2 查 找 房 源");
            System.out.println("\t\t\t3 删 除 房 屋 信 息");
            System.out.println("\t\t\t4 修 改 房 屋 信 息");
            System.out.println("\t\t\t5 房 屋 列 表");
            System.out.println("\t\t\t6 退    出");
            System.out.println("请输入你的选择（1-6）");
            key = Utility.readChar();
            switch (key) {
                case '1':
                    addHouse();
                    break;
                case '2':
                    findHouse();
                    break;
                case '3':
                    delHouse();
                    break;
                case '4':
                    update();
                    break;
                case '5':
                    listHouses();
                    break;
                case '6':
                    //使用工具类提供的方法
                    exit();
                    break;
            }
        } while (loop);
    }
}
package com.kamedaken.houserent.service;

import com.kamedaken.houserent.domain.House;
import com.kamedaken.houserent.utils.Utility;

/**
 * HouseService.java 类【业务层】
 * //定义House[],保存House对象
 * 1。响应HouseView对调用
 * 2。完成对房屋信息对各种操作
 */
public class HouseService {
    private House[] houses;
    private int houseNums = 1;
    private int idCounter = 1;

    public HouseService(int size) {//构造器
        houses = new House[size];//创建HouseService，制定数组大小
        houses[0] = new House(1, "jack", "112", "片倉町", 31000, "まだ");

    }


    //find方法，返回House对象或null
    public House findById(int findId){
        for (int i = 0; i < houseNums; i++) {
            if(findId == houses[i].getId()){
                return houses[i];

            }
        }
        return null;
    }

    //del方法，删除房屋信息
    public boolean del(int delId){
        int index = -1;
        for (int i = 0; i < houseNums; i++) {
            if(delId == houses[i].getId()){//要删除的房屋id，是数组下标为i的元素
                index = i;

            }
        }
        if(index == -1){//说明不存在
            return false;

        }
        //
        for (int i = index; i < houseNums-1; i++) {
            houses[i] = houses[i+1];

        }
        //把当前存在的房屋信息最后一个null
        houses[--houseNums] = null;
        return true;
    }


    //add方法添加新对象，返回boolean
    public boolean add(House newHouse) {
        //判断是否还能添加
        if (houseNums == houses.length) {//数组溢出
            System.out.println("数组已满");
            return false;

        }
        houses[houseNums++] = newHouse;
        //设计Id自增长机制
        newHouse.setId(++idCounter);
        return true;

    }

    public House[] list() {
        return houses;

    }


}
package com.kamedaken.houserent.domain;

/**
 * House的对象表示房屋信息
 */
public class House {
    private int id;
    private String name;
    private String phone;
    private String address;
    private int rent;
    private String state;

    public House(int id, String name, String phone, String address, int rent, String state) {
        this.id = id;
        this.name = name;
        this.phone = phone;
        this.address = address;
        this.rent = rent;
        this.state = state;
    }

    public int getId() {
        return id;
    }

    public void setId(int id) {
        this.id = id;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public String getPhone() {
        return phone;
    }

    public void setPhone(String phone) {
        this.phone = phone;
    }

    public String getAddress() {
        return address;
    }

    public void setAddress(String address) {
        this.address = address;
    }

    public int getRent() {
        return rent;
    }

    public void setRent(int rent) {
        this.rent = rent;
    }

    public String getState() {
        return state;
    }

    public void setState(String state) {
        this.state = state;
    }
    //方便输出

    @Override
    public String toString() {
        return id +
                "\t\t" + name +
                "\t" +
                "\t" + phone +
                "\t\t" + address +
                "\t" + rent +
                "\t" + state;
    }
}
```

# OOP高级



##类变量

类变量也叫静态变量/静态属性，是该类的所有对象共享的变量，任何一个该类的对象访问它时，取到的都是相同的值，同样任何一个该类的对象去修改它时，修改的也是同一个变量。

### 类变量语法

```java
访问修饰符 staic 数据类型 变量名；
 static 访问修饰符 数据类型变量名
```

### 访问类变量

```java
类名.类变量名
或
对象名.类变量
```

### 类变量细节

1.当需要让某个类的所有对象共享一个变量时，就可以考虑使用类变量：定义学生类

统计学生应该交多少学费

2.类变量与普通属性的区别

类变量是该类所有对象共享的，属性是每个对象独享的

3.加static称为类变量或静态变量，否则称为实例变量

4.类变量可以通过类名.类变量名访问

5.实例变量不能通过类名.类变量名 方式访问

6.**类变量在类加载时就初始化了**，即使不创建对象也可以使用

7.类变量的生命周期是随着类的加载开始，随着类消亡而销毁

## 类方法

```java
package com.Kameda.static_;

public class StaticMethod {
    public static void main(String[] args) {
        Stu min = new Stu("MIN");
        min.payFee(100);

        Stu ka = new Stu("Ka");
        ka.payFee(200);

        Stu.shoeFee();

        //如果希望不创建实例，也可以直接调用某个方法
        //这时适合调用静态方法
        System.out.println(Math.sqrt(9));

        System.out.println(Cal.calSum(1,2));
        //不能用是因为类变量和类方法随着类的加载而加载，
        // 类的加载比对象的创建要找，如果使用this或super的话，会找不到这个对象
    }
}
class Cal{
    public static double calSum(double n1,double n2){
        return n1+n2;

    }
}
class Stu{
    private String name;
    private static double  fee=0;

    public Stu(String name) {
        this.name = name;
    }
    //
    //1.当方法使用static修饰后，方法就是静态方法
    //2。静态方法就可以访问静态变量
    public static void payFee(double fee){
        Stu.fee += fee;//累积
    }
    public static void shoeFee(){
        System.out.println(Stu.fee);
    }
}

```

### 类方法细节

1.类方法和普通方法都是随着类的加载而加载，将信息存储在方法区

类方法中无this的参数

普通方法中隐含着this的参数

2.类方法可以通过类名调用，也可以通过对象名调用

3.普通方法通过对象名调用

4.类方法中不允许使用对象有关的关键字，this，super等

5.类方法只能访问静态变量或静态方法

6.普通成员方法，都能访问。

## main方法

```java
package com.Kameda.static_.main_;

public class Main01 {
    private int n1 = 100;
    private static String name = "Kameda";
    public static void hi(){
        System.out.println("hi方法");
    }
    public static void main(String[] args) {
        System.out.println(name);
        hi();
        //静态方法main要访问本类的非静态成员，需要先创建对象，再调用即可
        Main01 main01 = new Main01();
        System.out.println(main01.n1);
    }
}
/*
1)在main()方法中，我们可以直接调用main方法所在类的静态方法或静态属性。
2) 但是，不能直接访问该类中的非静态成员，必须创建该类的一个实例对象后，才能通过这个对象去访问类中的非静态成员
*/
```

## 代码块

```java
package com.Kameda.static_.codeblock;

public class CodeBlock01 {
    public static void main(String[] args) {
        Movie movie = new Movie("nihao", 30, "jialing");
        //代码块的调用优先于构造器
    }
}
class Movie{
    private String name;
    private double price;
    private String director;
    {
        System.out.println("你好");
        System.out.println("广告");
        System.out.println("电影要开始了——");
    }

    public Movie(String name) {
        this.name = name;
        System.out.println("第一个构造器被调用");
    }

    public Movie(String name, double price) {
        this.name = name;
        this.price = price;
    }

    public Movie(String name, double price, String director) {
        this.name = name;
        this.price = price;
        this.director = director;
        System.out.println("第三个被调用");
    }
}
```

### 代码块注意事项

1）static代码块静态代码块，作用就是对类进行初始化，随着类加载而执行，并且只执行一次，普通代码块，每创建一个对象就执行

```java
package com.Kameda.static_.codeblock;
/*
类被加载的情况举例
创建子类对象实例时，父类也会被加载，先加载父类
 */
public class CodeBlockDetail01 {
    public static void main(String[] args) {
        AA aa = new AA();
        System.out.println(Cat.n1);//使用类的静态成员时,加载类
        new DD();
    }
}
class Animal{
    static {
        System.out.println("Animal执行");
    }
}
class Cat extends Animal{
    public static int n1 = 999;
    static {
        System.out.println("cat静态代码块被执行");
    }
}
class BB{
    static {
        System.out.println("BB被执行");
    }
}
class AA extends BB{
    //静态代码块
    static {
        System.out.println("AA被执行");
    }
}
class DD{
    //普通代码块在new对象时被调用，创建一次，就调用一次
    //普通代码块是构造器的补充
    {
        System.out.println("DD被执行");
    }
}
```

2）类什么时候加载

创建对象实例时（new）

创建子类对象实例时，父类也会被加载

使用类的静态成员时（静态属性，静态方法）

3）普通代码块，在创建对象实例时，会被隐式加载

被创建一次，就会调用一次

如果只是使用类的静态成员时，代码块并不会执行

小结：1.static代码块是类加载时，执行，只会执行一次

2.普通代码块是在创建对象时调用，创建一次，调用一次

3.类加载的三种情况

4）**创建一个对象时，在一个类的调用顺序**

① 调用静态代码块和静态属性初始化

② 调用普通代码块和普通属性的初始化

③ 调用构造器

5）构造器的最前面其实隐含了super（）和调用普通代码块

静态代码块和属性初始化，在类加载时就执行完毕，因此优于构造器和普通代码块执行

6）**当创建一个子类对象时，他们的静态代码块，静态属性初始化，普通代码块，普通属性初始化，构造器的调用顺序如下**

① 父类的静态代码块和静态属性

②子类的静态代码块和静态属性

③ 父类的普通代码块和普通属性初始化

④父类的构造器

⑤ 子类的普通代码块和普通属性初始化

⑥子类的构造方法

7）静态代码块中只能直接调用静态成员，普通代码块可以调用任意成员

## 设计模式

静态方法和属性的经典应用

大量的实践中总结和理论化之后优选的代码结构，编程风格结局问题的思考方式经典的棋谱。

```java
package com.Kameda.single_;

import java.lang.management.GarbageCollectorMXBean;

public class SingTon01 {
    public static void main(String[] args) {
        GirlFriend instance = GirlFriend.getInstance();
        System.out.println(instance);
//
    }
}
class GirlFriend{
    private String name;
    /*
    1.构造器私有化
    2。在类内部直接创建
    3。提供一个公共的静态方法返回gf对象
     */

    //为了在静态方法中能够返回gf对象 设置成静态[饿汉式]
    private static GirlFriend gf = new GirlFriend("siyu");

     private  GirlFriend(String name) {
        this.name = name;
    }

    public static GirlFriend getInstance(){
         return gf;
    }

    @Override
    public String toString() {
        return "GirlFriend{" +
                "name='" + name + '\'' +
                '}';
    }
}
```

```java
package com.Kameda.single_;
/**
 * 懒汉式单例
 */
public class SingleTon02 {
    public static void main(String[] args) {
        Cat instance = Cat.getInstance();
        System.out.println(instance);
    }
}
//希望在程序运行过程中 只能创建一个cat对象
class Cat {
    private String name;
    public static int n1 = 999;
    private static Cat cat;

    /*
    1.构造器私有化
    2。定义static对象
    3.提供一个public static方法
    4.懒汉式当用户调用时才会创建
     */
    private Cat(String name) {
        this.name = name;
    }

    public static Cat getInstance() {
        if (cat == null) {//如果没有创建
            cat = new Cat("dun-dun");
        }
        return cat;
    }

    @Override
    public String toString() {
        return "Cat{" +
                "name='" + name + '\'' +
                '}';
    }
}
```

1.区别在于创建对象的时机不同，懒汉在使用时创建

2.饿汉式不存在线程安全问题，懒汉式存在

3.饿汉式可能存在资源浪费

4.java。lang。Runtime是经典的单例模式源码

## Final

```java
package com.Kameda.final_;
public class Final01 {
    public static void main(String[] args) {
//        E e = new E();
//        e.TAX_RATE = 0.9;

    }
}
//要求A不能被其他类继承
final class A {

}
//class B extends A{}
class C {
    //如果要求hi方法不能被子类重写
    public final void hi() {

    }
}
class D extends C {
//    @Override
//    public void hi() {
//        super.hi();
//    }
}
class E {//当某个属性值不希望被修改
    public final double TAX_RATE = 0.08;
}
class F {//某个局部变量不希望被修改

    public void cry() {
        final double NUM = 0.01;
//        NUM = 9;
    }
}
```

细节

1.final修饰的属性又叫常量，一般用XX_XXX来命名

2.final修饰的属性在定义时必须赋给初始值且以后不可修改，赋值位置可以在

定义时，构造器中，代码块中

3.如果final修饰的属性是静态不能在构造器中赋值

4.final类不能被继承但可以实例化对象

5.类不是final类，但是含有final方法，可以被继承

6.一般来说如果一个类已经是final类，方法不用加final

7.final不能修饰构造器

8.final与static往往搭配使用，编译器底层优化，不会导致类加载提升效率

9。包装类Integer，Double，Float，Boolean，String都是final类

```java
package com.Kameda.final_;

public class FinalExercise01 {
    public static void main(String[] args) {
        Circle circle = new Circle(9);
        System.out.println(circle.calArea());
    }
}
class Circle {
    private double radius;
    private final double PI;//= 3.14;

    public Circle(double radius) {
        this.radius = radius;
    }

    {
        PI = 3.14;
    }

    public double calArea() {
        return PI * radius * radius;
    }
}
```

##抽象类（abstract）

当父类的一些方法不能确定时，用Abstract修饰就是抽象类

```java
package com.Kameda.abstract_;

public class AbstractDetail01 {
    public static void main(String[] args) {
        //抽象类不能被实例化
        //new A();
    }
}
//抽象类不一定要有抽象方法
abstract class A{
    public void eat(){
        System.out.println("qwer");
    }

}
//类中有抽象方法必须修饰为抽象类
//abstract只能修饰类和方法
//抽象类可以有任何成员【抽象类的本质还是类】
//如果一个类继承了抽象类，则他必须实现抽象类中的抽象方法
//抽象方法不能使用关键字 final private static修饰
```

练习

![截屏2022-11-02 15.07.53](assets/%E6%88%AA%E5%B1%8F2022-11-02%2015.07.53.png)

```java
package com.Kameda.abstract_;

public class AbstractExercise01 {
    public static void main(String[] args) {
        Manager jack = new Manager("jack", 999, 9000);
        jack.setBonus(9000);
        jack.work();

        CommonEmployee tom = new CommonEmployee("tom", 999, 9000);
        tom.work();

    }
}
package com.Kameda.abstract_;

 abstract public class Employee {
    private String name;
    private int id;
    private double salary;

    public Employee(String name, int id, double salary) {
        this.name = name;
        this.id = id;
        this.salary = salary;
    }

    public abstract void work();

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getId() {
        return id;
    }

    public void setId(int id) {
        this.id = id;
    }

    public double getSalary() {
        return salary;
    }

    public void setSalary(double salary) {
        this.salary = salary;
    }
}
package com.Kameda.abstract_;

public class Manager extends Employee{
    private double bonus;
    public Manager(String name, int id, double salary) {
        super(name, id, salary);
    }

    @Override
    public void work() {
        System.out.println("经理"+ getName()+"工作中");
    }

    public double getBonus() {
        return bonus;
    }

    public void setBonus(double bonus) {
        this.bonus = bonus;
    }
}
package com.Kameda.abstract_;

public class CommonEmployee extends  Employee{
    public CommonEmployee(String name, int id, double salary) {
        super(name, id, salary);
    }

    @Override
    public void work() {
        System.out.println("普通员工"+getName()+"工作中");
    }
}
```

### 模版设计模式

```java
package com.Kameda.abstract_;

public class TestTemplate {
    public static void main(String[] args) {
        AA aa = new AA();
        aa.calculateTime();//oop基础

        BB bb = new BB();
        bb.calculateTime();
    }
}
package com.Kameda.abstract_;

abstract public class Template {
    public abstract void job();

    public void calculateTime(){
        long start = System.currentTimeMillis();
        job();//动态绑定
        long end = System.currentTimeMillis();
        System.out.println("任务执行时间" +(end-start));
    }
}
package com.Kameda.abstract_;

public class AA extends Template {
    public void job() {
        //得到开始时间
        long num = 0;
        for (long i = 1; i <= 10000000; i++) {
            num += i;
        }

    }
}
package com.Kameda.abstract_;

public class BB extends Template {
    public void job() {
        //得到开始时间
        long num = 0;
        for (long i = 1; i <= 10000000; i++) {
            num *= i;
        }

    }
}
```

##🚩接口

Usb插槽就是现实的接口，厂家统一了大小标准排线等

设计需求在php/。net/go中也大量存在

```java
package com.Kameda.interface_;

public class Interface01 {
    public static void main(String[] args) {
        Camera camera = new Camera();
        Phone phone = new Phone();

        Computer computer = new Computer();
        computer.work(phone);

        computer.work(camera);

    }
}
package com.Kameda.interface_;

public interface UsbInterface {//接口
    //规定接口相关方法,规范
    public  void start();
    public void stop();
}package com.Kameda.interface_;

public interface UsbInterface {//接口
    //规定接口相关方法,规范
    public  void start();
    public void stop();
}
package com.Kameda.interface_;

/**
 * phone类实现UsbInterface接口规定的方法
 */
public class Phone implements UsbInterface{
    @Override
    public void start() {
        System.out.println("手机开始");
    }

    @Override
    public void stop() {
        System.out.println("手机停止");
    }
}
package com.Kameda.interface_;

public class Camera implements UsbInterface{//实现接口，重写接口方法
    @Override
    public void start() {
        System.out.println("相机开始");
    }

    @Override
    public void stop() {
        System.out.println("相机停止");
    }
}
package com.Kameda.interface_;

public class Computer {
    public void work(UsbInterface usbInterface){

        usbInterface.start();
        usbInterface.stop();
    }
}
```

本质 就是给出一些没有实现的方法封装到一起，到某个类要使用时再根据具体器情况重写

​        就是更加抽象的抽象类，抽象类里的方法可以有方法体。

体现了程序设计的多态和高内聚低耦合的设计思想

jdk8。0后接口类可以有静态方法，默认方法，即可以有方法的具体实现

```java
public interface DBInterface { //项目经理
public void connect();//连接方法
public void close();//关闭连接 }
package com.hspedu.interface_;
//A 程序
public class MysqlDB implements DBInterface {
@Override
public void connect() {
System.out.println("连接 mysql");
   }
@Override
public void close() {
System.out.println("关闭 mysql"); }
}

//B 程序员连接 Oracle
public class OracleDB implements DBInterface{
@Override
public void connect() {
System.out.println("连接 oracle"); }
@Override
public void close() {
System.out.println("关闭 oracle"); }
}
package com.hspedu.interface_;
public class Interface03 {
public static void main(String[] args) {
    MysqlDB mysqlDB = new MysqlDB(); t(mysqlDB);
OracleDB oracleDB = new OracleDB(); t(oracleDB);
}
public static void t(DBInterface db) { db.connect();
db.close(); }
}
```

###细节

1.接口不能被实例化

2.接口中所有的方法是public方法，接口中抽象方法可以不应abstract修饰

3.一个普通类实现接口，就必须将该接口的所有方法实现

4.抽象类实现接口可以不用实现接口的方法

5.一个类可以实现多个接口

6.接口中的属性只能是final，而且是public static final修饰符

7.接口中属性的访问形式：接口。属性名

8.接口不能继承其他类，但可以继承多个别的接口（类和接口是实现关系）

9.接口的修饰符只能是public和默认，这一点和类一样

###实现接口VS继承类

```java
package com.Kameda.interface_;

public class ExtendsVsInterface {
    public static void main(String[] args) {
        LittleMonkey wukong = new LittleMonkey("wukong");
        wukong.climbing();
        wukong.swimming();
        wukong.flying();
    }
}

//接口
interface Fishable {
    void swimming();
}
interface Birdable{
    void flying();
}

class Monkey {
    private String name;

    public Monkey(String name) {
        this.name = name;
    }

    public String getName() {
        return name;
    }

    public void climbing() {
        System.out.println(name + "会爬树");
    }
}

/**
 * 继承自动拥有父类功能
 * 子类需要拓展功能可以通过实现接口方式拓展
 * 实现接口是但继承机制的补充
 */
class LittleMonkey extends Monkey implements Fishable,Birdable {//单继承

    public LittleMonkey(String name) {
        super(name);
    }

    @Override
    public void swimming() {
        System.out.println(getName() + "游泳");
    }

    @Override
    public void flying() {
        System.out.println(getName()+"通过学习会飞翔");
    }
}
```

继承的价值：解决代码的复用性和可维护性

接口的价值：设计好规范方法。即更加灵活

比继承更灵活，一定程度上可以实现代码的解藕

### 接口的多态特性

1.多态参数

UsbInterface usb，即可以接收手机对象又可以接收相机对象，体现了接口的多态

2.多态数组

```java
package com.Kameda.interface_;

public class InterfacePloyArr {
    public static void main(String[] args) {
        //多态数组
        Usb[] usbs = new Usb[2];
        usbs[0] = new Phone_();
        usbs[1] = new Camera_();
        /*
给 Usb 数组中，存放 Phone 和
请遍历 Usb 数组，如果是 Phone 对象，除了调用 Usb 接口定义的方法外， 还需要调用 Phone 特有方法 call
*/
        for (int i = 0; i < usbs.length; i++) {
            usbs[i].work();
            //类型判断 向下转型
            if(usbs[i] instanceof Phone_){//判断运行类型
                ((Phone_) usbs[i]).call();
            }
        }
    }
}

interface Usb {
    void work();
}

class Phone_ implements Usb {
    public void call() {
        System.out.println("手机可以打电话");
    }

    @Override
    public void work() {
        System.out.println("手机工作中");
    }
}

class Camera_ implements Usb {
    @Override
    public void work() {
        System.out.println("相机工作中");
    }
}
```

3.接口的多态传递

```java
package com.Kameda.interface_;

/**
 * 演示多态传递现象
 */
public class InterfacePloyPass {
    public static void main(String[] args) {
        IG ig = new Teacher();//接口类型的变量可以指向，实现了该接口的类的对象实例
        //如果IG继承了IH接口，而Teacher类实现了IG接口
        //那么Teacher也实现了IH接口，这就是多态传递现象
        IH ih = new Teacher();

    }
}

interface IH {
    void eat();
}

interface IG extends IH {
}

class Teacher implements IG {
    @Override
    public void eat() {

    }
}
```

练习

```java
public class InterfaceExercise02 {
public static void main(String[] args) {
} }
interface A { // 1min 看看 int x = 0;
} //想到 等价 public static final int x = 0;
class B {
int x = 1;
} //普通属性
class C extends B implements A { public void pX() {
//System.out.println(x); //错误，原因不明确 x
    //可以明确的指定 x
//访问接口的 x 就使用 A.x //访问父类的 x 就使用 super.x System.out.println(A.x + " " + super.x);
}
public static void main(String[] args) { new C().pX();
} }
```

## 🚩内部类

如果定义类在局部位置(方法中/代码块) :(1) 局部内部类 (2) 匿名内部类

定义在成员位置 (1) 成员内部类 (2) 静态内部类

类的五大成员：属性，方法，构造器，代码块，内部类

```java
package com.Kameda.InnerClass;

public class InnerClass01 {
    public static void main(String[] args) {

    }
}
class Outer{//外部类
    private int n1  = 100;

    public Outer(int n1) {
        this.n1 = n1;
    }

    public void m1(){
        System.out.println("m1()");
    }
    {
        System.out.println("代码块");
    }
    class Inner{//内部类

    }
}
```

### 局部内部类

```java
package com.Kameda.InnerClass;

public class LocalInnerClass {
    public static void main(String[] args) {
        Outer02 outer02 = new Outer02();
        outer02.m1();
        System.out.println(outer02.hashCode());
    }
}
class Outer02{//外部类
    private int n1 = 100;
    private void m2(){
        System.out.println("m2");
    }
    public void m1(){
        //1.局部内部类定义在外部类的局部位置，通常在方法中
        //4.作用域：仅仅定义在它 的方法体或代码块中
        String name= "vvv";
        final class Inner02{//3.相当于局部变量，不能添加访问修饰符，final修饰可以
            //2.可以访问外部类的所有成员，包括是私有的
            private int n1 = 800;
            public void f1(){
                //5.局部内部类可以直接访问外部类的成员
                //7.如果外部类和局部内部类的成员重名时，默认遵循就近原则
                //如果想访问外部类成员时，使用（this.成员）访问
                System.out.println("n1=" + n1);
                //Outer02.this 本质就是外部类的对象，哪个对象调用m1。Outer01.this就是哪个对象
                System.out.println(Outer02.this.n1);
                System.out.println(Outer02.this.hashCode());
                //m2
                m2();
            }
        }
        //6。外部类在方法中，可以创建Inner02对象，然后嗲用方法即可
        Inner02 inner02 = new Inner02();
        inner02.f1();

    }


}
```

### **匿名内部类**

```java
package com.Kameda.InnerClass;

/**
 * 演示匿名内部使用
 */
public class AnonymousInnerClass {
    public static void main(String[] args) {
        Outer04 outer04 = new Outer04();
        outer04.method();
    }
}

class Outer04 {
    private int n1 = 10;

    public void method() {
        //基于接口的匿名内部类
//        Tiger tiger = new Tiger();
//        tiger.cry();//每个类只使用一次
        IA tiger = new IA() {//简化开发 运行类型就是匿名内部类
            @Override
            public void cry() {
                System.out.println("老虎叫");
            }
        };
        //jdk底层分配  匿名内部类类名$1,马上创建了Outer04$1实例，并把地址返回给tiger
        //匿名内部类使用一次就不能再使用
        System.out.println("tiger运行类型" + tiger.getClass());
        tiger.cry();
//        new Outer04$1; 用完即死

        //演示基于类的匿名内部类
        /*
        class Outer04$2 extends Father{
        }
         */
        //同时直接返回匿名内部类的对象
        Father father = new Father("MIN") {//传递给构造器
            @Override
            public void test() {
                System.out.println("匿名内部类重写test方法");
            }
        };
        System.out.println(father.getClass());
        father.test();
        //基于抽象类的匿名内部类
        Animal animal = new Animal() {
            @Override
            void eat() {
                System.out.println("小狗吃骨头");
            }
        };
        animal.eat();

    }
}

interface IA {
    public void cry();
}

//class Tiger implements IA{
//    @Override
//    public void cry() {
//        System.out.println("老虎叫");
//    }
//}
class Father {
    public Father(String name) {

    }

    public void test() {

    }
}

abstract class Animal {
    abstract void eat();
}
```

#### 细节

```java
package com.Kameda.InnerClass;

import com.sun.scenario.effect.impl.sw.java.JSWBlend_SRC_OUTPeer;

public class AnonymousInnerClassDetail {
    public static void main(String[] args) {
        Outer05 outer05 = new Outer05();
        outer05.f1();
    }
}
class Outer05{
    private int i = 99;
    public void f1(){
        //不能添加访问修饰符 地位相当于局部变量
        //作用域在它 的方法和代码块中

        Person person = new Person() {
            private int i = 88;
            @Override
            public void hi() {
                System.out.println("匿名内部类");
                System.out.println(i);
                System.out.println(Outer05.this.i);
            }
        };
        person.hi();//动态绑定

        //也可以直接调用
        new Person(){
            @Override
            public void hi() {
                System.out.println("直接调用");

            }

            @Override
            public void ok(String str) {
                super.ok(str);
            }
        }.ok("MIN");
    }
}
class Person{
    public void hi(){
        System.out.println("Person hi()");
    }
    public void ok(String str){
        System.out.println("person ok()");
    }
}
```

练习

```java
package com.Kameda.InnerClass;

public class InnerExercise02 {
    public static void main(String[] args) {
/*
1.有一个铃声接口 Bell，里面有个 ring 方法。(右图)
2.有一个手机类 Cellphone，具有闹钟功能 alarmClock，参数是 Bell 类型(右图)
3.测试手机类的闹钟功能，通过匿名内部类(对象)作为参数，打印:懒猪起床了
4.再传入另一个匿名内部类(对象)，打印:小伙伴上课了
*/
        CellPhone cellPhone = new CellPhone();
        /**
         * 1。传递的是实现了Bell接口的匿名内部类
         * 2。重写了ring（）
         * 3。
         */
        cellPhone.alarmClock(new Bell() {
            @Override
            public void ring() {
                System.out.println("懒猪起床");
            }
        });
        cellPhone.alarmClock(new Bell() {
            @Override
            public void ring() {
                System.out.println("小伙伴上课");
            }
        });
    }
}
interface Bell{
    void ring();
}
class CellPhone{
    public void alarmClock(Bell bell){
        System.out.println(bell.getClass());
        bell.ring();
    }
}
```

### 成员内部类

```java
package com.Kameda.InnerClass;

public class MemberInnerClass01 {
    public static void main(String[] args) {
        Outer08 outer08 = new Outer08();
        outer08.t1();
        //外部其他类，使用成员内部类的三种方式
        //解读
        //new Inner08();相当于外部类的成员
        Outer08.Inner08 inner08 = outer08.new Inner08();
        //2 在外部中编写一个方法返回Inner08的实例
        Outer08.Inner08 inner08Instance = outer08.getInner08Instance();
        inner08Instance.say();
    }
}

class Outer08 {
    private int n1 = 10;
    public String name = "MIN";

    //1。成员内部类，定义在外部类的成员位置
    //2。可以添加任意访问修饰符
    //3。作用域在整个类体中
    class Inner08 {//成员内部类
        private int sal = 90000;
        private int n1 = 66;

        public void say() {
            //可以直接访问外部类的所有成员，包括私有的
            System.out.println(n1 + name);
            //内部类与外部类重名，遵循就近原则
            //外部类名.this.成员访问
        }
    }

    //使用成员内部类
    //创建成员内部类的对象，直接调用
    public void t1() {
        Inner08 inner08 = new Inner08();
        inner08.say();
        System.out.println(inner08.sal);

    }

    public Inner08 getInner08Instance() {
        return new Inner08();
    }
}
```

### 静态内部类

```java
package com.Kameda.InnerClass;

public class StaticInnerClass {
    public static void main(String[] args) {
        Outer10 outer10 = new Outer10();
        outer10.m1();
        //外部其他类访问静态内部类
        //1.满足权限类名直接访问
        Outer10.Inner10 inner10 = new Outer10.Inner10();
        inner10.say();
        //2。写方法，可以返回静态内部类的对象实例
        Outer10.Inner10 inner101 = outer10.getInner10();
        inner101.say();

        Outer10.Inner10 inner10_ = Outer10.getInner10_();
        inner10_.say();//不想创建外部类
    }
}

class Outer10 {
    private int n1 = 10;
    private static String name = "min";

    private static void cry() {

    }

    //1.放在外部类的成员位置
    //2。用static修饰
    //3.不能访问非静态成员
    //4.可以添加访问修饰符修饰
    //5.作用域为整个类体
    //成员内部类，静态内部类 是放在成员位置上本质，就是一个成员
    static class Inner10 {
        private static String name = "Kameda";
        public void say() {
            System.out.println(name);
            cry();
            System.out.println(Outer10.name);//静态无需this
        }

    }

    public void m1() {//访问静态内部类方式，创建对象在访问
        Inner10 inner10 = new Inner10();
        inner10.say();
    }

    public Inner10 getInner10() {
        return new Inner10();
    }

    public static Inner10 getInner10_() {
        return new Inner10();
    }
}
```

# 枚举和注解

##枚举

enumeration：一组常量的集合；属于一种特殊的类，里面只包含一组有限的特定的对象

###自定义实现枚举

```java
package com.Kameda.enum_;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class Enumeration02 {
    public static void main(String[] args) {
        System.out.println(Season.AUTUMN);

    }
}
//演示自定义枚举
class Season {
    private String name;
    private String desc;
    public static Season SPRING = new Season("Spring", "warm");
    public static Season WINTER = new Season("Winter", "clod");
    public static Season AUTUMN = new Season("Summer", "hot");
    public static Season SUMMER = new Season("Autumn", "clam");
    /*
    1.构造器私有化
    2。去掉setXxx方法，防止属性被修改
    3。在Season内部直接创建固定对象
    4.加final final加static会底层优化不加载类
     */
     private Season(String name, String desc) {
        this.name = name;
        this.desc = desc;
    }

    public String getName() {
        return name;
    }
    public String getDesc() {
        return desc;
    }

    @Override
    public String toString() {
        return "Season{" +
                "name='" + name + '\'' +
                ", desc='" + desc + '\'' +
                '}';
    }
}
/*
1.不需要提供setXXX方法，因为枚举对象值通常为只读
2.对枚举对象/属性使用final+stasic共同修饰，实现底层优化
3.枚举对象名通常使用全部大写
4.枚举对象根据需要也可以有多个变量
*/
```

###enum关键字实现枚举

```java
package com.Kameda.enum_;

import javax.swing.*;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class Enumeration03 {
    public static void main(String[] args) {
        System.out.println(Season.AUTUMN);
    }
}
enum Season02 {
    //常量名 实参列表
    SPRING("春天","Warm"),
    WINTER("Winter", "clod"),
    AUTUMN("Autumn", "clam"),
    SUMMER("Summer", "hot");
    //写在前面
    private String name;
    private String desc;
//    public static Season SPRING = new Season("Spring", "warm");
//    public static Season WINTER = new Season("Winter", "clod");
//    public static Season AUTUMN = new Season("Summer", "hot");
//    public static Season SUMMER = new Season("Autumn", "clam");
    //如果使用了 enum 来实现枚举类
//1. 使用关键字 enum 替代 class
//2. public static final Season SPRING = new Season("春天", "温暖") 直接使用 // SPRING("春天", "温暖") 解读 常量名(实参列表)
//3. 如果有多个常量(对象)， 使用 ,号间隔即可
//4. 如果使用 enum 来实现枚举，要求将定义常量对象，写在前面
//5. 如果我们使用的是无参构造器，创建常量对象，则可以省略 ()

    private Season02(String name, String desc) {
        this.name = name;
        this.desc = desc;
    }

    public String getName() {
        return name;
    }
    public String getDesc() {
        return desc;
    }

    @Override
    public String toString() {
        return "Season{" +
                "name='" + name + '\'' +
                ", desc='" + desc + '\'' +
                '}';
    }
}
```

###enum 关键字实现枚举注意事项

1.当我们使用enum 关键字开发一个枚举类时，默认会继承Enum类, 而且是一个final 类[如何证明],

2.传统的 public static final Season2 SPRING = new Season2("春天", "温暖"); 简化成 SPRING("春天", "温暖")， 这里必 须知道，它调用的是哪个构造器.

3.如果使用无参构造器创建枚举对象，则实参列表和小括号都可以省略

4.当有多个枚举对象时，使用,间隔，最后有一个分号结尾 5) 枚举对象必须放在枚举类的行首.

###enum常2用方法说明

1.  toString:Enum 类已经重写过了，返回的是当前对象 名,子类可以重写该方法，用于返回对象的属性信息
2.  name:返回当前对象名(常量名)，子类中不能重写
3.   ordinal:返回当前对象的位置号，默认从 0 开始
4.   values:返回当前枚举类中所有的常量
5. valueOf:将字符串转换成枚举对象，要求字符串必须为已有的常量名，否则报异常!
6. compareTo:比较两个枚举常量，比较的就是编号!

```JAVA
package com.Kameda.enum_;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 * 演示Enum类的各种使用方法
 */
public class EnumMethod {
    public static void main(String[] args) {
        Season02 autumn = Season02.AUTUMN;
        System.out.println(autumn.name());
        //输出的是该枚举对象的编号 从0开始编号
        System.out.println(autumn.ordinal());
        //反编译可以看到values方法 返回Season2【】
        Season02[] values = Season02.values();
        System.out.println("=====遍历取出枚举对象=======");
        for(Season02 season:values){//增强for循环
            //依次从数组中取出数据赋给对象，取出完毕则退出
            System.out.println(season);

        }
        //将字符串转换成枚举对象
        //根据输入的字符串到枚举对象中查找，没有则报错
        Season02 season02 = Season02.valueOf("AUTUMN");
        System.out.println(season02);

        //compareto：比较两个枚举常量，比较的就是编号
        System.out.println(Season02.AUTUMN.compareTo(Season02.SPRING));
        //输出的结果是编号相减
    }
}

```

### 练习

```java
package com.Kameda.enum_;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class EnumExercise02 {
    public static void main(String[] args) {
        //获取所有编剧对象
        Week[] weeks = Week.values();
        System.out.println("====全部週の情報以下======");
        for(Week week : weeks){
            System.out.println(week);
        }

    }
}
 /*
       声明 Week 枚举类，其中包含星期一至星期日的定义;
       MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY, SATURDAY, SUNDAY;
       使用 values 返回所有的枚举数组, 并遍历 , 输出左图效果
       */
enum  Week{
    MONDAY("月曜日"),TUESDAY("火曜日"),WEDNESDAY("水曜日"),
     THURSDAY("木曜日"),FRIDAY("金曜日"),SATURDAY("土曜日"),
     SUNDAY("日曜日");
     private String name;

    private Week(String name) {
         this.name = name;
     }

     @Override
     public String toString() {
         return  name;
     }
 }
```

### enum实现接口

```java
package com.Kameda.enum_;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class EnumDetail {
    public static void main(String[] args) {
        Music.CLASSICMUSIC.playing();
    }
}
class A{

}
//1.使用 enum 关键字后，就不能再继承其它类了，因为 enum 会隐式继承 Enum，而 Java 是单继承机制 //enum Season3 extends A {
//
//}
//2.enum 实现的枚举类，仍然是一个类，所以还是可以实现接口的.
interface  IPlaying{
    public void playing();
}
enum Music implements IPlaying{
    CLASSICMUSIC;

    @Override
    public void playing() {

    }
}
```

## 注解（Annotation）

1. 注解(Annotation)也被称为元数据(Metadata)，用于修饰解释包、类、方法、属性、构造器、局部变量等数据信息。

2. 和注释一样，注解不影响程序逻辑，但注解可以被编译或运行，相当于嵌入在代码中的补充信息。

3. 在JavaSE中，注解的使用目的比较简单，例如标记过时的功能，忽略警告等。在JavaEE中注解占据了更重要的角色，例如用来配置应用程序的任何切面，代替 java EE 旧版中所遗留的繁冗代码和 XML 配置等。

    

使用 Annotation 时要在其前面增加 @ 符号, 并把该 Annotation 当成一个修饰符使用。用于修饰它支持的程序元 素

###三个基本的 Annotation:

1.   @Override: 限定某个方法，是重写父类方法, 该注解只能用于方法
2.   @Deprecated: 用于表示某个程序元素(类, 方法等)已过时
3.   @SuppressWarnings: 抑制编译器警告

```java
package com.Kameda.annotation_;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class Override_ {
    public static void main(String[] args) {

    }
}

class Father {//父类

    public void fly() {
        System.out.println("Father fly...");
    }

}

class Son extends Father {//子类

    @Override //说明:表示重写了父类的fly方法
    /*
    1。如果写了@Override注解，编译器会检查是否重写父类方法，如果没有重写，
    编译器报错
    2。@Target(ElementType.METHOD)
      @Retention(RetentionPolicy.SOURCE)
      public @interface Override {
       }
    @interface表示一个注解类
    3。@Target修饰注解的注解 成为元注解
     */
    public void fly() {
        System.out.println("Son fly....");
    }
}
```

@Deprecated 过时注解案例

```java
package com.Kameda.annotation_;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class Deprecated {
    public static void main(String[] args) {
        A a = new A();
        System.out.println(a.n1);
    }
}
//表示该元素已经过时，不推荐使用
//查看注解类的源码
//可以修饰方法，类。字段，包，参数等
//可以做版本兼容过度使用
/*
@Documented
@Retention(RetentionPolicy.RUNTIME)
@Target(value={CONSTRUCTOR, FIELD, LOCAL_VARIABLE, METHOD, PACKAGE, PARAMETER, TYPE})
public @interface Deprecated {
}
 */
@java.lang.Deprecated
class A{
    public int n1 =10;
    @java.lang.Deprecated
    public void hi(){

    }
}
```

@SuppressWarning注解案例

```java
package com.Kameda.annotation_;

import java.util.ArrayList;
import java.util.List;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class SuppressWarnings_ {

    //使用注解抑制警告信息
    //可以指定等警告类型是
// //all，抑制所有警告
// //boxing，抑制与封装/拆装作业相关的警告
// //cast，抑制与强制转型作业相关的警告
// //dep-ann，抑制与淘汰注释相关的警告
// //deprecation，抑制与淘汰的相关警告
// //fallthrough，抑制与 switch 陈述式中遗漏 break 相关的警告
// //finally，抑制与未传回 finally 区块相关的警告
// //hiding，抑制与隐藏变数的区域变数相关的警告
// //incomplete-switch，抑制与 switch 陈述式(enum case)中遗漏项目相关的警告
// //javadoc，抑制与 javadoc 相关的警告
    // //nls，抑制与非 nls 字串文字相关的警告
// //null，抑制与空值分析相关的警告
// //rawtypes，抑制与使用 raw 类型相关的警告
// //resource，抑制与使用 Closeable 类型的资源相关的警告
// //restriction，抑制与使用不建议或禁止参照相关的警告
// //serial，抑制与可序列化的类别遗漏 serialVersionUID 栏位相关的警告
// //static-access，抑制与静态存取不正确相关的警告
// //static-method，抑制与可能宣告为 static 的方法相关的警告
// //super，抑制与置换方法相关但不含 super 呼叫的警告
// //synthetic-access，抑制与内部类别的存取未最佳化相关的警告
// //sync-override，抑制因为置换同步方法而遗漏同步化的警告
// //unchecked，抑制与未检查的作业相关的警告
// //unqualified-field-access，抑制与栏位存取不合格相关的警告
// //unused，抑制与未用的程式码及停用的程式码相关的警告
    //4。作用范围与放置位置有关
    //5。源码
    /*
    @Target({TYPE, FIELD, METHOD, PARAMETER, CONSTRUCTOR, LOCAL_VARIABLE})
    @Retention(RetentionPolicy.SOURCE)
    public @interface SuppressWarnings {
        String[] value();
}
     */
    @SuppressWarnings({"unchecked", "rawtypes", "unused"})
    public static void main(String[] args) {
        List list = new ArrayList();
        list.add("jack");
        list.add("tom");
        list.add("mary");
        int i;
        System.out.println(list.get(1));
    }
}
```

###Jdk的元注解

JDK 的元 Annotation 用于修饰其他 Annotation

1. Retention //指定注解的作用范围，三种 SOURCE,CLASS,RUNTIME
2. Target // 指定注解可以在哪些地方使用
3. Documented //指定该注解是否会在 javadoc 体现
4. Inherited //子类会继承父类注解

只能用于修饰一个 Annotation 定义, 用于指定该 Annotation 可以保留多长时间, @Rentention 包含一个 RetentionPolicy 类型的成员变量, 使用 @Rentention 时必须为该 value 成员变量指定值:
 @Retention 的三种值

1.   RetentionPolicy.SOURCE: 编译器使用后，直接丢弃这种策略的注释
2.   RetentionPolicy.CLASS: 编译器将把注解记录在 class 文件中. 当运行 Java 程序时, JVM 不会保留注解。这是默认值
3. RetentionPolicy.RUNTIME:编译器将把注解记录在 class 文件中. 当运行 Java 程序时, JVM 会保留注解. 程序可以通过反射获取该注解

##练习

```java
package com.Kameda.homework;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class HomeWork01 {
    public static void main(String[] args) {
        Car car = new Car();
        Car car1 = new Car(100);
        System.out.println(car);
        System.out.println(car1);
    }
}
class Car{
    double price = 10;
    static String color = "white";
    public String toString(){
        return price+ "\t"+color;
    }
    public Car(){
        this.price = 9;
        this.color = "red";
    }
    public Car(double price) {
        this.price = price;
    }

}
```

```java
package com.Kameda.homework;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class HomeWork02 {
    public static void main(String[] args) {

    }
}
class Frock{
    private int serialNumber;
    private static int currentNum = 100000;
    public Frock() {
        serialNumber = getNextNum();
    }
    public static int getNextNum(){
        currentNum+=100;
        return  currentNum;
    }

    public int getSerialNumber() {
        return serialNumber;
    }

}
class TestFrock{
    public static void main(String[] args) {
        System.out.println(Frock.getNextNum());
        System.out.println(Frock.getNextNum());
        Frock frock = new Frock();
        Frock frock1 = new Frock();
        Frock frock2 = new Frock();
        System.out.println(frock.getSerialNumber());
        System.out.println(frock1.getSerialNumber());
        System.out.println(frock2.getSerialNumber());
    }
}
```

```java
package com.Kameda.homework;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class HomeWork03 {
    public static void main(String[] args) {
        Cat cat = new Cat();
        Dog dog = new Dog();
        cat.shout();
        dog.shout();
    }
}

abstract class Animal {
    public abstract void shout();
}

class Cat extends Animal {
    public void shout() {
        System.out.println("みいおみいお");
    }
}

class Dog extends Animal {
    @Override
    public void shout() {
        System.out.println("わんわん");
    }
}
```

```java
package com.Kameda.homework;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class HomeWork04 {
    public static void main(String[] args) {
        CellPhone cellPhone = new CellPhone();
        //
        cellPhone.testWork(new ICalculate() {
            @Override
            public double work(double n1, double n2) {
                return n1*n2;
            }
        },8,9);
    }
}
/*
1.计算器接口具有work方法，功能是运算，有一个手机类CellPhone。
  定义方法testWork测试计算功能，嗲用计算接口work的方法
2。要求调用CellPhone对象的testWork方法，使用匿名内部类
 */
interface ICalculate{
    public double work(double n1,double n2);
}
class CellPhone{
    public void testWork(ICalculate iCalculate,double n1,double n2){
        double result = iCalculate.work(n1, n2);
        System.out.println("結果"+result);
    }
}
```

```java
package com.Kameda.homework;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class HomeWork05 {
    public static void main(String[] args) {
        A a = new A();
        a.f1();
    }
}
class A{
    private  String NAME="こんにちは";
    public void f1(){
        class B{
            private final String NAME ="MIN";
            public void show(){
                System.out.println("NAME" + NAME +"外部"+ A.this.NAME);
            }
        }
        B b = new B();
        b.show();
    }
}
```

```java
package com.Kameda.homework;

import com.sun.corba.se.impl.orbutil.HexOutputStream;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class HomeWork06 {
    public static void main(String[] args) {
        Person min = new Person("MIN", new Boat());
        min.common();
        min.passRiver();
        min.passFireHill();
    }
}

interface Vehicles {
    public void work();
}

class Horse implements Vehicles {
    @Override
    public void work() {
        System.out.println("一般的に馬を使う");
    }
}

class Boat implements Vehicles {
    @Override
    public void work() {
        System.out.println("川を渉時船を使う");
    }
}

class Plane implements Vehicles {
    @Override
    public void work() {
        System.out.println("火焰山飞机");
    }
}

class VehiclesFactory {
    private static Horse horse = new Horse();//饿汉式

    public static Horse getHorse() {
        //马始终是同一批

        return horse;
    }

    public static Boat getBoat() {
        return new Boat();
    }
    public static Plane getPlane(){
        return new Plane();
    }
}

class Person {
    private String name;
    private Vehicles vehicles;
    //创建人对象事先分配交通工具

    public Person(String name, Vehicles vehicles) {
        this.name = name;
        this.vehicles = vehicles;
    }

    public void passRiver() {
        //先取得一个船
//        Boat boat = VehiclesFactory.getBoat();
//        boat.work();
        //只要不是船就要获取
        if (!(vehicles instanceof Boat)) {
            vehicles = VehiclesFactory.getBoat();

        }
        vehicles.work();
    }

    public void common() {
        //判断
        if (!(vehicles instanceof Horse)) {
            vehicles = VehiclesFactory.getHorse();
        }
        //体现接口调用
        vehicles.work();
    }

    public void passFireHill() {
        if (!(vehicles instanceof Plane)){
            vehicles =VehiclesFactory.getPlane();
        }
        vehicles.work();
    }
}
```

```java
package com.Kameda.homework;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class HomeWork07 {
    public static void main(String[] args) {
        Car2 car2 = new Car2(60);
        car2.getAir().flow();
        Car2 car21 = new Car2(-9);
        car21.getAir().flow();
        Car2 car22 = new Car2(20);
        car22.getAir().flow();
    }
}
/*

 */
class Car2{
    private double temperature;

    public Car2(double temperature) {
        this.temperature = temperature;
    }

    class Air{
        public void flow(){
            if(temperature>40){
                System.out.println("エアコンの冷房");
            } else if (temperature<0) {
                System.out.println("エアコンの暖房");
            }else{
                System.out.println("温度正常、エアコン閉めて");
            }
        }
    }
    public Air getAir(){
        return new Air();
    }
}
```

```java
package com.Kameda.homework;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class HomeWork08 {
    public static void main(String[] args) {
        //枚举值的switch使用方法
        Color green = Color.YELLOW;
        green.show();
       //switch()中放入枚举对象
        switch (green) {
            case RED:
                System.out.println("匹配到黄色");
                break;
            case GREEN:
                System.out.println("匹配到绿色");
                break;
            default:
                System.out.println("没有匹配到");
        }
    }
}

interface IMIN {
    public void show();
}

enum Color implements IMIN {
    RED(255, 0, 0),
    BLUE(0, 0, 255),
    YELLOW(255, 255, 0),
    GREEN(0, 255, 0);

    private int redValue;
    private int greenValue;
    private int blueValue;

    Color(int redValue, int greenValue, int blueValue) {
        this.redValue = redValue;
        this.greenValue = greenValue;
        this.blueValue = blueValue;
    }


    @Override
    public void show() {
        System.out.println("属性值" + redValue + greenValue + blueValue);
    }
}
```

#异常（Exception）

java语言中，将程序执行中发生的不正常情况称为“异常”。

Error（错误）：jvm无法解决的严重问题。如系统错误，资源耗尽等严重情况StackOverflowError和oom，Error是严重错误，程序会崩溃。

Exception：其他编程错误或偶然外在因素导致的一般性问题，可以使用针对性的代码进行处理。。例如空指针访问，试图读取不存在的文件，网络连接中断等。Exception又分为两大类运行时异常，编译时异常。

## 异常体系图

![截屏2022-11-08 16.46.00](assets/%E6%88%AA%E5%B1%8F2022-11-08%2016.46.00.png)

1.运行时异常，编译器检查不出来。一般指编程时的逻辑错误，尽量避免。java。lang.Runtime

Exception类及其子类都是运行时的异常

2.对于运行时异常可以不做处理，，若全处理对程序的可读性和运行效率产生影响。

3.编译时异常，是编译器要求必须处置的异常。

## 常见的运行时异常

1. \1)  NullPointerException 空指针异常
2. \2)  ArithmeticException 数学运算异常
3. \3)  ArrayIndexOutOfBoundsException 数组下标越界异常
4. \4)  ClassCastException 类型转换异常
5. \5)  NumberFormatException 数字格式不正确异常[]

```java
package com.Kameda.Exception_;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class ClassCastException {
    public static void main(String[] args) {
        A b = new B();
        B b2 = (B)b;
        C c2 =(C)b;//抛出异常
    }
}
class A{}
class B extends A{

}
class C extends A{}

```

## 常见的编译时异常

![截屏2022-11-08 16.55.03](assets/%E6%88%AA%E5%B1%8F2022-11-08%2016.55.03.png)

##异常处理

1）try-catch-finally

自己捕获自行处理

<img src="assets/%E6%88%AA%E5%B1%8F2022-11-08%2017.01.26.png" alt="截屏2022-11-08 17.01.26" style="zoom:67%;" />

2）throws

将发生的异常抛出，交给调用者处理，最顶级的处理者是JVm

<img src="assets/%E6%88%AA%E5%B1%8F2022-11-08%2017.02.00.png" alt="截屏2022-11-08 17.02.00" style="zoom:67%;" />

try-catch 异常处理及细节

```java
package com.Kameda.try_;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class TryCatchDetail {
    public static void main(String[] args) {

        try {
            String str = "8989";
            int a = Integer.parseInt(str);
            System.out.println("数字:" + a);
        } catch (NumberFormatException e) {
            System.out.println("异常信息为"+ e);
        }finally {
            System.out.println("finally执行");
        }
        System.out.println("继续");
    }
}
```

```java
package com.Kameda.try_;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class TryCatchDetail02 {
    public static void main(String[] args) {
        //1.如果 try 代码块有可能有多个异常
        //2.可以使用多个 catch 分别捕获不同的异常，相应处理
        // 3.要求子类异常写在前面，父类异常写在后面
        try {
            Person person = new Person();
            person = null;
            System.out.println(person.getName());//NullPointerException
            int n1 = 10;
            int n2 = 0;
            int res = n1 / n2;//ArithmeticException
        } catch (NullPointerException e){
            System.out.println(e.getMessage());
        } catch(ArithmeticException e) {
            System.out.println(e.getMessage());
        }finally {

        }

    }
}

class Person {
    private String name = "jack";

    public String getName() {
        return name;
    }
}
package com.Kameda.try_;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class TryCatchDetail03 {
    public static void main(String[] args) {
       /*
     可以进行 try-finally 配合使用, 这种用法相当于没有捕获异常，
      因此程序会直接崩掉/退出。应用场景，就是执行一段代码，
      不管是否发生异常，都必须执行某个业务逻辑
     */
        try{
            int n1=10;
            int n2 = 0;
            System.out.println(n1/n2);
        }finally {
            System.out.println("执行了 finally..");
        }
        System.out.println("程序继续执行..");
    }
}

```

try-finally

应用场景就是执行一段代码，不管是否发生异常都必须执行某个业务逻辑

经典应用场景

```java
package com.Kameda.try_;

import java.util.Scanner;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class TryCatchExercise04 {
    public static void main(String[] args) {
        /*
        用户输入的不是整数就反复提醒他输入

         */
        Scanner scanner = new Scanner(System.in);
        int num=0;
        while (true){
            try {
                System.out.println("请输入整数");
                num=Integer.parseInt(scanner.next());
                break;
            } catch (NumberFormatException e) {
                System.out.println("输入的不是一个整数");
            }
        }
        System.out.println("输入值为"+ num);

    }
}
```

细节

```java
package com.Kameda.throws_;

import java.io.FileInputStream;
import java.io.FileNotFoundException;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class ThrowsDetail {
    public static void main(String[] args) {

    }

    public void f2() {
        //1.对于编译异常，程序必须处理，如try-catch或者throws
        //2。对于运行时异常，程序中如果没有处理，默认就是throws的方式处理
        int n1 = 10;
        int n2 = 0;
        double res = n1 / n2;
    }
    public static void f1() {
        try {
            f3();
        } catch (FileNotFoundException e) {
            throw new RuntimeException(e);
        }
    }
    public static void f3() throws FileNotFoundException {
        FileInputStream fis = new FileInputStream("d://aa.txt");
    }
    public static void f4(){
        //f5()抛出的是运行异常
        //java中对此有默认处理机制
    }
    public static void f5()throws ArithmeticException{

    }
}

class Father { //父类
    public void method() throws RuntimeException {
    }
}

class Son extends Father {//子类

    //3. 子类重写父类的方法时，对抛出异常的规定:子类重写的方法，
// 所抛出的异常类型要么和父类抛出的异常一致，要么为父类抛出的异常类型的子类型
// 4. 在 throws 过程中，如果有方法 try-catch , 就相当于处理异常，就可以不必 throws
    @Override
    public void method() throws ArithmeticException {
    }
}
```

## 自定义异常

当程序中出现了某些错误，但该错误信息并没有在Throwable子类中描述处理，这个时候可以自己设计异常类，用于描述该错误信息。

步骤

1）定义类：自定义异常类名 extends RuntimeException

2）继承Exception，属于编译异常

3）继承runtimeException属于运行异常

```java
package com.Kameda.customexception;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class CustomException {
    public static void main(String[] args) {
        int age = 80;
        if(!(age>=18&&age<=120)){
            throw new AgeException("年龄在18到120之间");
        }
        System.out.println("你的年龄范围正常");

    }
}
//自定义异常
class AgeException extends RuntimeException{
    public AgeException(String message) {//构造器
        super(message);
    }
}
```

throw和throws区别

<img src="assets/%E6%88%AA%E5%B1%8F2022-11-08%2020.30.49.png" alt="截屏2022-11-08 20.30.49" style="zoom:50%;" />

练习

```java
package com.Kameda.HomeWork;

import com.Kameda.Exception_.ArrayIndexOutofBoundsException_;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class Homework01 {
    public static void main(String[] args) {
        /*
        编写应用程序EcmDef.java，接收命令行的两个参数，计算两数相除
        计算两个数相除，要求使用方法cal(int n1,int n2)
        对数据格式不正确，缺少命令行参数，除零进行异常处理
         */


        try {
            if (args.length!=2){
                throw new ArrayIndexOutOfBoundsException("参数个数不对");
            }
            int n1=Integer.parseInt(args[0]);
            int n2=Integer.parseInt(args[1]);

            double res = cal(n1,n2);
            System.out.println(res);
        } catch (ArrayIndexOutOfBoundsException e) {
            System.out.println(e.getMessage());
        }catch (NumberFormatException e){
            System.out.println("参数格式不正确");
        }catch (ArithmeticException e){
            System.out.println("出现了分母为零对异常");
        }

    }
    public static double cal(int n1,int n2){
        return n1/n2;
    }
}
/*
就是看catch会不会让try结束，不结束就依次执行,结束就先执行finally
 */
```

#包装类

\1) 针对八种基本数据类型相应的引用类型—包装类 2) 有了类的特点，就可以调用类中的方法。

<img src="assets/%E6%88%AA%E5%B1%8F2022-11-10%2014.44.35.png" alt="截屏2022-11-10 14.44.35" style="zoom:67%;" />

<img src="assets/%E6%88%AA%E5%B1%8F2022-11-10%2014.45.43.png" alt="截屏2022-11-10 14.45.43" style="zoom:67%;" />

![截屏2022-11-10 14.46.02](assets/%E6%88%AA%E5%B1%8F2022-11-10%2014.46.02.png)

包装类和基本数据类型的转换

```java
package com.Kameda.wrapper;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class Integer01 {
    public static void main(String[] args) {
        int n1 =100;
        Integer integer = new Integer(n1);
        Integer integer1 = Integer.valueOf(n1);

        int i = integer.intValue();

        //jdk5后
        int n2= 200;
        Integer integer2=n2;//底层原理调用valueOf方法
        int n3 = integer2;
    }
}
```

练习

```java
package com.Kameda.wrapper;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class WrapperExercise01 {
    public static void main(String[] args) {
        Double d = 100d;
        Float f= 1.5f;

        Object obj1= true? new Integer(1):new Double(2.0);
        System.out.println(obj1);//三元运算符是一个整体

        Object obj2;
        if (true)
            obj2 = new Integer(1);
        else
            obj2 = new Double(2.0);
        System.out.println(obj2);
    }
}
```

包装类型和 String 类型的相互转换

```java
package com.Kameda.wrapper;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class WrapperVSString {
    public static void main(String[] args) {
        //包装类(Integer)->String
        Integer i = 100;//自动装箱
        //方式1
        String str1 = i + "";
        //方式2
        String str2 = i.toString();
        //方式 3
        String str3 = String.valueOf(i);
        //String -> 包装类(Integer)
        String str4 = "12345";
        Integer i2 = Integer.parseInt(str4);//使用到自动装箱
        Integer i3 = new Integer(str4);//其中构造器可以
        System.out.println("ok~~");
    }
}
```

Integer 类和 Character 类的常用方法

```java
package com.Kameda.wrapper;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class WrapperMethod {
    public static void main(String[] args) {
        System.out.println(Integer.MIN_VALUE); //返回最小值
        System.out.println(Integer.MAX_VALUE);//返回最大值
        System.out.println(Character.isDigit('a'));//判断是不是数字
        System.out.println(Character.isLetter('a'));//判断是不是字母
        System.out.println(Character.isUpperCase('a'));//判断是不是大写
        System.out.println(Character.isLowerCase('a'));//判断是不是小写
        System.out.println(Character.isWhitespace('a'));//判断是不是空格
        System.out.println(Character.toUpperCase('a'));//转成大写
        System.out.println(Character.toLowerCase('A'));//转成小写
    }
}
```

Integer 类面试题

```java
package com.Kameda.wrapper;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class WrapperExercise02 {
    public static void main(String[] args) {
        Integer i = new Integer(1);
        Integer j = new Integer(1);
        System.out.println(i == j); //False //所以，这里主要是看范围 -128 ~ 127 就是直接返回
        /*
              如果 i 在 IntegerCache.low(-128)~IntegerCache.high(127),就直接从数组返回 //2. 如果不在 -128~127,就直接 new Integer(i)
              public static Integer valueOf(int i) {
              if (i >= IntegerCache.low && i <= IntegerCache.high)
                return IntegerCache.cache[i + (-IntegerCache.low)]; return new Integer(i);
        } */
        Integer m = 1; //底层 Integer.valueOf(1); -> 阅读源码
        Integer n = 1;//底层 Integer.valueOf(1);
        System.out.println(m == n); //T //所以，这里主要是看范围 -128 ~ 127 就是直接返回 //，否则，就 new Integer(xx);
        Integer x = 128;//底层 Integer.valueOf(1);
        Integer y = 128;//底层 Integer.valueOf(1);
        System.out.println(x == y);//False

    }
}
```

```java
package com.Kameda.wrapper;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class WrapperExercise03 {
    public static void main(String[] args) {
        //示例一
        Integer i1 = new Integer(127);
        Integer i2 = new Integer(127);
        System.out.println(i1 == i2);//F
//示例二
        Integer i3 = new Integer(128);
        Integer i4 = new Integer(128);
        System.out.println(i3 == i4);//F
//示例三
        Integer i5 = 127;//底层Integer.valueOf(127);
        Integer i6 = 127;//-128~127
        System.out.println(i5 == i6); //T
//示例四
        Integer i7 = 128;
        Integer i8 = 128;
        System.out.println(i7 == i8);//F
        // 示例五
        Integer i9 = 127; //Integer.valueOf(127)
        Integer i10 = new Integer(127);
        System.out.println(i9 == i10);//F
//示例六
        Integer i11 = 127;
        int i12 = 127;
//只有有基本数据类型，==判断的是值是否相同
        System.out.println(i11 == i12); //T
        // 示例七
        Integer i13 = 128;
        int i14 = 128;
        System.out.println(i13 == i14);//T
    }
}
```

## String类

String对象用于保存字符串，也就是一组字符序列

字符串常量对象使用双引号阔气的字符序列

字符串使用unicode编码，一个字符占两个字节

String类常用的构造器

```java
package com.Kameda.string_;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class String01 {
    public static void main(String[] args) {
        //String对象用于保存字符串，也就是一组字符序列
        //字符串常量对象使用双引号阔气的字符序列
        //字符串使用unicode编码，一个字符占两个字节
        //String类有很多构造器，构造器的重载
        // 常用的有 String s1 = new String();
        //String s2 = new String(String original);
        //String s3 = new String(char[] a);
        //String s4 = new String(char[] a,int startIndex,int count)
        //String s5 = new String(byte[] b)
        //5. String 类实现了接口 Serializable【String 可以串行化:可以在网络传输】
        //                 接口 Comparable [String 对象可以比较大小】
        // 6. String 是 final 类，不能被其他的类继承
        //7. String 有属性 private final char value[]; 用于存放字符串内容
        //8. 一定要注意:value 是一个 final 类型，不可以修改:即 value 不能指向
       // 新的地址，但是单个字符内容是可以变化
        String name = "jack";
        name ="tom";
        final char value[] = {'a','b','c'};
        char[] v2 = {'t','H'};
        value[0] = 'H';
        //value = v2;

    }
}
```

创建String对象的两种方式

方式1:直接赋值String s ="KAMEDA";

方式2:调用构造器String 是= new String（“KAMEDA”）;

方式1：先从常量池查看是否有“KAMEDA”空间，如果有直接指向，没有创建后指向。s最终指向常量池的空间地址

方式2:先在对中创建空间，里面维护了value属性，指向常量池中的KAMEDA空间，如果没有重新创建，如果有直接通过value指向。最终指向的是堆中空间地址。

<img src="assets/%E6%88%AA%E5%B1%8F2022-11-10%2018.37.28.png" alt="截屏2022-11-10 18.37.28" style="zoom: 50%;" />

字符串的特性

1）String是一个final类，代表不可变的字符序列

2）字符串是不可变的。一个字符串对象一旦被分配，其内容是不可改变的

**重要规则**：常量相加；看到是池。变量相加，是在堆中。看源码学习

<img src="assets/%E6%88%AA%E5%B1%8F2022-11-10%2021.00.09.png" alt="截屏2022-11-10 21.00.09" style="zoom:100%;" />

String常见方法

```java
package com.Kameda.string_;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class StringMethod {
    public static void main(String[] args) {
        //1. equals 前面已经讲过了. 比较内容是否相同，区分大小写
        String str1 = "hello";
        String str2 = "Hello";
        System.out.println(str1.equals(str2));//
       // 2.equalsIgnoreCase 忽略大小写的判断内容是否相等
        String username = "johN";
        if ("john".equalsIgnoreCase(username)) {
            System.out.println("Success!");
        } else {
            System.out.println("Failure!");
        }
        // 3.length 获取字符的个数，字符串的长度
        System.out.println("KAMEDA".length());
        // 4.indexOf 获取字符在字符串对象中第一次出现的索引，索引从 0 开始，如果找不到，返回-1
        String s1 = "wer@terwe@g";
        int index = s1.indexOf('@');
        System.out.println(index);// 3
        System.out.println("weIndex=" + s1.indexOf("we"));//0
        // 5.lastIndexOf 获取字符在字符串中最后一次出现的索引，索引从 0 开始，如果找不到，返回-1
        s1 = "wer@terwe@g@";
        index = s1.lastIndexOf('@');
        System.out.println(index);//11
        System.out.println("ter 的位置=" + s1.lastIndexOf("ter"));//4
       // 6.substring 截取指定范围的子串
        String name = "hello,みんさん";
       //下面 name.substring(6) 从索引 6 开始截取后面所有的内容
        System.out.println(name.substring(6));//截取后面的字符
        //name.substring(0,5)表示从索引 0 开始截取，截取到索引 5-1=4 位置
        System.out.println(name.substring(2, 5));//llo
    }
}
```

```java
package com.Kameda.string_;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class StringMethod02 {
    public static void main(String[] args) {
        // 1.toUpperCase 转换成大写
        String s = "heLLo";
        System.out.println(s.toUpperCase());//HELLO
        // 2.toLowerCase
        System.out.println(s.toLowerCase());//hello
        // 3.concat 拼接字符串
        String s1 = "宝玉";
        s1 = s1.concat("林黛玉").concat("薛宝钗").concat("together");
        System.out.println(s1);//宝玉林黛玉薛宝钗 together
        // 4.replace 替换字符串中的字符
        s1 = "宝玉 and 林黛玉 林黛玉 林黛玉";
        //在 s1 中，将 所有的 林黛玉 替换成薛宝钗
        //  s1.replace() 方法执行后，返回的结果才是替换过的.
        // 注意对 s1 没有任何影响
        String s11 = s1.replace("宝玉", "jack");
        System.out.println(s1);//宝玉 and 林黛玉 林黛玉 林黛玉
        System.out.println(s11);//jack and 林黛玉 林黛玉 林黛玉
        // 5.split 分割字符串, 对于某些分割字符，我们需要 转义比如 | \\等
        String poem = "锄禾日当午,汗滴禾下土,谁知盘中餐,粒粒皆辛苦";
        // 1. 以 , 为标准对 poem 进行分割 , 返回一个数组
        // 2. 在对字符串进行分割时，如果有特殊字符，需要加入 转义符 \
        String[] split = poem.split(",");
        poem = "E:\\aaa\\bbb";
        split = poem.split("\\\\");
        System.out.println("==分割后内容===");
        for (int i = 0; i < split.length; i++) {
            System.out.println(split[i]);
        }
        // 6.toCharArray 转换成字符数组
        s = "happy";
        char[] chs = s.toCharArray();
        for (int i = 0; i < chs.length; i++) {
            System.out.println(chs[i]);
        }
        /*7. compareTo 比较两个字符串的大小，如果前者大，则返回正数，后者大，则返回负数，如果相等，返回 0
        (1) 如果长度相同，并且每个字符也相同，就返回 0
        (2) 如果长度相同或者不相同，但是在进行比较时，可以区分大小
        就返回 if (c1 != c2) {
            return c1 - c2;
        }
        (3) 如果前面的部分都相同，就返回 str1.len - str2.len
        */
        String a = "jac";// len = 3
        String b = "jack";// len = 4
        System.out.println(a.compareTo(b)); // 返回值是 'c' - 'a' = 2 的值
        // 8.format 格式字符串
        /* 占位符有:
         * %s 字符串 %c 字符 %d 整型 %.2f 浮点型 *
         */
        String name = "john";
        int age = 10;
        double score = 56.857090909;
        char gender = '男';
        //将所有的信息都拼接在一个字符串.
        String info = "我的姓名是" + name + "年龄是" + age + ",成绩是" + score + "性别是" + gender+"希望大家能喜欢我";
        System.out.println(info);

        //1. %s , %d , %.2f %c 称为占位符
        //2. 这些占位符由后面变量来替换
        //3. %s 表示后面由 字符串来替换
        //4. %d 是整数来替换
        //5. %.2f 表示使用小数来替换，替换后，只会保留小数点两位, 并且进行四舍五入的处理
        // 6. %c 使用 char 类型来替换
        String formatStr = "我的姓名是%s 年龄是%d，成绩是%.2f 性别是%c.希望大家喜欢我!";
        String info2 = String.format(formatStr, name, age, score, gender);
        System.out.println("info2=" + info2);


    }
}
```

###StringBuffer类

代表可变的字符串序列，可以对字符串内容进行增删

很多方法与String相同，但StringBuffer是可变长度

StringBuffer是一个容器

```java
package com.Kameda.stringbuffer_;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class StringBuffer01 {
    public static void main(String[] args) {
//1. StringBuffer 的直接父类 是 AbstractStringBuilder
//2. StringBuffer 实现了 Serializable, 即 StringBuffer 的对象可以串行化
//3. 在父类中 AbstractStringBuilder 有属性 char[] value,不是 final
// 该 value 数组存放 字符串内容，引出存放在堆中的
//4. StringBuffer 是一个 final 类，不能被继承
//5. 因为 StringBuffer 字符内容是存在 char[] value, 所有在变化(增加/删除)
// 不用每次都更换地址(即不是每次创建新对象)， 所以效率高于 String//private final char value[]
        StringBuffer stringBuffer = new StringBuffer();
    }
}
```

String和StringBuffer的相互转换

```java
package com.Kameda.stringbuffer_;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class StringAndStringBuffer {
    public static void main(String[] args) {
        String str = "hello tom";
       //方式 1 使用构造器
       //注意: 返回的才是 StringBuffer 对象，对 str 本身没有影响
        StringBuffer stringBuffer = new StringBuffer(str);
       //方式 2 使用的是 append 方法
        StringBuffer stringBuffer1 = new StringBuffer();
        stringBuffer1 = stringBuffer1.append(str);

        //看看 StringBuffer ->String
        StringBuffer stringBuffer3 = new StringBuffer("KAMEDA LAB");
        //方式 1 使用 StringBuffer 提供的 toString 方法
        String s = stringBuffer3.toString();
        //方式 2: 使用构造器来搞定
        String s1 = new String(stringBuffer3);
    }
}
```

StringBuffer的常见方法

```java
package com.Kameda.stringbuffer_;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class StringBufferMethod {
    public static void main(String[] args) {
        StringBuffer s = new StringBuffer("hello");
       //增
        s.append(',');// "hello,"
        s.append("张三丰");//"hello,张三丰"
        s.append("赵敏").append(100).append(true).append(10.5);//"hello,张三丰赵敏 100true10.5"
        System.out.println(s);//"hello,张三丰赵敏 100true10.5"
        //删
        /*
        *删除索引为 >= start && <end 处的字符
        * 解读:删除 11 ~14 的字符[11, 14)
        */
        s.delete(11, 14);
        System.out.println(s);//"hello,张三丰赵敏 true10.5"
         //改
        //使用 周芷若 替换 索引 9-11 的字符 [9,11)
        s.replace(9, 11, "周芷若");
        System.out.println(s);//"hello,张三丰周芷若 true10.5"
        // 查找指定的子串在字符串第一次出现的索引，如果找不到返回-1
        int indexOf = s.indexOf("张三丰");
        System.out.println(indexOf);//6
        //插
        //在索引为 9 的位置插入 "赵敏",原来索引为 9 的内容自动后移
        s.insert(9, "赵敏");
        System.out.println(s);//"hello,张三丰赵敏周芷若 true10.5"
        //长度
        System.out.println(s.length());//22 System.out.println(s);
    }
}
```

练习

```java
package com.Kameda.stringbuffer_;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class StringBufferExercise02 {
    public static void main(String[] args) {
        /*
         输入商品名称和商品价格，要求打印效果示例, 使用前面学习的方法完成: 商品名 商品价格
         手机 123,564.59 //比如 价格 3,456,789.88 要求:价格的小数点前面每三位用逗号隔开, 在输出。
          思路分析
         1. 定义一个 Scanner 对象，接收用户输入的 价格(String)
         2. 希望使用到 StringBuffer 的 insert ，
         需要将 String 转成 StringBuffer 3. 然后使用相关方法进行字符串的处理
         */
        String price = "12345345343454.59";
        StringBuffer sb = new StringBuffer(price);
//        int i = sb.lastIndexOf(".");

        for (int j = sb.lastIndexOf(".")-3; j >0 ; j-=3) {

            sb= sb.insert(j, ",");
        }
        System.out.println(sb);

    }
}
```

###StringBuilder类

是一个可变字符序列。此类提供一个与StringBuffer兼容的API，但不保证同步。此类被设计用作StringBuffer的一个简易替换，用在字符串缓冲区被单个线程使用时，建议优先使用。

```java
package com.Kameda.stringbuilder_;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class StringBuilder01 {
    public static void main(String[] args) {
        //1. StringBuilder 继承 AbstractStringBuilder 类
        //2. 实现了 Serializable ,说明 StringBuilder 对象是可以串行化(对象可以网络传输,可以保存到文件)
        //3. StringBuilder 是 final 类, 不能被继承
        //4. StringBuilder 对象字符序列仍然是存放在其父类 AbstractStringBuilder 的 char[] value;
        // 因此，字符序列是堆中
        //5. StringBuilder 的方法，没有做互斥的处理,即没有 synchronized 关键字,因此在单线程的情况下使用
        //  StringBuilder
        StringBuilder stringBuilder = new StringBuilder();
    }
}
```

<img src="assets/%E6%88%AA%E5%B1%8F2022-11-11%2017.02.20.png" alt="截屏2022-11-11 17.02.20" style="zoom:50%;" />

```java
package com.Kameda.stringbuilder_;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class StringVsStringBufferVsStringBuilder {
    public static void main(String[] args) {

        long startTime = 0L;
        long endTime = 0L;
        StringBuffer buffer = new StringBuffer("");
        startTime = System.currentTimeMillis();
        for (int i = 0; i < 80000; i++) {//StringBuffer 拼接 20000 次
            buffer.append(String.valueOf(i));
        }
        endTime = System.currentTimeMillis();
        System.out.println("StringBuffer 的执行时间:" + (endTime - startTime));

        StringBuilder builder = new StringBuilder("");
        startTime = System.currentTimeMillis();
        for (int i = 0; i < 80000; i++) {//StringBuilder 拼接 20000 次
            builder.append(String.valueOf(i));
        }
        endTime = System.currentTimeMillis();
        System.out.println("StringBuilder 的执行时间:" + (endTime - startTime));

        String text = "";
        startTime = System.currentTimeMillis();
        for (int i = 0; i < 80000; i++) {//String 拼接 20000
            text = text + i;
        }
        endTime = System.currentTimeMillis();
        System.out.println("String 的执行时间:" + (endTime - startTime));

    }
}
/*
1.如果字符串存在大量修改，一般使用StringBuffer或者StringBuilder
2。单线程使用StringBuilder，多线程使用StringBuffer
3。很少修改，被多个对象应用使用String，配置信息等
 */
```



## Math类

```java
package com.Kameda.math_;

/**
 * @Author: Bill.MIN
 * @Version: Kameda Lab
 */
public class MathMethod {
    public static void main(String[] args) {
        //1.abs 绝对值
        int abs = Math.abs(-9);
        System.out.println(abs);//9
        //2.pow 求幂
        double pow = Math.pow(2, 4);//2 的 4 次方 System.out.println(pow);//16
        //3.ceil 向上取整,返回>=该参数的最小整数(转成 double);
        double ceil = Math.ceil(3.9);
        System.out.println(ceil);//4.0
        //4.floor 向下取整，返回<=该参数的最大整数(转成 double)
        double floor = Math.floor(4.001);
        System.out.println(floor);//4.0
        //5.round 四舍五入 Math.floor(该参数+0.5)
        long round = Math.round(5.51);
        System.out.println(round);//6
        //6.sqrt 求开方
        double sqrt = Math.sqrt(729);
        System.out.println(sqrt);//3.0
        //7.random 求随机数
        // random 返回的是 0 <= x < 1 之间的一个随机小数
        // 思考:请写出获取 a-b 之间的一个随机整数,a,b 均为整数 ，比如 a = 2, b=7
        // 即返回一个数 x 2<=x<=7
        // Math.random() * (b-a) 返回的就是 0 <= 数 <= b-a
        //(1) (int)(a) <= x <= (int)(a + Math.random() * (b-a +1) )
        //(2) 使用具体的数介绍 a=2 b=7
        // (int)(a + Math.random() * (b-a +1) ) = (int)( 2 + Math.random()*6)
        // Math.random()*6 返回的是 0 <= x < 6 小数
        // 2 + Math.random()*6 返回的就是 2<= x < 8 小数
        // (int)(2 + Math.random()*6) = 2 <= x <= 7
        // (3) 公式就是 (int)(a + Math.random() * (b-a +1) )
        for (int i = 0; i < 100; i++) {
        }
        System.out.println((int) (2 + Math.random() * (7 - 2 + 1)));
        //max , min 返回最大值和最小值
        int min = Math.min(1, 9);
        int max = Math.max(45, 90);
        System.out.println("min=" + min);
        System.out.println("max=" + max);
    }
}
```

