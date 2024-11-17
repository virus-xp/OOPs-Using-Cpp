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

### Rough Code ₰

```cpp
#include <iostream>
#include <string>
using namespace std;

class Teacher {
private:
    double salary;

public:

    //Constructor
    //This is also Non-Parameterized Constructor
    Teacher() {
        cout << "Teacher Object Created" << endl;
        // or if i wanna make a default value for salary then i can do this here
        salary = 0;
    }
    //This is also Parameterized Constructor
    Teacher(string n, string d, string s, double sal) {
        cout << "Teacher Object Created" << endl;
        name = n;
        dept = d;
        subject = s;
        salary = sal;
    }

    //Copy Constructor
    Teacher(const Teacher &t) {
        cout << "Teacher Object Created" << endl;
        name = t.name;
        dept = t.dept;
        subject = t.subject;
        salary = t.salary;
    }

    //properties / attributes
    string name;
    string dept;
    string subject;
    //double salary;


    //methods
    void ChangeDept(string newDept) {
        dept = newDept;
    }
    // Special function to give access for private member
    //setter
    void setSalary(double s) {
        salary = s;
    }
    //getter
    double getSalary() {
        return salary;
    }
};

//TODO: Example for Encapsulation:
class Account {
private:
    double salary; // data hiding
    string password; // data hiding

public:
    string accountId;
    string username;
   
};

int main() {
    // Parameterized Constructor
    Teacher t2("Sikandar", "School Of Engineering & Technology", "Computer Science & Engineering", 250000);
    
    Teacher t1; // Automatically call Constructor
    t1.name = "Sikandar";
    t1.subject = "Computer Science & Engineering";
    t1.dept = "School Of Engineering & Technology";
    t1.setSalary(250000);

    cout << "Teacher 1 Name: " << t1.name << endl;
    cout << "Teacher 1 Subject: " << t1.subject << endl ;
    cout << "Teacher 1 Departement: " << t1.dept << endl ;
    cout << "Teacher 1 Salary: " << t1.getSalary() << endl ;


    // Teacher t2;
    // Teacher t3;
    // Teacher t4;

    return 0;
}
```
---
