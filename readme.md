# Design Patterns Notes

## Note: A lot of these notes and codes is based on the [Design Patterns](https://refactoring.guru/design-patterns).

<details>
<summary> strategy Pattern </summary>

## Strategy Pattern:

### Defination

- Strategy is a behavioral design pattern that lets you define a family of algorithms, put each of them into a separate class, and make their objects interchangeable.

### Problem

- Any change to one of the algorithms, whether it was a simple bug fix or a slight adjustment of the street score, affected the whole class, increasing the chance of creating an error in already-working code.
  In addition, teamwork became inefficient. Your teammates, who had been hired right after the successful release, complain that they spend too much time resolving merge conflicts. Implementing a new feature requires you to change the same huge class, conflicting with the code produced by other people.

### Solution

- The Strategy pattern suggests that you take a class that does something specific in a lot of different ways and extract all of these algorithms into separate classes called strategies.
  The original class, called context, must have a field for storing a reference to one of the strategies. The context delegates the work to a linked strategy object instead of executing it on its own.
  The context isn’t responsible for selecting an appropriate algorithm for the job. Instead, the client passes the desired strategy to the context. In fact, the context doesn’t know much about strategies. It works with all strategies through the same generic interface, which only exposes a single method for triggering the algorithm encapsulated within the selected strategy.
  This way the context becomes independent of concrete strategies, so you can add new algorithms or modify existing ones without changing the code of the context or other strategies.

### UML Diagram

![uml_strategy_pattern](https://refactoring.guru/images/patterns/diagrams/strategy/structure-2x.png?id=5bd791857c3bab419bcf4fa86877439d)

### Pros and Cons

![strategy_pattern_pros_and_cons](screenshots/strategyPatternPros&Cons.jpg)

</details>

<details>
<summary> Observer Pattern </summary>

## Observer Pattern:

### Defination

- Observer is a behavioral design pattern that lets you define a subscription mechanism to notify multiple objects about any events that happen to the object they’re observing.

### Problem

- It's a Poll problem. Imagine that you have subscripers objects that every now and then ask the publisher class if it has any change and act accordingly.This is a very common problem in the real world.

### Solution

- The Observer pattern suggests that you add a subscription mechanism to the publisher class so individual objects can subscribe to or unsubscribe from a stream of events coming from.Now, whenever an important event happens to the publisher, it goes over its subscribers and calls the specific notification method on their objects.

### UML Diagram

![uml_observer_pattern](https://refactoring.guru/images/patterns/diagrams/observer/structure-2x.png)

### Pros and Cons

![observer_pattern_pros_and_cons](screenshots/observerPatternPros&Cons.jpeg)

</details>
