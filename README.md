# GCC 入门使用教程
--GCC入门使用教程的练习以及笔记

// 没有看第一节和第二节

```bash
gcc -Wall <FileName> -o <OutFileName>
 
  -W  显示告警，
  -Wall 显示所有到告警
  -o 用于指定输出的文件名，省略则输出为a.out
```

如果在编译到时候遇到乱码，则使用如下指令来修改：
```bash
export LANG=C
```

当程序比较大到时候，需要把程序写到多个程序中，这时需要定义两个文件：

* `fileName.h` 用于定义函数声明；
* `fileName.c` 用于实现书写函数到实现

定义完成后，在使用这个函数到文件首部，使用`#include "fileName.h"`将函数声明引入进来。注意：函数实现到文件中也要引入进来

多个程序到编译，只需要将多个程序加入到编译列表即可。例如

```bash
gcc -Wall main.c hello.c -o newhello.o
```

注意:

1. 不需要将头文件加入编译文件列表中。
2. 使用双引号的`include`，则是从当前目录下查找
3. 如果使用尖括号到`include`，则是从系统头文件目录查找
  * 常见到系统头文件目录：`/usr/include` 或者 `/usr/local/include/`

