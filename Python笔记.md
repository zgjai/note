##Python2.X


1. 中文编码
	在2.X版本中，若文件不指定编码，则默认使用ASCII格式；但在3.X中则默认使用UTF-8编码。所以若要在代码中包含中文，则需在文件开头加入：
		
		# -*- coding: UTF-8 -*-

2. python代码块
	python代码块不适用{}来控制类、函数等，而是使用模块缩进。
	文件格式不对时报错：IndentationError
	
3. 标准数据类型
	* Numbers （数字）
		* int （有符号整型）
		* long （长整型） 
		* float （浮点型）
		* complex （复数）
		
	* String （字符串）
	* List （列表）
	* Tuple （元组）
	* Dictionary （字典）

 
4. 算数运算符  

	|  运算符 | 描述 | 实例 |  
	| ---: | :---: | :--- |
	| + |  加  | |
	| - |  减  | |
	| * |  乘  | |
	| / |  除  | |
	| % |  取模 | |
	| ** |  幂 | 10**20表示10的20次方 |
	| // |  取整数 | 9.0//2.0输出结果为4.0 | 

5. 条件判断语句
	格式：
	if 判断条件:
		执行语句.....
	else:
		执行语句.....
	
	多判断条件的格式:
	if 判断条件1:
		执行语句1.....
	elif 判断条件2:
		执行语句2.....
	elif 判断条件3:
		执行语句3.....
	else:
		执行语句4.....
		
	示例:  
		
		flag = False
		name = 'luren'
		if name == 'python':
			flag = True
			print 'welcome boss'
		else:
			print name
			

6. while循环语句
	格式：
	while 判断条件:
			执行语句.....
	else:
			执行语句.....
			
	示例: 
	
		#!/usr/bin/python
		# -*- coding: UTF-8 -*-
		
		count=0
		while count<5:
			print count, " is less than 5"
			count = count + 1
		else:
			print count, " is not less than 5"
			

7. for循环语句
	格式1:
	for iterating_var in sequence:
		执行语句.....
		
	示例:
	
		#!/usr/bin/python
		# -*- coding: UTF-8 -*-
		
		for letter in 'Python':
			print '当前字母: ', letter 
			
	格式2:
	for index in sequence.length:
		执行语句.....
		
	示例:
	
		#!/usr/bin/python
		# -*- coding: UTF-8 -*-
		
		fruits = ['banana', 'apple', 'mango']
		for index in range(len(fruits)):
			print '当前水果: ', fruits[index]
			
8. pass语句  
	pass语句是空语句，是为了保持程序结构的完整性，一般用作占位语句。  
	

9. 数字类型转换  
	* int(x [,base ])  
		将x转换为一个整数  
	* long(x [,base ])  
		将x转换为一个长整数  
	* float(x )  
		将x转换为一个浮点数  
	* complex(real [,imag ])  
		创建一个复数  
	* str(x )  
		将对象x转换为字符串  
	* repr(x )  
		将对象x转换为表达式字符串  
	* eval(str )  
		用来计算在字符串中的有效Python表达式，并返回一个对象  
	* tuple(s )  
		将序列s转换为一个元组  
	* list(s )  
		将序列s转换为一个列表  
	* chr(x )  
		将一个整数转换为一个字符  
	* unichr(x )  
		将一个整数转换为Unicode字符  
	* ord(x )  
		将一个字符转换为它的整数值  
	* hex(x )  
		将一个整数转换为一个十六进制字符串  
	* oct(x )  
		将一个整数转换为一个八进制字符串  
		
10. 数学函数
	* abs(x)  
		返回数字的绝对值
	* ceil(x)  
		返回数字的上入整数，如math.ceil(4.1)返回5  
	* cmp(x,y)  
		若x\<y返回-1，若x==y返回0，若x>y返回1  
	* exp(x)  
		返回e的x次幂(e<sup>x</sup>)，如math.exp(1)返回值为2.718281828459045  
	* fabs(x)  
		返回数字的绝对值的浮点值，math.fabs(-10)返回10.0  
	* floor(x)  
		返回数字的下舍整数  
	* log(x)  
		如math.log(math.e)返回1.0，math.log(100,10)返回2.0  
	* log10(x)  
		返回以10为基数的x的对数，如math.log10(100)返回2.0  
	* max(x1,x2...)   
		返回给定参数的最大值，参数可以为序列  
	* min(x1,x2...)  
		返回给定参数的最小值，参数可以为序列  
	* modf(x)  
		返回x的整数部分与小数部分，两个部分的数值符号与x相同，整数部分以浮点型表示  
	* pow(x,y)  
		x<sup>y</sup> 运算后的值  
	* round(x [,n])  
		返回浮点数x的四舍五入值，如给出n值，则代表舍入到小数点后的位数    
	* sqrt(x)  
		返回数字x的平方根
		
