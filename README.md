# Object-Oriented Programming (OOP) in C++
<p align="center">
  <b>Salik Seraj Naik®</b>
</p>
## Introduction
Object-Oriented Programming (OOP) is a programming paradigm based on the concept of "objects", which can contain data and code to manipulate that data. C++ is a popular language that supports OOP.

## Key Concepts

### 1. Classes and Objects
- **Class**: A blueprint for creating objects (a particular data structure).
- **Object**: An instance of a class.

```cpp
class Car {
public:
    string brand;
    string model;
    int year;
};

Car myCar;
```

### 2. Encapsulation
Encapsulation is the bundling of data and methods that operate on the data within one unit, e.g., a class. It restricts direct access to some of the object's components.

```cpp
class Car {
private:
    string brand;
    string model;
    int year;

public:
    void setBrand(string b) {
        brand = b;
    }

    string getBrand() {
        return brand;
    }
};
```

### 3. Inheritance
Inheritance is a mechanism where a new class inherits properties and behavior (methods) from an existing class.

```cpp
class Vehicle {
public:
    string brand = "Ford";
    void honk() {
        cout << "Tuut, tuut!" << endl;
    }
};

class Car : public Vehicle {
public:
    string model = "Mustang";
};
```

### 4. Polymorphism
Polymorphism means "many shapes" and it allows methods to do different things based on the object it is acting upon.

```cpp
class Animal {
public:
    virtual void makeSound() {
        cout << "Some generic animal sound" << endl;
    }
};

class Dog : public Animal {
public:
    void makeSound() override {
        cout << "Woof" << endl;
    }
};
```

### 5. Abstraction
Abstraction means hiding the complex implementation details and showing only the necessary features of an object.

```cpp
class AbstractCar {
public:
    virtual void startEngine() = 0; // Pure virtual function
};

class Tesla : public AbstractCar {
public:
    void startEngine() override {
        cout << "Tesla engine started" << endl;
    }
};
```

## Conclusion
OOP in C++ helps in organizing complex programs, making them easier to manage and understand. The key concepts of OOP are classes and objects, encapsulation, inheritance, polymorphism, and abstraction.
