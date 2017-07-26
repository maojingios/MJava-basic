
# 基础语法

## 基本语法：
1、Java是大小写敏感语言，如“Hello”和“hello”是不同的；

2、类名首字母大写，随后单词首字母大写；

3、方法名首字母小写；

4、源文件名必须与类名相同；

5、主方法入口，所有java程序由public static void main (String []args)方法开始。

## 标识符
1、Java所有组成部分都需要名字。类名、变量名以及方法名都被称作为标识符。标识符可以是大小写字母、美元符$或者下划线_开头，后面可以跟大小写字母、美元符、下划线或者数字，其中关键字不能作为标识符，横线—、数字不能作为标识符的开头。

## 修饰符
和其他语言一样，Java中也可使用修饰符来修饰类中的方法和属性：

1、访问控制修饰符：

default（在同一包内可见，不使用任何修饰符）、public（共有的，对所有类都可见）、private（私有的，在同一类可见）、protected（受保护的，在同一包内或所有子类中可见）

2、访问控制和继承：

父类中的public，子类也必须为public；

父类中声明为protected，子类中要么为protected，要么为public；

父类中声明为private，子类不能被继承。


2、非访问控制修饰符：final、abstract、strictfp。

static修饰符，用来创建类方法，类变量。静态方法不能使用类的非静态变量，静态方法从参数列表获取参数。

final修饰符，用来修饰类、方法、和类变量。final修饰的类不能被继承、修饰的方法在子类中不可被重新定义；修饰的变量为常量，不可被修改。被声明为final的对象不能指向其他对象，但final里面的数据可以被修改。

abstract修饰符，用来创建抽象类和抽象方法。抽象类不能用来实例化对象，声明抽象类的唯一目的就是将来对该类进行扩充。一个类不能同时被final和abstract修饰。一个来包含抽象方发，那么该类一定要声明为抽象类，

抽象方法是一种没有任何实现的方法，该方法的具体实现由子类提供。抽象方法声明以分号结尾。

synchronized关键字声明的方法同一时间只能被一个线程访问。

volatile修饰的成员变量在每次被线程访问时，都回到共享内存中去取最新的值，保证不同的线程获取同一变量的值是一样的。

## Java变量
1、局部变量：

在方法、构造方法、或者语句块中定义；局部变量没有默认值，必须经过初始化才能使用。

2、类变量（静态变量）：

定义在类中，方法体之外，但必须声明为static类型；实例变量在类创建的时候创建，在类销毁的时候销毁；实例变量是具备默认值的，数值类型是0，布尔类型是false，引用类型是null;其他类通过类名.

3、成员变量（非静态变量）。定义在类中，方法体之外。

## 静态变量与实例变量的区别

1、静态变量属于类，该类不产生对象，通过类访问静态变量；

2、实例变量属于对象，需产生该类对象，通过对象访问实例变量；

3、实例变量在创建对象时，才会分配内存空间；静态变量在加载类字节码时，就会分配内存空间。


## 数组
数组是存储在堆内存上的对象，可保存多个同类型的变量。

## 类定义

	public class Dog{
	
		String breed;
		int age;
		String color;
	
		void barking(){}
		
		void hungry(){}
		
		void sleeping(){}
	}

## 构造函数
构造函数必须与类同名，可定义多个构造函数。如没有显示声明构造函数，Java在编译器会默认提供一个构造函数。

## 基本数据类型

1、内置数据类型：

byte（1个字节、8位）、short（2个字节、16位）、int（4个字节、32位）、long（8个字节，64位）、float（单精度，32位）、double（64位，双精度）;boolean（true、false）、char（16位的Unicode字符）。

2、引用类型

引用类型指向对象，数组,对象都是引用类型。引用类型默认值是null。

3、常量

常量在程序运行过程中不会被修改。使用final修饰。

4、类型转换

同一类型数据、由低向高转。

## 循环结构

1、while：

	while (布尔表达式){
	   循环内容
	}
	
	注：只要布尔表达式为true，循环体就会一直执行下去。

2、do ...while:

	do{
	
	}while(布尔表达式)
	
	注：与while相比，do、、、while至少会被执行一次。

3、for循环

4、数组增强for循环
	
	public class Test {
	   public static void main(String args[]){
	      int [] numbers = {10, 20, 30, 40, 50};
	 
	      for(int x : numbers ){
	         System.out.print( x );
	         System.out.print(",");
	      }
	      System.out.print("\n");
	      String [] names ={"James", "Larry", "Tom", "Lacy"};
	      for( String name : names ) {
	         System.out.print( name );
	         System.out.print(",");
	      }
	   }
	}

