# 编程作业: 综合练习（1）

## @抄写题＃1: 约瑟夫问题

[来源: POJ](http://pkuic.openjudge.cn/ziyoulianxi/15/) (Coursera声明：在POJ上完成的习题将不会计入Coursera的最后成绩。)

**总时间限制: 1000ms 内存限制: 65536kB**

### 描述

约瑟夫问题：有ｎ只猴子，按顺时针方向围成一圈选大王（编号从１到ｎ），从第１号开始报数，一直数到ｍ，数到ｍ的猴子退出圈外，剩下的猴子再接着从1开始报数。就这样，直到圈内只剩下一只猴子时，这个猴子就是猴王，编程求输入ｎ，ｍ后，输出最后猴王的编号。

### 输入

每行是用空格分开的两个整数，第一个是 n, 第二个是 m ( 0 < m,n <=300)。最后一行是：

0 0

### 输出

对于每行输入数据（最后一行除外)，输出数据也是一行，即最后猴王的编号

### 样例输入

```
6 2
12 4
8 3
0 0
```

### 样例输出

```
5
1
7
```

### 解题思路

这里我采用了自己的解法，感觉用数组处理更方便简洁。

用 `id` 存储猴子编号，`state` 存储状态，1表示在圈内，0表示圈外

然后按照题目思路报数处理就行了，主要注意是**围成一圈**，所以对 `id` 循环时要做一定处理。



## 抄写题＃2：分数求和

[来源: POJ](http://pkuic.openjudge.cn/practice/1006/) (Coursera声明：在POJ上完成的习题将不会计入Coursera的最后成绩。)

**注意： 总时间限制: 1000ms 内存限制: 65536kB**

### 描述

输入n个分数并对他们求和，用约分之后的最简形式表示。

比如：

q/p = x1/y1 + x2/y2 +....+ xn/yn，

q/p要求是归约之后的形式。

如：5/6已经是最简形式，3/6需要规约为1/2, 3/1需要规约成3，10/3就是最简形式。

PS:分子和分母都没有为0的情况，也没有出现负数的情况

### 输入

第一行的输入n,代表一共有几个分数需要求和

接下来的n行是分数

### 输出

输出只有一行，即归约后的结果

### 样例输入

```
2
1/2
1/3
```

### 样例输出

```
5/6
```





## 编程题＃1：年龄与疾病

[来源: POJ](http://pkuic.openjudge.cn/hw03/1/) (Coursera声明：在POJ上完成的习题将不会计入Coursera的最后成绩。)

**注意： 总时间限制: 1000ms 内存限制: 65536kB**

### 描述

某医院想统计一下某项疾病的获得与否与年龄是否有关，需要对以前的诊断记录进行整理。

### 输入

共2行，第一行为过往病人的数目n（0 < n <= 100)，第二行为每个病人患病时的年龄。

### 输出

每个年龄段（分四段：18以下，19-35，36-60，大于60**注意看样例输出的格式**）的患病人数占总患病人数的比例，以百分比的形式输出，精确到小数点后两位（double）。关于c++的格式化的输入输出，请参考：http://www.cplusplus.com/reference/iomanip。也可以在网上搜索一下，资料很多的。

### 样例输入

```
10
1 11 21 31 41 51 61 71 81 91
```

### 样例输出

```
1-18: 20.00%
19-35: 20.00%
36-60: 20.00%
60-: 40.00%
```

### 提示

注意最后一行的输出是“60-: ”，而不是“61-: ”。

每个冒号之后有一个空格。

输出可以用 `cout<<fixed<<setprecision(2) << f;` 来保留f后面的两位小数。



## 编程题＃2：成绩判断

[来源: POJ ](http://pkuic.openjudge.cn/hw03/2/)(Coursera声明：在POJ上完成的习题将不会计入Coursera的最后成绩。)

**注意： 总时间限制: 1000ms 内存限制: 6000kB**

### 描述

输入一个0--100的分数，判断分数代表什么等级。

95<=分数<=100, 输出1

90<=分数<95,输出2

85<=分数<90,输出3

80<=分数<85,输出4

70<=分数<80,输出5

60<=分数<70输出6

分数 < 60;输出7.

### 输入

n

### 输出

m

### 样例输入

```
87
```

### 样例输出

```
3
```



## @编程题＃3：找出第k大的数

[来源: POJ](http://pkuic.openjudge.cn/hw03/3/) (Coursera声明：在POJ上完成的习题将不会计入Coursera的最后成绩。)

**注意： 总时间限制: 1000ms 内存限制: 65536kB**

### 描述

用户输入N和K，然后接着输入N个正整数（无序的），程序在不对N个整数排序的情况下，找出第K大的数。注意，第K大的数意味着从大到小排在第K位的数。

### 输入

N

K

a1 a2 a3 a4 ..... aN

### 输出

b

### 样例输入

```
5
2
32 3 12 5 89
```

### 样例输出

```
32
```

### 提示

这是一道很经典的算法问题，是公司面试的常见考题。以后学习递归之后再回头看看这道题，或许有新解法。

### 解题思路

我用了最简单，也是效率最低的方法，遍历每个数，求出比他大的个数，如果为k-1个，那么这个数就是第k大的数。

网上也有利用算法知识解决的，快速排序等等，因为还没学到这部分内容先跳过。

## 编程题＃4：人民币支付

[来源: POJ](http://pkuic.openjudge.cn/hw03/5/) (Coursera声明：在POJ上完成的习题将不会计入Coursera的最后成绩。)

**注意： 总时间限制: 1000ms 内存限制: 65536kB**

### 描述

从键盘输入一指定金额（以元为单位，如345），然后输出支付该金额的各种面额的人民币数量，显示100元，50元，20元，10元，5元，1元各多少张，要求**尽量使用大面额的钞票**。

### 输入

一个小于1000的正整数。

### 输出

输出分行，每行显示一个整数，从上到下分别表示100元，50元，20元，10元，5元，1元人民币的张数

### 样例输入

```
735
```

### 样例输出

```
7
0
1
1
1
0
```