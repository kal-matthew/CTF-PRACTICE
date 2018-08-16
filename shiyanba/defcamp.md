1、通过IDA反汇编程序；
2、F5 main函数，得到如下程序：
![1](https://github.com/kal-matthew/CTF-PRACTICE/blob/master/shiyanba/picture/defcamp_1.png)

通过查看程序，链表中一共10个元素。元素中存储序号值+109。对于输入s，如果sub_40074D返回值为0，则正确。
3、查看sub_40074D函数

![2](https://github.com/kal-matthew/CTF-PRACTICE/blob/master/shiyanba/picture/defcamp_2.png)

第一个for循环5次

每次循环都将我们输入的password的对应字符与链表数据域中的数值进行比对，如果相等，就会把该数值对应的序号存放在v6数组中。

第二个for就是v6数组与v9数组进行比对。
v9数组 5 2 7 2 5 6

所以对应数值 114 111 116 111 114 115

对应的ASCII码为：rotors

提交答案为flag{}  (没有冒号，坑）
