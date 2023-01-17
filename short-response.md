# Problem Set 4-5

## Classes and Inheritance 

**1. What is inheritance in programming?**

**Inhertiance** is when a new class has all the functionality of the class in which it derived from while having its own functionality as well. The new class is called a *child*  and the other class that it inherits from is refered to as the *parent* class.

**2. In a code snippet, demonstrate inheritance by creating two classes where one is the parent class and one is the child class.**
```javascript

class Car {
  constructor(color, speed) {
    this._speed = speed;
    this._color = color;
  }
}

class BMW extends Car {
  constructor(color, speed, make) {
    super(color, speed);
    this._make = make;
  }

  aboutMe() {
    return `I'm  ${this._make}  , my color is ${this._color}, and my speed is ${this._speed}
  }
}

//Car is this parent class, and BMW is the child class. 
```
**3. What is polymorphism? Show an example in a code snippet.**

Polymorphism is the idea that we can perform a task in multiple forms or ways and is applied of functions and methods.
Both the parent and child class have the `area()` method, but depending on which object the method is used on each time it is called it will output different things. `ob` is a new instance of `class B`, so when `area` is called on `ob` not only does it calculate `100 * 200` it also `console. logs` "Class B" and the reason it can calculate `100 * 200` is because of the `super class A`.

```javascript

  class A {
        area(x, y) {
            console.log(x * y);
        }
    }
    class B extends A {
        area(a, b) {
            super.area(a, b);
            console.log('Class B')
        }
    }
    var ob = new B(); 
    var output = ob.area(100, 200); // 20000 'Class B'
    ```
    