11. 随机数函数
	* choice(seq)  
		从序列的元素中随机挑选一个元素，比如random.choice(range(10))，从0到9中随机挑选一个整数  
	* randrange([start,] stop [,step])  
		从指定范围内，按指定基数递增的集合中获取一个随机数，基数缺省值为1  
	* random()  
		随机生成下一个实数，它在[0,1)范围内  
	* seed([x])  
		改变随机数生成器的种子seed  
	* shuffle(lst)  
		将序列的所有元素随机排序  
	* uniform(x,y)  
		随机生成下一个实数，它在[x,y]范围内

12. 字符串
	Python不支持单字符类型，单字符也是作为一个字符串使用。Python访问字符串，可以使用方括号来截取字符串。  
	示例：
	
		#!/usr/bin/python
		# -*- coding: utf-8 -*-
		
		var1 = 'Hello World!'
		var2 = "Python Runoob"
		
		print "var1[0]: ", var1[0]
		print "var2[1:5]: ", var2[1:5]
		
	示例执行结果为：  
	
		var1[0]: H
		var2[1:5]: ytho
		
	
13. 字符串运算符  
	假设a="Hello", b="Python"
	
	| 操作符 | 描述 | 结果 |
	|---|:-----|:-----|
	| + | 字符串 | HelloPython |
	| * | 重复输出字符串 | a*2结果为HelloHello |
	| [] | 通过索引获取字符串中字符 | a[1]结果为e |
	| [:] | 截取字符串中的一部分 | a[1:4]结果为ell |
	| in | 成员运算符-如果字符串中包含给定的字符返回True | H in a结果为1 |
	| not in | 成员运算符-如果字符串中不包含给定的字符返回True | M not in a 结果1 |
	| r/R | 原始字符串 - 原始字符串：所有的字符串都是直接按照字面的意思来使用，没有转义特殊或不能打印的字符。 原始字符串除在字符串的第一个引号前加上字母"r"（可以大小写）以外，与普通字符串有着几乎完全相同的语法。 | print r'\n' 输出 \n 和 print R'\n' 输出 \n |
	| % | 格式字符串 | 类似于c中的sprintf |  
	
14. 三引号  
	Python三引号允许一个字符串跨多行，字符串中可以包含换行符、制表符以及其它特殊字符，自始至终保持一小块字符串的格式是所谓的WYSIWYG（所见即所得）格式的。
	
	
15. Python列表(List)  
	列表是最常用的Python数据类型，它可以作为一个方括号内的逗号分隔值出现。列表的数据项不需要具有相同的类型。与字符串的索引一样，列表索引从0开始，列表可以进行截取、组合等。
	示例：
	
		list1 = ['physics', 'chemistry', 1997, 2000];
		list2 = [1, 2, 3, 4, 5];
		list3 = ["a", "b", "c", "d"];
		
	* 删除列表元素  
		del list1[2]：表示删除list1的第3个元素  
	* 列表脚本操作符  
		示例：  
		
		| Python表达式 | 结果 | 描述 |
		|:-----|:-----|:-----|
		| len([1,2,3]) | 3 | 长度 |
		| [1,2,3] + [4,5,6] | [1,2,3,4,5,6] | 组合 |
		| ['Hi!']*4 | ['Hi!','Hi!','Hi!','Hi!'] | 重复 |
		| 3 in [1,2,3] | True | 元素是否存在于列表中 |
		| for x in [1,2,3]: print x | 1 2 3 | 迭代 |   
	
	* 列表截取  
		示例：L = ['spam', 'Spam', 'SPAM!']
		
		| Python表达式 | 结果 | 描述 |
		|:-----|:-----|:-----|
		| L[2] | 'SPAM!' | 读取列表中第三个元素 |
		| L[-2] | 'Spam' | 读取列表中倒数第二个元素 |
		| L[1:] | ['Spam', 'SPAM!'] | 从第二个元素开始截取列表 |
		
16. Python元组(tup)  
		Python元组与列表类似，不同之处在于元组的元素不能修改。元组使用小括号，列表使用方括号。
		注意：元组中只包含一个元素时，需要在元素后面添加逗号，如：  tup = (50,);  
		
17. Python字典(Dictionary)
		字典是另一种可变容器模型，且可存储任意类型对象。  
		示例：  
		
		dict = { 'abc':123, 98.6:37 };
		#获取字典里的值  
		print dict['abc'], dict[98.6];
		#修改字典里的值
		dict['abc'] = 8;
		#删除字典元素
		del dict['abc'];
		#清空字典元素
		dict.clear();
		#删除字典
		del dict;		
		