5、break

跳出整个循环语句。

6、continue

跳转到下一次循环的迭代。在for中，跳转到更新语句；在while或者do、、、while中跳转到布尔表达式。


## Java Number & Math类

1、一般的在Java开发过程中使用byte、short、int、long、double来表示数据；但实际开发中需要使用对象。因此Java为每个内置数据类型提供了包装类。（Integer、Long、Byte）.

2、常用Math函数

	xxxValue()：将 Number 对象转换为xxx数据类型的值并返回。

	compareTo()：将number对象与参数比较。
	
	equals()：判断number对象是否与参数相等。
	
	valueOf()：返回一个 Number 对象指定的内置数据类型
	
	toString()：以字符串形式返回值。
	
	parseInt()：将字符串解析为int类型。
	
	abs()：返回参数的绝对值。
	
	ceil()：对整形变量向左取整，返回类型为double型。
	
	floor()：对整型变量向右取整。返回类型为double类型。
	
	rint()：返回与参数最接近的整数。返回类型为double。
	
	round()：返回一个最接近的int、long型值。
	
	min()：返回两个参数中的最小值。
	
	max()：返回两个参数中的最大值。
	
	exp()：返回自然数底数e的参数次方。
	
	log()：返回参数的自然数底数的对数值。
	
	pow()：返回第一个参数的第二个参数次方。
	
	sqrt()：求参数的算术平方根。
	
	sin()：求指定double类型参数的正弦值。
	
	cos()：求指定double类型参数的余弦值。
	
	tan()：求指定double类型参数的正切值。
	
	asin()：求指定double类型参数的反正弦值。
	
	acos()：求指定double类型参数的反余弦值。
	
	atan()：求指定double类型参数的反正切值。
	
	atan2()：将笛卡尔坐标转换为极坐标，并返回极坐标的角度值。
	
	toDegrees()：将参数转化为角度。
	
	toRadians()：将角度转换为弧度。
	
	random()：返回一个随机数。
	
	
## Character

1、char：

	char ch = 'a';
	
	char unichar = '\u039A';//Unicode字符表示形式。
	
	char[] charArray = {'a','b','c','d'};
	
	在实际开发中经常需要使用对象，Java为我们提供Character包装类，提供了一系列的方法来操作字符。

2、Character：

	Character ch = new Character('a');

3、装箱-拆箱

	Chatacter ch = 'a'; //装箱
	
	注：将一个char类型的值传给Chatacter 类，编译器会自动将char类型参数转换成Character类型，这种特征称为装箱，反过来称为拆箱。
	
	char c = test ('x');// 原始字符 'x' 用 test 方法装箱;返回拆箱的值到 'c'

4、常用方法

	isLetter()：是否是一个字母
	
	isDigit()：是否是一个数字字符
	
	isWhitespace()：是否是一个空格
	
	isUpperCase()：是否是大写字母
	
	isLowerCase()：是否是小写字母
	
	toUpperCase()：指定字母的大写形式

	toLowerCase()：指定字母的小写形式

	toString()：返回字符的字符串形式，字符串的长度仅为1
	

## String

1、String

	String str = @"mkin";
	
	注：系统为我们提供了11种方式来创建字符串，String一旦创建就不能修改，如果需要对字符串进行更多操作，请使用StringBuffer或者StringBuilder类。

