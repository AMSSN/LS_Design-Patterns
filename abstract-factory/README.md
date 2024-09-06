## Abstract Factory

Abstract factory pattern has creational purpose and provides an interface for 
creating families of related or dependent objects without specifying their 
concrete classes. Pattern applies to object and deal with object relationships, 
which are more dynamic. In contrast to Factory Method, Abstract Factory pattern
produces family of types that are related, ie. it has more than one method of 
types it produces.


### When to use

* a system should be independent of how its products are created, composed, and represented
* a system should be configured with one of multiple families of products
* a family of related product objects is designed to be used together
* you want to provide a class library of products, and you want to reveal just their interfaces, not their implementations



### 抽象工厂

抽象工厂模式以创建为目的，它提供了一个接口，用于创建相关或从属的对象族，而无需指定它们的具体类。该模式适用于对象并处理对象关系，这种关系更加动态。与工厂方法（Factory Method）相比，抽象工厂模式产生的类型族是相关的，即它产生的类型有不止一个方法。


### 何时使用

* 系统应独立于其产品的创建、组成和表示方式
* 一个系统应配置多个产品系列中的一个系列
* 相关产品对象的系列被设计为一起使用
* 你想提供一个产品类库，而你只想揭示它们的接口，而不是它们的实现方式


定义产品接口：  
ProductA 和 ProductB 定义了产品的接口。这些接口规定了所有具体产品必须实现的方法，例如 getName()。  
具体产品实现：  
ConcreteProductAX 和 ConcreteProductAY 继承自 ProductA，并实现了 getName() 方法。  
ConcreteProductBX 和 ConcreteProductBY 继承自 ProductB，并实现了 getName() 方法。  
每个具体产品都返回不同的字符串，用于标识其类型。  
抽象工厂：  
AbstractFactory 定义了一个抽象接口，包含两个方法：createProductA() 和 createProductB()。这些方法用于创建 ProductA 和 ProductB 的实例。  
具体工厂：  
ConcreteFactoryX 继承自 AbstractFactory，并实现了 createProductA() 和 createProductB() 方法。  
ConcreteFactoryX 创建 ConcreteProductAX 和 ConcreteProductBX 的实例。  
ConcreteFactoryY 同样继承自 AbstractFactory，并创建 ConcreteProductAY 和 ConcreteProductBY 的实例。  
主函数：  
创建 ConcreteFactoryX 和 ConcreteFactoryY 的实例。使用工厂创建 ProductA 和 ProductB 的实例，并输出其名称。最后释放所有分配的内存。  



![](..\imgsource\abstract-factory1.png)


