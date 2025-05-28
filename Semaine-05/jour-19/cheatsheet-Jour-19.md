# Inheritance

4 types of inheritance

* Single inheritance
One class inherits from only one parent class.

* Multiple inheritance
A class inherits from more than one class.

* Multilevel inheritance
A class inherits from one class, which inherits from another class and so on

* Hierarchical inheritance
Child classes all inherit from a single base class.
Similar to *single inheritance* but we're creating more child classes.

And

* Hybrid inheritance
when we use several types of inheritance.
Esp. the case in complex applications.

## Overriding and inheritance

In most OOP, you can override the variables of a parent class in the child class.

## Differences between Interface and abstract classes

Abstract class has at least one method that's not defined
Interface has all its methods undefined.

* Typescript adds interface support to JS

## Objects relationships (UML)

Unified Modelling Language : UML class diagrams are mostly used in software engineering for modeling the static structure of applications.

https://www.visual-paradigm.com/guide/uml-unified-modeling-language/uml-aggregation-vs-composition/

* Association  
Objects know about each other but exist independently

Example :

```js
class Driver {
  constructor(name) {
    this.name = name;
  }
}

class Car {
  constructor(model) {
    this.model = model;
    this.driver = null;
  }
  
  assignDriver(driver) {
    this.driver = driver; // Association: car knows about driver
  }
}

const john = new Driver("John");
const toyota = new Car("Camry");
toyota.assignDriver(john); // They're associated but independent
```

* Aggregation  
One object contains others but the contained objects can exist without the container.

Example:

```js
class Student {
  constructor(name) {
    this.name = name;
  }
}

class Classroom {
  constructor() {
    this.students = []; // Classroom "has" students
  }
  
  addStudent(student) {
    this.students.push(student);
  }
}

const student1 = new Student("Alice");
const classroom = new Classroom();
classroom.addStudent(student1); 
// Student can exist even if classroom is destroyed
```

* Composition  
The contained objects cannot exist without the container

## Polymorphism

Several classes have the same methods
Also, allows objects to be treated as if they're identical

--

Surcharge - héritage - polymorphisme

--