2、String常用方法：

	char charAt(int index)：返回指定索引处的 char 值。
	
	int compareTo(Object o)：把这个字符串和另一个对象比较。
	
	int compareTo(String anotherString)：按字典顺序比较两个字符串。
	
	int compareToIgnoreCase(String str)：按字典顺序比较两个字符串，不考虑大小写。
	
	String concat(String str)：将指定字符串连接到此字符串的结尾。
	
	boolean contentEquals(StringBuffer sb)：当且仅当字符串与指定的StringButter有相同顺序的字符时候返回真。
	
	static String copyValueOf(char[] data)：返回指定数组中表示该字符序列的 String。
	
	static String copyValueOf(char[] data, int offset, int count)：返回指定数组中表示该字符序列的 String。
	
	boolean endsWith(String suffix)：测试此字符串是否以指定的后缀结束。
	
	boolean equals(Object anObject)：将此字符串与指定的对象比较。
	
	boolean equalsIgnoreCase(String anotherString)：将此 String 与另一个 String 比较，不考虑大小写。
	
	byte[] getBytes()： 使用平台的默认字符集将此 String 编码为 byte 序列，并将结果存储到一个新的 byte 数组中。
	
	byte[] getBytes(String charsetName)：使用指定的字符集将此 String 编码为 byte 序列，并将结果存储到一个新的 byte 数组中。
	
	void getChars(int srcBegin, int srcEnd, char[] dst, int dstBegin)：将字符从此字符串复制到目标字符数组。
	
	int hashCode()：返回此字符串的哈希码。
	
	int indexOf(int ch)：返回指定字符在此字符串中第一次出现处的索引。
	
	int indexOf(int ch, int fromIndex)：返回在此字符串中第一次出现指定字符处的索引，从指定的索引开始搜索。
	
	int indexOf(String str)： 返回指定子字符串在此字符串中第一次出现处的索引。
	
	int indexOf(String str, int fromIndex)：返回指定子字符串在此字符串中第一次出现处的索引，从指定的索引开始。
	
	String intern()： 返回字符串对象的规范化表示形式。
	
	int lastIndexOf(int ch)： 返回指定字符在此字符串中最后一次出现处的索引。
	
	int lastIndexOf(int ch, int fromIndex)：返回指定字符在此字符串中最后一次出现处的索引，从指定的索引处开始进行反向搜索。
	
	int lastIndexOf(String str)：返回指定子字符串在此字符串中最右边出现处的索引。
	
	int lastIndexOf(String str, int fromIndex)： 返回指定子字符串在此字符串中最后一次出现处的索引，从指定的索引开始反向搜索。
	
	int length()：返回此字符串的长度。
	
	boolean matches(String regex)：告知此字符串是否匹配给定的正则表达式。
	
	boolean regionMatches(boolean ignoreCase, int toffset, String other, int ooffset, int len)：测试两个字符串区域是否相等。
	
	boolean regionMatches(int toffset, String other, int ooffset, int len)：测试两个字符串区域是否相等。
	
	String replace(char oldChar, char newChar)：返回一个新的字符串，它是通过用 newChar 替换此字符串中出现的所有 oldChar 得到的。
	
	String replaceAll(String regex, String replacement：使用给定的 replacement 替换此字符串所有匹配给定的正则表达式的子字符串。
	
	String replaceFirst(String regex, String replacement)： 使用给定的 replacement 替换此字符串匹配给定的正则表达式的第一个子字符串。
	
	String[] split(String regex)：根据给定正则表达式的匹配拆分此字符串。
	
	String[] split(String regex, int limit)：根据匹配给定的正则表达式来拆分此字符串。
	
	boolean startsWith(String prefix)：测试此字符串是否以指定的前缀开始。
	
	boolean startsWith(String prefix, int toffset)：测试此字符串从指定索引开始的子字符串是否以指定前缀开始。
	
	CharSequence subSequence(int beginIndex, int endIndex)： 返回一个新的字符序列，它是此序列的一个子序列。
	
	String substring(int beginIndex)：返回一个新的字符串，它是此字符串的一个子字符串。
	
	String substring(int beginIndex, int endIndex)：返回一个新字符串，它是此字符串的一个子字符串。
	
	char[] toCharArray()：将此字符串转换为一个新的字符数组。
	
	String toLowerCase()：使用默认语言环境的规则将此 String 中的所有字符都转换为小写。
	
	String toLowerCase(Locale locale)：使用给定 Locale 的规则将此 String 中的所有字符都转换为小写。
	
	String toString()： 返回此对象本身（它已经是一个字符串！）。
	
	String toUpperCase()：使用默认语言环境的规则将此 String 中的所有字符都转换为大写。
	
	String toUpperCase(Locale locale)：使用给定 Locale 的规则将此 String 中的所有字符都转换为大写。
	
	String trim()：返回字符串的副本，忽略前导空白和尾部空白。
	
	static String valueOf(primitive data type x)：返回给定data type类型x参数的字符串表示形式。


## java StringBuffer & StringBuilder

1、区别

StringBuilder为线程不安全，访问速度优于StringBuffer；一般情况下建议使用StringBuilder，涉及线程安全时使用StringBuffer。

注：实际开发中，使用StringBuffer多。

## Java数组

1、java数组是用来存储固定大小的同类型元素。

2、声明：

首选：dataType[] arrayVar;

