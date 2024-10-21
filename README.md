# EXPERIMENT - 14
## Aim :
To study and implement Inheritance

## Apparatus :
Vs code

## Theory :
C++ Inheritance

Inheritance is a core concept in object-oriented programming (OOP) that allows one class to acquire the properties and behaviors of another class. This promotes code reusability, extendability, and hierarchical classification.

## Types of Inheritance

- **Single Inheritance**:
  - A derived class inherits from a single base class.

- **Multiple Inheritance**:
  - A derived class inherits from more than one base class.

- **Multilevel Inheritance**:
  - A class is derived from another derived class, forming a multi-level hierarchy.

- **Hierarchical Inheritance**:
  - Multiple derived classes inherit from a single base class.

- **Hybrid Inheritance**:
  - A combination of multiple inheritance and multilevel inheritance.

## Access Specifiers in Inheritance :

  - Public members of the base class remain public in the derived class.
  - Protected members remain protected.
  - Private members are not directly accessible but can be accessed via public/protected methods.

- **Protected Inheritance**:
  - Public and protected members of the base class become protected in the derived class.

- **Private Inheritance**:
  - Public and protected members of the base class become private in the derived class.

## Abstract Classes

- **Abstract Class**:
  - A class containing at least one pure virtual function (e.g., `virtual void func() = 0;`).
  - Cannot be instantiated directly.
  - Designed to be inherited by other classes.

## Benefits of Inheritance

- **Code Reusability**: Allows reuse of existing code.
- **Extendability**: Facilitates the addition of new features with minimal changes.
- **Polymorphism**: Supports the creation of more flexible and extensible systems by allowing derived classes to override base class methods.


## Codes - 

### 1. Single Inheritance 
```
#include <iostream>
#include <string>
using namespace std;

class Uni {
    public:
    string uni = "Symbiosis: ";
    void discipline(){
        cout<<"Engineering"<<endl;
    }
};
class Dep: public Uni {
    public:
    string dept="Electronics & TeleCommunication";
};

int main(){
    Dep u1;
    u1.discipline();
    cout<<u1.uni+" "+u1.dept;
}
```

### 2. Multiple Inheritance 
```
#include <iostream>
#include <string>
using namespace std;

// Parent Class-1
class Vehicle {
    public:string company = "Ford";
    void type() {
        cout << "Mustang" << endl;
    }
};

// Parent Class-2
class Specs {
public:
    string mileage = "8 km/l";
    
    void colour() {
        cout << "Grey" << endl;
    }
};

// Child Class (derived from both Vehicle and Specs)
class Car : public Vehicle, public Specs {
public:
    string seater = "4 seater";
};

int main() {
    Car f2;
    
    f2.colour(); 
    cout << f2.company << endl; 
    f2.type(); 
    cout << "(" << f2.seater << ")" << endl; 
    cout << "MILEAGE: " << f2.mileage << endl; 

    return 0;
}
```

### 3. Multilevel Inheritance 
```
#include <iostream>
#include <string>
using namespace std;

// Parent Class-1
class Food {
public:
    string cuisine = "Indian";
    
    void type() {
        cout << "Asian" << endl;
    }
};

// Child Class-1 (derived from Parent-1)
class Dish : public Food {
public:
    string dish = "Biryani";
};

// Child Class-2 (derived from Child-1)
class Restaurant : public Dish {
public:
    string name = "Spice Kitchen";
};

int main() {
    Restaurant f3;
    
    f3.type();  
    cout << f3.cuisine << ": " << f3.dish << endl;   
    cout << "Restaurant: " << f3.name << endl;  

    return 0;
}
```

### 4. 
```
#include <iostream>
#include <string>
using namespace std;

//Parent Class-1
class Jeans {
    public:
    string type[3]= {"Bootcut", "Wide Leg", "Skinny"};
    void brand(){
        cout<<"H&M - Denim"<<endl;
    }
};
//Child Class-1
class Bootcut: public Jeans {
    public:
    string color="Dark Blue";
};
//Child Class-2
class WL: public Jeans {
    public:
    string color="Black";
};
//Child Class-3
class Skinny: public Jeans {
    public:
    string color="Grey";
};

int main(){
    Bootcut j1;
    cout<<endl;
    j1.brand();
    cout<<j1.type[0]<<": "<<j1.color<<endl;

    WL j2;
    cout<<endl;
    j2.brand();
    cout<<j2.type[1]<<": "<<j2.color<<endl;

    Skinny j3;
    cout<<endl;
    j3.brand();
    cout<<j3.type[2]<<": "<<j3.color<<endl;
}
```

## Outputs - 
### 1- 
