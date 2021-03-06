# question-design-pattern
some questions and answers for design pattern.

#### 1. 面向对象的四大基本特性？
封装：可以使类具有独立性和隔离性；保证类的高内聚。只暴露给外部和子类必须的属性和操作。类封装的实现依赖类的修饰符public、protected、private等。<br>
继承：对现有类的一种复用机制。一个类如果继承现有的类，则将拥有被继承类的所有非私有属性和操作。继承包括类的继承和接口的实现。<br>
多态：多态实在继承的基础上实现的。多态的三个要素：继承、重写、父类引用指向子类对象。父类引用指向不同的子类对象时，调用相同的方法，呈现不同的行为，就是多态的特性。多态可以分为编译时多态（方法重载）和运行时多态（方法重写）。<br>
抽象：提取事物的关键特性，为事物建立模型的过程。得到的抽象模型中包含属性（数据）和操作（行为）。这个抽象模型称为类。

#### 2. 面向对象的七大设计原则？
SOLID原则（<br>
&emsp;&emsp;单一职责原则：单一职责<br>
&emsp;&emsp;开放关闭原则：对扩展开放，对修改封闭，实现热插拔，提高扩展性<br>
&emsp;&emsp;里氏替换原则：实现抽象的规范，实现子类父类的相互替换<br>
&emsp;&emsp;接口隔离原则：接口单独设计，降低耦合度<br>
&emsp;&emsp;依赖倒置原则：针对接口编程<br>
）<br>
迪米特原则：不知道原则，功能模块尽量独立<br>
组合优于继承原则（合成复用原则）：尽量使用聚合、组合，而不是继承

#### 3. 单例模式的各种实现方法？code
(1) 懒汉式，线程不安全。多个线程可以实例化多个实例。<br>
(2) 懒汉式，线程安全。对getInstance方法同步，效率低<br>
(3) 饿汉式，基于classloader机制避免了多线程的同步问题，但没有达到lazy loading。<br>
(4) 饿汉式，static代码块，同上。<br>
(5) 静态内部类，同样利用了classloader机制保证实例化的时候只有一个线程，饿汉式中只要类被加载了，instance就会被实例化。这种方式类被加载了不会实例化instance，调用getInstance方法的时候才会状态内部类Holder。<br>
(6) 枚举，JVM保证enum不能被反射且构造方法只执行一次<br>
(7) DCL双检锁，（volatile避免初始化的时候指令重排？？？）