18. Python日期和时间  
		Python提供了一个time和calendar模块可以用于格式化和时间。时间间隔是以秒为单位的浮点小数。
		示例：
		
		#!/usr/bin/python
		# -*- coding: UTF-8 -*-
		
		import time;  # 引入time模块
		
		ticks = time.time()
		print "当前时间戳为：", ticks
		
		
	时间元组：
		
	| 序号 | 对应属性名 | 字段 | 值 |
	|:-----|:-----|:-----|:-----|
	| 0 | tm_year | 4位数年 | 2008 |
	| 1 | tm_mon | 月 | 1到12 |
	| 2 | tm_mday | 日 | 1到31 |
	| 3 | tm_hour | 小时 | 0到23 |
	| 4 | tm_min | 分钟 | 0到59 |
	| 5 | tm_sec | 秒 | 0到61（60或61是闰秒）|
	| 6 | tm_wday | 一周的第几日 | 0到6（0是周一） |
	| 7 | tm_yday | 一年的第几日 | 1到366（儒略历） |
	| 8 | tm_isdst | 夏令时 | -1,0,1,-1是决定是否为夏令时的旗帜 |
		
	示例：
	
		#!/usr/bin/python
		# -*- coding: UTF-8 -*-
		
		import time
		
		localtime = time.localtime(time.time())
		print "本地时间为：", localtime
		
	输出结果为：
	
		本地时间为：time.struct_time(tm_year=2016, tm_mon=4, tm_mday=18, tm_hour=9, tm_min=9, tm_sec=51, tm_wday=0, tm_yday=109, tm_isdst=0)
		
				
		
19. Python函数  
		函数语法：
		
		def functionname( parameters ):
			"函数_文档字符串"
			function_suite
			return [expression]
	注意：Python是按引用传递参数的  
		参数类型：  
		
	*  必备参数  
		必备参数必须以正确的顺序传入函数，同C、Java 
	*  关键字参数  
		关键字参数和函数调用关系紧密，函数调用使用关键字参数来确定传入的参数值。使用关键字参数，允许函数调用时参数的顺序与声明时不一致，因为Python解释器能够用参数名匹配参数值。  
	*  默认参数  
		亦可以称为缺省参数，同C、Java
	*  不定长参数  
		可能需要一个函数能处理比当初声明时更多的参数，这些参数叫做不定长参数，和上述参数不同的是，声明时不会命名该参数。  
		基本语法：
		
			def functionname(\[formal_args, \] *var_args_tuple ):
			"函数_文档字符串"
			function_suite
			return [expression]
		示例：
		
			#!/usr/bin/python
			# -*- coding: UTF-8 -*-
			
			def printinfo( arg1, *vartuple):
				"打印任何传入的参数"
				print "输出："
				print arg1
				for var in vartuple:
					print var
				return;
				
			printinfo( 10 );
			printinfo( 70, 60, 50 );
			
		结果：
		
			输出：
			10
			输出：
			70
			60
			50
			
			
	#####匿名函数
	Python使用lambda来创建匿名函数。 
	 
	* lambda只是一个表达式，函数体比def简单很多
	* lambda的主体是一个表达式，而不是一个代码块。仅仅能在lambda表达式中封装有限的逻辑进去。
	* lambda函数拥有自己的命名空间，且不能访问自有参数列表之外或全局命名空间里的参数。
	* 虽然lambda函数看起来只能写一行，却不等同于C或C++的内联函数，后者的目的是调用小函数时不占用栈内存从而增加运行效率。
	示例：
	
			#!/usr/bin/python
			# -*- coding: UTF-8 -*-
			
			sum = lambda arg1, arg2: arg1 + arg2;
			print "相加后的值为：", sum( 10, 20 )
			print "相加后的值为：", sum( 20, 20 )
			
	结果：
	
			相加后的值为：30
			相加后的值为：40
			

