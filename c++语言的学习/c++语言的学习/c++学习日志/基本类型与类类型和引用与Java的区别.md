基本类型：定义：c++内置的简单数据类型，如int、float、char、bool等
存储方法：直接存储在栈内存或静态存储区
		示例：
			int a= 10;//栈中直接存储值10
			double b=3.14;栈中直接存储值3.14
类类型：定义：通过class或struct定义的自定义类型如（std::string、vector等）
	存储方式：对象本身：可以存储在栈或堆内存中
			成员数据：可能包含基本类型或其他类类型的成员变量
			示例：#include<string>
				std::string s = "hello";栈中存储对象，对象内部
引用：
	c++中的引用（&）
		本质：是变量的别名，绑定到一个已存在的对象，不涉及内存地址的直接操作
		特点：必须初始化：引用一旦绑定到对象，不能修改指向
			无空引用：不能指向nullptr
			直接操作对象：对引用的操作等于对原对象的操作
	java中的引用
		本质：类似c++的指针但更安全，存储对象在堆中的地址
		特点：可重新赋值：引用可以指向不同的对象
			可为null：允许空引用
				自动内存管理：通过垃圾回收（GC）释放对象
c++对象存储方式：
	（1）栈内存（stack）：
				1.对象直接创建：自动管理生命周期，函数结束时释放
				std::string s="hello";//栈中对象
	（2）堆内存（Heap）：
				1.动态分配：通过new创建，需手动delete释放
				std::string* s=new std::string("hello object");
				delete s;
c++中的值传递，引用传递，指针传递
![[c++的三种传递.png]]
	//值传递
		void modifyByValue(int x){x =30;}
	//引用传递
		void modifyByReference(int& x){x = 30;}
	//指针传递
		void modifyByPointer(int* x){*x=20;}
	int main(){
	int a =10;
	modifyByValue(a);//a仍为10
	modifyByReference(a);//a变为30
	modifyByPointer(&a);//a变为30
	}