# SOLID principles in C#

If you want to read it in detail checkout this article:[SOLID Principles](https://www.c-sharpcorner.com/UploadFile/damubetha/solid-principles-in-C-Sharp/) written by Damodara Naidu.

## Overview

SOLID design principles in C# are basic design principles. **SOLID** stands for **Single Responsibility Principle (SRP)**, **Open closed Principle (OCP)**, **Liskov substitution Principle (LSP)**, **Interface Segregation Principle (ISP)**, and **Dependency Inversion Principle (DIP)**.

### Introduction to SOLID principles

- **S: Single Responsibility Principle (SRP)**

SRP says, "Every software module should have only one reason to change.".
This means that every class or similar structure in your code should have only one job. Everything in that class should be related to a single purpose. Our class should not be like a Swiss knife wherein if one of them needs to be changed, the entire tool needs to be altered. It does not mean that your classes should only contain one method or property. There may be many members as long as they relate to a single responsibility.

The Single Responsibility Principle gives us a good way of identifying classes at the design phase of an application, and it makes you think of all the ways a class can change. However, a good separation of responsibilities is done only when we have the full picture of how the application should work.

- **O: Open/Closed Principle**

The Open/closed Principle says, "A software module/class is open for extension and closed for modification."

Here "Open for extension" means we must design our module/class so that the new functionality can be added only when new requirements are generated. "Closed for modification" means we have already developed a class, and it has gone through unit testing. We should then not alter it until we find bugs. As it says, a class should be open for extensions; we can use inheritance.

- **L: Liskov Substitution Principle**

The Liskov Substitution Principle (LSP) states, "you should be able to use any derived class instead of a parent class and have it behave in the same manner without modification.". It ensures that a derived class does not affect the behavior of the parent class; in other words, a derived class must be substitutable for its base class. This principle is just an extension of the Open Closed Principle, and we must ensure that newly derived classes extend the base classes without changing their behavior.

- **I: Interface Segregation Principle**

The Interface Segregation Principle (ISP) states "that clients should not be forced to implement interfaces they don't use. Instead of one fat interface, many small interfaces are preferred based on groups of methods, each serving one submodule.".
We can define it in another way. An interface should be more closely related to the code that uses it than the code that implements it. So the methods on the interface are defined by which methods the client code needs rather than which methods the class implements. So clients should not be forced to depend upon interfaces they don't use.
Like classes, each interface should have a specific purpose/responsibility (refer to SRP). You shouldn't be forced to implement an interface when your object doesn't share that purpose. The larger the interface, the more likely it includes methods not all implementers can use. That's the essence of the Interface Segregation Principle.

- **D: Dependency Inversion Principle**

The Dependency Inversion Principle (DIP) states that high-level modules/classes should not depend on low-level modules/classes. First, both should depend upon abstractions. Secondly, abstractions should not rely upon details. Finally, details should depend upon abstractions.
High-level modules/classes implement business rules or logic in a system (application). Low-level modules/classes deal with more detailed operations; in other words, they may write information to databases or pass messages to the operating system or services.
A high-level module/class that depends on low-level modules/classes or some other class and knows a lot about the other classes it interacts with is said to be tightly coupled. When a class knows explicitly about the design and implementation of another class, it raises the risk that changes to one class will break the other. So we must keep these high-level and low-level modules/classes loosely coupled as much as possible. To do that, we need to make both of them dependent on abstractions instead of knowing each other
