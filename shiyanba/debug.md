过程
1、通过IDA打开文件 debug，发现出现 “printing flag” 字段

![debug](https://github.com/kal-matthew/CTF-PRACTICE/blob/master/shiyanba/picture/debug.png)

2、在linux中通过gdb进行调试
a、在  __libc_start_main处设置断点，run
b、设置 eip值为上面截图中的命令第一行，也就是0x0804849b,continue,得到flag值

gdb调试过程如下：

知识点：IDA、gdb中的断点，eip值