20. Python模块  
		简单地说，模块就是一个保存了Python代码的文件。模块里能定义函数，类和变量。模块里也能包含可执行的代码。  
		想使用Python源文件，只需在另一个源文件里执行import语句，语法如下：
		
		import module1[, module2[,... moduleN]]
		
	Python的from语句可以从模块中导入一个指定的部分到当前命名空间中。示例，导入模块fib的fibonacci函数：
	
		from fib import fibonacci
		
	当你导入一个模块，Python解析器对模块位置的搜索顺序是：  
	* 当前目录
	* 在shell变量PYTHONPATH下的每个目录
	* 查看默认路径 
	
	#####命名空间和作用域    
	变量是拥有匹配对象的名字。命名空间是一个包含了变量名称们（键）和它们各自相应的对象们（值）的字典。
	
	* dir()函数  
		该函数返回一个排好序的字符串列表，内容是一个模块里定义过的名字。返回的列表容纳了在一个模块里定义的所有模块，变量和函数。
		示例：
		
			#!/usr/bin/python
			# -*- coding: UTF-8 -*-
			
			import math
			
			content = dir(math)
			
			print content;
			
		结果：
		
			['__doc__', '__file__', '__name__', 'acos', 'asin', 'atan', 
			'atan2', 'ceil', 'cos', 'cosh', 'degrees', 'e', 'exp', 
			'fabs', 'floor', 'fmod', 'frexp', 'hypot', 'ldexp', 'log',
			'log10', 'modf', 'pi', 'pow', 'radians', 'sin', 'sinh', 
			'sqrt', 'tan', 'tanh'] 
			
	* globals()函数和locals()函数  
		根据调用地方的不同，这两个函数分别被用作返回全局和局部命名空间里的名字。
		如果在函数内部调用locals()，返回的是所有能在该函数里访问的命名。
		如果在函数内部调用globals()，返回的是所有在该函数里能访问的全局名字。
		两个函数的返回类型都是字典，所以名字们能用keys()函数获取。
		
	* reload()函数  
		当一个模块被导入到一个脚本里，模块顶层部分的代码只会被执行一次，因此，如果你想重新执行模块里顶层部分的代码，可以用reload()函数，该函数会导入之前导入过的模块。
		

21. Python文件I/O  
	* 读取键盘输入
		* raw\_input函数  
			raw\_input([prompt])函数从标准输入读取一个行，并返回一个字符串（去掉结尾的换行符）：
			
				#!/usr/bin/python
				# -*- coding: UTF-8 -*-
				
				str = raw_input("请输入：");
				print "你输入的内容是：", str
			
		* input函数  
			input([prompt])函数和raw_input([prompt])函数基本类似，但是input可以接收一个Python表达式作为输入，并将运算结果返回。
			
	* 打开和关闭文件  
			Python提供了必要的函数和方法进行默认情况下的文件基本操作，可以使用file对象做大部分的文件操作。    
		* open函数  
			必须先用Python内置的open()函数打开一个文件，创建一个file对象，相关的方法才可以调用它进行读写。  
			语法：
			
				file object = open(file_name [, access_mode] [, buffering])
				
			各个参数的细节如下：  
			file_name：是一个包含了你要访问的文件名称的字符串值  
			access_mode：决定了打开文件的模式：只读，写入，追加等。默认是只读（r）  
			buffering：如果buffering的值被设为0，就不会寄存。如果buffering的值取1，访问文件时会寄存行。如果将buffering的值设为大于1的整数，表明了这就是寄存区的缓冲大小。如果取负值，寄存区的缓冲大小则为系统默认。
			  
		* File对象的属性    
			一个文件被打开后，根据这个file对象，可以得到有关该文件的各种信息。
			* file.closed  如果文件被关闭则返回true，否则返回false
			* file.mode  返回被打开文件的访问模式
			* file.name  返回文件的名称
			* file.softspace  如果用print输出后，必须跟一个空格符，则返回false，否则返回true。  
		* close()函数  
			File对象的close()方法刷新缓冲区里任何还没写入的信息，并关闭该文件，这之后便不能再进行写入。当一个文件对象的引用被重新指定给另一个文件时，Python会关闭之前的文件。
			语法：
			
				fileObject.close();
				
		* write()函数  
			write()函数可将任何字符串写入一个打开的文件。
			示例：
			
				#!/usr/bin/python
				# -*- coding: UTF-8 -*-
				
				fo = open("foo.txt", "wb")
				print "文件名： ", fo.name
				fo.write( "www.runoob.com!\n" );
				fo.close();
		
		* read()函数  
			read()函数从一个打开的文件中读取一个字符串
			语法：
			
				fileObject.read([count]);
				
			在这里，被传递的参数是要从已打开的文件中读取的字节数。该方法从文件的开头开始读入，如果没有传入count，它会尝试尽可能多地读取更多的内容，很可能是直到文件的末尾。
			
		* 文件定位  
			tell()方法告诉你文件内的当前位置。  
			seek( offset [, from] )方法改变当前文件的位置。Offset变量表示要移动的字节数。From变量指定开始移动字节的参考位置。  
			如果from被设为0，这意味着将文件的开头作为移动字节的参考位置。如果设为1，则使用当前的位置作为参考位置。如果被设为2，那么以该文件的末尾作为参考位置。  
			
		* 重命名和删除文件  
			Python的os模块提供了帮助执行文件处理操作的方法，比如重命名和删除文件。要使用这个模块，必须先导入它，然后才可以调用相关的各种功能。
			rename()方法：  
			语法：
			
				os.rename(current_file_name, new_file_name)
				
			remove()方法：  
			语法：  
			
				os.remove(file_name)
				
			