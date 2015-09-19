# designPattern
php设计模式


心得笔记

设计模式：在软件开发过程中，经常出现的典型场景的典型解决方案，称为设计模式。

设计模式常常是因为某种语言不能达到某种目的而设计产生，但是在php中，很多设计模式都被自然消除了，有些设计模式在实际开发过程中可能用的地方不太多，但是设计模式的思想却非常值得学习。

1、多态

在面向对象过程中，指某种对象实例的不同表现形态。

多态特点，在静态语言中体现的更为明显。

即在C等强类型语言中，函数传入参数必须指明类型，并且传入的参数如果类型不对，则程序无法运行。在php中，则可以不指明参数类型，弱类型语言可以体现。则也可以传入类型，比如int ,Array ,或者某个类名（传入的值必须为该类的实例），此时若传入参数不符合指定的类型，程序无法运行。

那么多态就是，例如01.php中描述，只要写一个父类，就可以传入各个子类的类型，各自子类又变现各异，因为每个子类都属于其父类，从而这样无论再传哪个子类的实例都不会报错了，进而实现多态。

php太灵活了，搞得多态的意义好像不是很大了呢。。。。

例子   01.php


2、简单工厂模式

php程序员可能体会不到调用端与客户端的作用，因为有什么方法直接打开就能看，不像java，打成一个包，然后调用其方法，看不到里面的方法。

例子   02.php


3、工厂模式

例子：可参照hfphp框架中Factory.class.php，已使用工厂模式，根据不同的GET值实例化不同的类

4、单例模式
链接数据库，操作cookie，上传等场景中，保证该类的只实例化一个，即为单例模式

如果在外部实例化类，那必然会产生不同的对象,所以要在类的内部进行实例化

基本步骤：

1、封锁new 操作
2、内部new对象
3、getIns预先判断实例
4、加final,防止继承，再被实例化
5、还有防止克隆

具体情况根据场景不同有所改变。

04.php  DB.class.php


















