# Polymorphism & Composition Homework

## Polymorphism

1 What does the word 'polymorphism' mean?

Poly means 'many' and 'morph' means change, therefore, polymorphism is the ability to change to take on many forms.

2 What does it mean when we apply polymorphism to OO design? Give a simple Java example.
Polymorphism lets us set up methods in a parent class that are inherited by the child classes and can then be used to perform the same action but in different ways.

Example from Theme Park Homework - Stalls and RollerCoaster inherited from ISecurity
```
    public boolean isAllowed(Visitor visitor) {
        return visitor.getAge() >= 18;
    }
```

```
    public boolean isAllowed(Visitor visitor) {
        return visitor.getHeight() >= 145 && visitor.getAge() > 12;
    }
```


3 What can we use to implement polymorphism in Java?
Interfaces are used to implement polymorphism.

4 How many 'forms' can an object take when using polymorphism?
There are no limits to the number of forms an object can take using polymorphism.

5 Give an example of when you could use polymorphism.
As above Theme Park example - when some of the attractions and stalls have conditions of use such as height or age that need to be met to allow a user to proceed. 


## Composition and Aggregation

1 What do we mean by 'composition' in reference to object-oriented programming?
Composition is where an object is made up of smaller parts.

2 When would you use composition? Provide a simple example in Java.

```
class Car {
    private String make;
    private String model;
    private Engine engine;
    private GearBox gearBox;

    public Car(String make, String model, Engine engine, Gearbox gearbox) {
        this.make = make;
        this.model = model;
        this.engine = engine;
        this.gearbox = gearbox;
    }
```

3 Give a difference between composition and aggregation?
Composition is where something is built of smaller parts that go together to make the whole object - such a house being _**composed**_ of walls, roof, windows etc in other words they are _**a part of**_ the house. If any one part is missing then the other parts can't exist.

Aggregation is where something can be built of smaller parts that go together to make the whole object - such as an engine, tyres and battery. They are _**aggregated**_ together to make the car in other words the car -**has**_ an engine, tyres and a battery. The car can still exist if any part is not added ie an clutch pedal is not added to an automatic car.

4 What is/are the advantage(s) of using composition/aggregation?
Code is cleaner and reusable.

5 When using composition, when an object is destroyed, what happens to all the objects it is composed of?
They can't exist on their own.

6 When using aggregation, when an object is destroyed, what happens to all the objects it is composed of?
They can continue to exist.