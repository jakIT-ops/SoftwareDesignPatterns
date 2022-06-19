<br>
<div align="center">
  <img src="img/designpatternrel.JPG">
</div>
<br>

## Types of Design Patterns

### Creational

Creational design patterns relate to how objects are constructed from classes. New-ing up objects may sound trivial but unthoughtfully littering code with object instance creations can lead to headaches down the road. The creational design pattern come with powerful suggestions on how best to encapsulate the object creation process in a program.

* Builder Pattern
* Prototype Pattern
* Singleton Pattern
* Abstract Factory Pattern


### Structural

Structural patterns are concerned with the composition of classes i.e. how the classes are made up or constructed. These include:

* Adapter Pattern
* Bridge Pattern
* Composite Pattern
* Decorator Pattern
* Facade Pattern
* Flyweight Pattern
* Proxy Pattern

### Behavioral

Behavioral design patterns dictate the interaction of classes and objects amongst eachother and the delegation of responsibility. These include:

* Interpreter Pattern
* Template Pattern
* Chain of Responsibility Pattern
* Command Pattern
* Iterator Pattern
* Mediator Pattern
* Memento Pattern
* Observer Pattern
* State Pattern
* Strategy Pattern
* Visitor Pattern

# Creational Patterns

### Builder pattern

As the name implies, a builder pattern is used to build objects. Sometimes, the objects we create can be complex, made up of several sub-objects or require an elaborate construction process. The exercise of creating complex types can be simplified by using the builder pattern. A composite or an aggregate object is what a builder generally builds.

Formally, a <b>builder pattern encapsulates or hides the process of building a complex object and separates the representation of the object and its construction. The separation allows us to construct different representations using the same construction process. In Java speak, different representations implies creating objects of different classes that may share the same construction process.</b>

<br>
<div align="center">
  <img src="img/classDiagram.JPG">
  <br>
  <code>Class Diagram</code>
</div>
<br>

### Singleton Pattern

Singleton pattern as the name suggests is used to create one and only instance of a class. There are several examples where only a single instance of a class should exist and the constraint be enforced. Caches, thread pools, registries are examples of objects that should only have a single instance.

Its trivial to new-up an object of a class but how do we ensure that only one object ever gets created? The answer is to make the constructor private of the class we intend to define as singleton. That way, only the members of the class can access the private constructor and no one else.

Formally the Singleton pattern is defined as <b>ensuring that only a single instance of a class exists and a global point of access to it exists.</b>

<br>
<div align="center">
  <img src="img/singleton.JPG">
  <br>
  <code>Class Diagram</code>
</div>
<br>

<b>Other Examples</b>

* java.lang.Runtime
* java.awt.Desktop

### Prototype Pattern

Formally, the pattern is defined as specify the kind of objects to create using a prototypical instance as a model and making copies of the prototype to create new objects.

<br>
<div align="center">
  <img src="img/prototype.JPG">
  <br>
  <code>Class Diagram</code>
</div>
<br>

<b>Other Examples</b>

* In Java the root Object class exposes a clone method. The class implements the interface java.lang.Cloneable

### Factory Method Pattern

A factory produces goods, and a software factory produces objects. Usually, object creation in Java takes place like so:

```java
SomeClass someClassObject = new SomeClass();
```

Formally, the factory method is defined as <code>providing an interface for object creation but delegating the actual instantiation of objects to subclasses.</code>

<br>
<div align="center">
  <img src="img/factormethod.JPG">
  <br>
  <code>Class Diagram</code>
</div>
<br>

<b>Other Examples</b>

* java.util.Calendar.getInstance()
* java.util.ResourceBundle.getBundle()
* java.text.NumberFormat.getInstance()

### Abstract Factory Pattern

Formally, the abstract factory pattern is defined as <b>defining an interface to create families of related or dependent objects without specifying their concrete classes.</b>


<br>
<div align="center">
  <img src="img/abstractfactory.JPG">
  <br>
  <code>Class Diagram</code>
</div>
<br>

<b>Other Examples</b>

* <code>javax.xml.parsers.DocumentBuilderFactory.newInstance()</code> will return you a factory.

* <code>javax.xml.transform.TransformerFactory.newInstance()</code> will return you a factory.
