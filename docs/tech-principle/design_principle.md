# 经典系统设计原则

> 经典的系统设计原则一定离不开经典的思维方式

- SOLID 原则
单一职责原则，Single Responsibility Principle(SRP)
> There should never be more than one reason for a class to change."[5] In other words, every class should have only one responsibility.

开放封闭原则，Open-Closed Principle(OCP)
> Software entities ... should be open for extension, but closed for modification. 这意味着当需要添加新功能时，应该扩展现有的实体，而不是修改它们。

里氏替换原则，即Liskov Substitution Principle(LSP)
> 所有引用基类别的地方必须能够透明地使用其子类别的对象。换句话说，子类别应该可以替换其父类别并且不会破坏系统的正确性。

接口隔离原则，Interface Segregation Principle(ISP)
> 隔离意味着保持独立，接口隔离原则是关于接口的独立性。客户端不应该被迫依赖于它不使用的接口。接口应该被拆分为更小和更具体的部分，以便客户端只需要知道它们所需的部分。

依赖反转原则，Dependency Inversion Principle(DIP)
> Depend upon abstractions, [not] concretes. 该原则描述的是我们的 class 应该依赖接口和抽象类而不是具体的类和函数。

- SLAP(Single Level of Abstration Principle, SLAP) 原则
抽象一致性原则：可以减少混乱，降低理解成本，思想源自组合方法模式(Composed Method Pattern, CMP)。该原则强调每个方法中的所有代码都处于同一级抽象层次。如果高层次抽象和底层细节杂糅在一起，就会显得代码凌乱，难以理解，从而造成复杂性。

## 抽象思维训练方法

- 程序命名训练：不要放过任何一个带有歧义，表达模糊，语义不清的命名
- 领域建模训练：对问题域的分析，整理，抽象，划分和建模，都是对抽象思维的一次训练。包括对优秀源码的研究，都可以试图揣摩其背后的抽象建模思维。


