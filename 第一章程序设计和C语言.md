#### 例1.1 输出This is C program

```c
#include <stdio.h>
	int main(){
   		printf("This is a C program");
    	return 0;
}
```

#### 例1.2 求两个数之和

```c
#include <stdio.h>
int main(int argc, char const *argv[]) {
  	int Sum(int x, int y); // 函数声明
 	int a, b, c;
 	printf("请输入两个数\n");
 	scanf("%d,%d", &a, &b);
  	c = Sum(a, b);
 	printf("%d\n", c);
  	return 0;
}
int Sum(int x, int y) { // 函数定义
  	int sum = 0;
  	sum = x + y;
 	return sum;
}
```

#### 例1.3 两个数比大小

```c
#include <stdio.h>
int main() {
    int Max(int x, int y); // 函数声明
    int a, b, max;
    printf("请输入两个数:\n");
    scanf("%d,%d", &a, &b);
    max = Max(a, b); // 函数调用
    if (max == 0)
        printf("您输入的两个数相等\n");
    else
        printf("最大的数是: %d\n", max);
}
int Max(int x, int y) {
    int max;
    if (x == y) // 如果两个数相等就返回0
        max = 0;
    else if (x > y)
        max = x;
    else
        max = y;
    return max;
}
```



#### 1. 什么是程序?什么是程序设计?

1. 程序是一组计算机能够识别和执行的指令

2. 程序设计是给出解决特定问题的程序过程

   程序设计是指设计编制调试程序的方法和过程

#### 2. 为什么需要计算机语言?高级语言有哪些特点?

1. 因为计算机语言是人与计算机之间传递信息的媒介；计算机语言解决了人和计算机交流的语言问题

2. 

   高级语言的数据结构丰富	

   高级语言接近自然语言和数学语言,容易掌握

   高级语言独立于机器，通用性强

#### 3.正确理解以下名词及其含义

源程序	

​		用高级语言编写的的程序称为源程序

​		指未编译的按照一定的程序设计语言规范书写的文本文件，是一系列人类可读的计算机语言指令

可执行程序	

​		将所有编译后得到的目标模块连接起来，在与函数库相连接成为一个整体，生成一个可供计算机执行的目标程序，称为可执行程序

目标程序    

​		用编译器把高级语言所写的程序转换为机器指令的程序称为目标程序

​		源程序经过“编译程序”编译所得到的二进制代码称为目标程序

​		目标程序指源程序经编译可直接被计算机运行的机器码集合，在计算机文件上以. obj作扩展名

程序编辑	

​		上机输入或者编辑源程序

程序编译	

​		用户使用编译程序对其个人编制的源程序进行编译的过程

程序链接

​		将所有编译后得到的目标模块连接装配起来，在与函数库相连接成为一个整体的过程称之为程序连接

程序	

​		一组计算机能识别和执行的指令

程序文件

​		程序的文件称为程序文件，程序文件存储的是程序，包括源程序和可执行程序

函数    

​		将一段经常需要使用的代码封装起来，在需要使用时可以直接调用，来完成一定功能

主函数	

​		称main函数，是程序执行的起点

被调用函数	

​		由一个函数调用另一个函数，则称第二个函数为被调用函数

库函数

​		一般是指编译器提供的可在c源程序中调用的函数。可分为两类，一类是c语言标准规定的库函数，一类是编译器特定的库函数

程序调试    

​		是将编制的程序投入实际运行前，用手工或编译程序等方法进行测试，修正语法错误和逻辑错误的过程

程序测试

​		是指对一个完成了全部或部分功能、模块的计算机程序在正式使用前的检测，以确保该程序能按预定的方式正确地运行

#### 4. 写一个C程序输出Hello World

```c
#include <stdio.h>
	int main(){
        printf("Hello World!")
        return 0;
    }
```



#### 5. 写一个C程序输入以下图形

```html
*****
 *****
  *****
   *****
```



```c
#include <stdio.h>
int main(){
	int i, j;
		for (i = 0; i <4; i++){
			for (j = 0; j < i; j++){
				printf("  ");
			}
			printf("*****\n");
		}
	return 0;
}

```



#### 6. 写一个C程序,输入3个数,输出最大者

```c
#include <stdio.h>
int main()
{
	int Max(int x, int y, int z);
	int a, b, c, max;
	printf("请输入三个数:\n");
	scanf("%d%d%d", &a, &b, &c);
	max = Max(a, b, c);
	printf("最大的数是:%d\n", max);
	return 0;
}
int Max(int x, int y, int z)
{
	int max = x;
	if (max < y)
		max = y;
	if (max < z)
		max = z;
	return max;
}
```

