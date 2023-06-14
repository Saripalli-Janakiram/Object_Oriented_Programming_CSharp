# Source Generated From Chat GPT #
# OBJECT ORIENTED PROGRAMMING USING C#
# The main concepts of object-oriented programming (OOP) are:

1. Classes and Objects: A class is a blueprint for creating objects, which are instances of that class. A class defines the properties and methods that an object will have.

2. Encapsulation: Encapsulation is the concept of hiding the internal details of an object and providing a public interface for interacting with it. 
This protects the object's data and behavior from outside interference and ensures that it can only be accessed through the methods that are defined in its class.

3. Inheritance: Inheritance is the concept of creating new classes that are derived from existing classes. This allows the new classes to inherit the properties and methods of the parent class, 
and also to override or extend them as needed.

4. Polymorphism: Polymorphism is the concept of having multiple forms or behaviors for a single object or method. This allows objects of different classes to be treated as if they were of the same class,
 and also allows methods to be defined in a way that can handle different types of objects.

5. Abstraction: Abstraction is the concept of focusing on the essential features of an object and ignoring the details that are not relevant to its behavior. 
This allows for more flexible and maintainable code, as changes to the implementation details of an object do not affect the way it is used by other parts of the program.

Object-oriented programming (OOP) is a programming paradigm that is based on the concept of "objects." Objects are instances of classes, which are used to represent real-world entities and abstract concepts. 
C# is a popular programming language that supports OOP concepts, and it is widely used for building desktop, web, and mobile applications.
In C#, a class is a blueprint for creating objects. It defines the properties and methods that an object will have.
For example, if we were creating a program to represent a car, we might create a Car class that would have properties like color, make, model, and year, as well as methods like Start(), Stop(), Accelerate(), and Brake().
Look at the example below:
```csharp
public class Car
{
    public string Color { get; set; }
    public string Make { get; set; }
    public string Model { get; set; }
    public int Year { get; set; }

    public void Start()
    {
        // Code to start the car
    }

    public void Stop()
    {
        // Code to stop the car
    }

    public void Accelerate()
    {
        // Code to accelerate the car
    }

    public void Brake()
    {
        // Code to apply the brakes
    }
}
```
Once we have defined a class, we can create objects based on that class. For example, we might create a new Car object like this:
// Syntax
```
Car myCar = new Car();
```

We can then set the properties of the object like this:
myCar.Color = "Red";
myCar.Make = "Toyota";
myCar.Model = "Camry";
myCar.Year = 2022;

And we can call the methods of the object like this:
myCar.Start();
myCar.Accelerate();
myCar.Brake();
myCar.Stop();

This is just a simple example, but it illustrates the basic concepts of object-oriented programming in C#. By defining classes and creating objects based on those classes,
we can create complex programs that model real-world systems and solve real-world problems.

These concepts provide a framework for building modular, reusable, and extensible code that can model complex real-world systems and solve a wide range of problems. 
OOP languages like C#, Java, and Python have built-in support for these concepts, making it easy for developers to write code that is organized, efficient, and easy to maintain.
# Encapsulation
Encapsulation is one of the fundamental principles in object-oriented programming (OOP) and plays a crucial role in the C# programming language. It is the process of bundling data and methods (or functions) together into a single unit called a class, and controlling access to that class's members. The primary goal of encapsulation is to hide the internal details and complexities of an object and provide a public interface through which other objects can interact with it.

In C#, encapsulation is achieved by using access modifiers to specify the accessibility of class members. There are four access modifiers in C#:

1. Public: Public members are accessible from anywhere in the program. They can be accessed by instances of the class, derived classes, and other classes.

2. Private: Private members are accessible only within the same class. They cannot be accessed from outside the class, including derived classes.

3. Protected: Protected members are accessible within the same class and derived classes. They cannot be accessed from outside the class hierarchy.

4. Internal: Internal members are accessible within the same assembly (or project). They cannot be accessed from outside the assembly.

By default, class members (fields, properties, and methods) are private if no access modifier is specified. It is a common practice to make fields private and expose them through public properties, which provide controlled access to the data stored in the class.

Encapsulation allows you to control how external entities interact with your class. It enables you to enforce constraints and validations on the class's internal data, ensuring data integrity and maintaining the class's state. By hiding the implementation details, you can modify the internal workings of the class without affecting other parts of the program that use the class.

Here's a simple example to illustrate encapsulation in C#:

```csharp
public class Person
{
    private string name;  // Private field
    
    public string Name   // Public property
    {
        get { return name; }
        set { name = value; }
    }
    
    public void SayHello()  // Public method
    {
        Console.WriteLine("Hello, my name is " + name);
    }
}
```

In the example above, the `name` field is encapsulated and made private. Access to the `name` field is provided through the public `Name` property, which allows controlled access to the field. The `SayHello` method is also public, allowing other parts of the program to interact with the `Person` class and invoke the method.

Encapsulation promotes code organization, enhances code reusability, and improves maintainability by providing a clear separation between the internal implementation of a class and its public interface. It also helps prevent accidental modification of data and enforces consistent usage of the class throughout the program.
