1.switch的基本使用
![[switch的基本使用.png]]
2.执行流程：
	用变量接收的值和下面case后面的常量值匹配，匹配上哪个case就执行哪个case对应的执行语句，如果以上所有case都没有匹配上，就走default对应的执行语句n
3.break关键字：代表的是结束switch语句
4.注意：switch关键字能匹配什么类型的数据：
		byte  short int char 枚举类型 String类型
		==浮点型具有精度损失问题，所以不行==
5.case穿透性
	1.如果没有break，则会出现case的穿透性，程序就一直往下穿透执行，直到遇到了break或者switch代码执行完毕了，就停止了