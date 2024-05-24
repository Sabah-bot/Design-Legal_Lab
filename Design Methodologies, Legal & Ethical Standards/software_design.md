# Software Design Methodologies - Answers!

## Introduction

There is no single correct way to approach a software engineering problem. Designing a product which satisfies a customer's needs while leveraging a team's skillset (and delivering on time and on budget) isn't something with a one-size-fits-all solution. There is, however, usually one option which is a better fit for a given situation than others. In this exercise we will find out about some of the different ways in which we could go about designing a system.

## Design Strategies

There are three principle design strategies used in software engineering:

- Structured design
- Function oriented design
- Object oriented design

None of these are compulsory when designing a product but following one will greatly aid the process. Each has its benefits and each has its drawbacks. Unlike many other aspects of software engineering they generally exist in isolation as the principles of each sit in direct opposition to each other in some scenarios.

There is no scenario where one of these strategies _can't_ be used, but we may be making our lives harder by choosing one over another. Likewise the majority of programming languages can be used with any strategy, but some are better fits for one strategy than another. For example Java is an excellent choice for an object oriented design while Scala would be a better choice for a functional design. Some languages such as Python can be used effectively with either, but have to sacrifice some features to achieve that flexibility.

Within each methodology there are various **design patterns** which provide further structure for us. In general though these are much more easily transferred across methodologies, although the precise implementation will vary by language. In practice the language used for a project will likely be the last thing to be chosen, determined by a combination of methodology and design pattern.

## Task

In this exercise you will be required to research the design strategies listed above and answer some questions about them. Your answers should be in a markdown (`.md`) file and uploaded to GitHub, then the link submitted using the lab submission form. There is no MVP/extension split for this task - you should attempt to answer every question. You can collaborate with others in the cohort on the research part of the task but everyone should submit their own answers.


1. What do we mean by **coupling** and **cohesion** when discussing structured design?

Coupling refers to the degree of direct connection that one component or module has of another. In software design, low coupling is preferred as it indicates that components are independent and changes in one component are less likely to impact others. This promotes flexibility and maintainability. As a result High coupling means that a change in one component affects many others, making the system complex, rigid, and fragile

A good example is a module is said to have low cohesion if it contains unrelated elements. For example, a User class containing a method on how to validate the email address. User class can be responsible for storing the email address of the user but not for validating it or sending an email:

Cohesion and coupling are related to each other. Each can affect the level of the other.

High cohesion correlates with loose coupling. A module having its elements tightly related to each other and serving a single purpose would sparingly interact and depend on other modules. Thus, will have loose coupling with other modules.

Similarly, the tight coupling could be a sign of low cohesion. Modules could be heavily dependent on each other due to the elements spread across the two modules. And thus, will have low cohesion.

![alt text](https://www.baeldung.com/wp-content/uploads/sites/4/2021/05/comparison.png)

2. What is the difference between **top-down** and **bottom-up** design? Which best describes a function oriented design?

Top-down design starts with the highest-level components of a system and progressively breaks them down into more detailed components. This approach is often used in structured programming and function-oriented design.

Bottom-up design begins with the most basic or low-level components and integrates them to form higher-level systems. This approach is often used in object-oriented design.

Function-oriented design is best described by the top-down design approach, where the system is decomposed into functions or procedures.

3. In which design methodology would a **class diagram** be most useful?

Class diagrams are most useful in object-oriented design methodologies. They provide a visual representation of the classes in a system and their relationships, making it easier to design and understand the structure of an object-oriented system.


4. What are the **four pillars of object oriented programming**? Give a single-sentence description of each.

**Encapsulation**
Encapsulation is the concept of bundling the data (attributes) and methods (functions) that operate on the data into a single unit, usually a class, and restricting access to some of the object's components.

**Abstraction**
Abstraction involves hiding the complex implementation details of a system and exposing only the necessary and relevant parts. It helps in reducing complexity and allows focusing on the interaction at a high level.

**Inheritance**
Inheritance is a mechanism where a new class (subclass) is derived from an existing class (superclass). The subclass inherits attributes and methods from the superclass, promoting code reusability.

**Polymorphism**
Polymorphism allows objects of different classes to be treated as objects of a common superclass. It enables a single interface to represent different underlying forms (data types).

![alt text](https://miro.medium.com/v2/resize:fit:720/format:webp/1*BirtADeool-n8VNsXYAoZg.png)


5. What is the **strategy pattern**? How would its implementation differ between a functional and object oriented system?

The strategy pattern is a behavioral design pattern that defines a family of algorithms, encapsulates each one, and makes them interchangeable. It allows the algorithm to vary independently from clients that use it.

In a functional system, the strategy pattern can be implemented using higher-order functions. Different strategies can be defined as separate functions and passed as arguments to a higher-order function that uses these strategies.

In an object-oriented system, the strategy pattern can be implemented using interfaces or abstract classes to define a common strategy interface. Concrete strategy classes implement this interface, and the context class holds a reference to a strategy object and delegates the algorithm execution to it.


6. Imagine your is creating a new online payment system. In order to gain maximum market share it can't be tied to a particular sector - it needs to work just as well when ordering a takeaway as when buying a new coat. Which design methodology would you suggest following? Give some justification for your decision.

I would suggest following an object-oriented design methodology for creating the new online payment system.

Object-oriented design allows for high modularity, flexibility, and reusability, which are crucial for a system that needs to operate across various sectors. The use of encapsulation ensures that payment details are securely managed, while inheritance and polymorphism provide the flexibility to handle different types of transactions and payment methods. Additionally, object-oriented design can simplify maintenance and scalability as the system evolves and new features are added.
