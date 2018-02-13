# OOP lecture 5 2/12/18


## Abstraction
  - The user will have the info on what the object does instead of how it does it
  - in java, abstraction is achieved using abstract class and interfaces
  - use the abstract key word to define an abstract method.
  - it is up to the user of this class to define how that method is implemented.

    `abstract void greeting(string greet)`
  - It is now  up to the user to define this method when they extend the class
  - abstraction functions are used when you use the `extend` keyword
  - **PROS** dont have to rewrite common methods
  - **CONS** cannot be multiply inherited

## Interfaces
  - interface is a class full of abstractions.
  - you define how a class should look but not the actual methods.
  - interfaces are **implemented** with `implement` key word.
  - **PROS** can implement multiple interfaces
  - **CONS** of interfaces are that each class must have its own implementation of the functions in that interface.


> You can only **extend** one class but you can **implement** many classes.
- Interfaces vs Abstraction


## Upcasting
  - Parent classes that are used as extension of other classes can be used to instantiate an object of sub classes
  - If the parent class  `Art` is extended in a sub class `Cartoon` so `public class Cartoon extends Art{}`
    then a cartoon object can be created as such.
      `Art myArt = new Cartoon()`


## Downcasting
   - Downcasting is not as simple as Upcasting.
   - You must class the sub class onto the parent class in order for you to downcast it like so:
   >`Cartoon myCartoon = (Cartoon) myArt`
   - Here we cast `Cartoon` onto `myArt` a previously declared `Art` obj.


## Polymorphism
  - The ability of an object to be associated with a super class so it can be grouped with other sub classes.
  - This relies on the principal of upcasting.
  - For example if I have a super class Orchestra obj then I can create an array of Orchestra objs filled with sub  classes in the Orchestra like so.

  `Orchestra[] myOchestra = new Ochestra(new WoodWind(), new Brass())`
    Here `woodWind` and Brass extend the super class `Ochestra` so they can be defined in an Orchestra array with **Polymorphism.**
