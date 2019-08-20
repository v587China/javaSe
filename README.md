## **Java核心技术卷一**

### **第四章类和对象**

`私有方法:不能被其它类调用的方法`

`final实例域:构建对象时必须初始化这样的域(直接初始化或者每一个构造函数初始化),且不能被修改;实例域是对象时则表示引用不会指向其他对象,但是对象的状态是可变的`

`静态域:类级别的属性,所有对象共有`

`静态方法:类级别的方法,所有对象共有`

`类设计技巧`

- `一定要保证数据私有`

- `一定要对数据初始化`

- `不要在类中使用过多的基本类型`

- `不是所有的域都需要独立的域访问器和域更改器`

- `将职责过多的类进行分解`

- `类名和方法名要能够体现它们的职责`

- `优先使用不可变的类`

### **第五章继承**

`解决的问题:继承已存在的类就是复用(继承)这些类的方法和域,添加新的方法和域,以满足新的需求`

`继承后的问题:属性,方法,构造器`

`父类的私有方法,属性,构造函数,子类不能直接访问,可以通过父类提供的共有方法访问`

`父子同名的非私有方法,属性,构造函数,子类通过super关键字调用父类的`

`不想被继承的类或方法使用final`

`抽象类:抽象类不能被实例化`

### **第六章接口,lambda表达式,内部类**

#### **lambda表达式**

`只有一个抽象方法的接口称为函数式接口(functional interface),可以提供一个lambda表达式,lambda表达式中不能改变变量`

`函数式接口(functional interface),建议使用@FunctionalInterface注解来标记并约束这个接口`

`方法引用:已经有现成的方法可以完成你想要传递到其他代码的某个动作`

 - `用::操作符分隔方法名与对象或类名.主要有3种情况`

   - `object::instance Method``可以使用this,super作为目标`

   - `Class::static Method`

   - `Class::instance Method``第1个参数会成为方法的目标`

`构造器引用:类型::new;eg:Integer::new.int[]::new`

#### **内部类**




### **第8章泛型程序设计**

`泛型程序设计(Generic programming)意味着编写的代码可以被很多不同类型的对象所重用`

`使用泛型机制编写的程序代码要比那些杂乱地使用Object变量,然后再进行强制类型转换的代码具有更好的安全性和可读性`

`泛型类.泛型方法`

`类型变量限定:限定类型用&分隔,在Java的继承中,可以根据需要拥有多个接口超类型,但限定中至多有一个类如果用一个类作为限定,它必须是限定列表中的第一个`

`泛型代码和虚拟机:虚拟机没有泛型类型对象,所有对象都属于普通类`

   - `类型擦除:擦除(erased)类型变量,并替换为第一个限定的类型(无限定的变量用Object)(class Interval<T extends Serializable&Comparable >如果这样做,
   原始类型用Serializable替换T 而编译器在必要时要向Comparable插入强制类型转换.为了提高效率,应该将标签(tagging)接口(即没有方法的接口)放在边界列表的末尾)`

   - `翻译泛型表达式:程序调用泛型方法时,如果擦除返回类型,编译器插入强制类型转换`

   - `翻译泛型方法:`






