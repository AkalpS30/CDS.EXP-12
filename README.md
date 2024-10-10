# CDS.EXP-12
## Aim:
**To study and implement Constructors and Destructors.**

## Software:
`Microsoft VSCode`

## Theory:
Constructors:

A constructor is a member functoin of a class that has the same name as the class name.

It helps to initialize the object of a class.
It is called whenever an instance of the class is created.
Constructors are mostly declared inthe pulic section of the class though it can be declared in the private section of the class.
Constructors can be overloaed.
They can be defined inside or outside the class declaration.
They are classified into three types - (1) Default Constructor, (2) Parameterized Constructor and (3) Copy Constructor.

Destructors:
A destructor is also a specialmember function like a constructor. Destructor destroys the class objects created by the constructor.
Destructor has the same name as their class name preceded by a tilde (~) symbol.
It is not possible to define more than one destructor.
Destructor cannot be overloaded.

Destructor neither requires any argument nor returns any value.
It is automatically called when an object goes out of scope.
Destructor release memory space occupied by the objects created by the constructor. Objectsaredestroyedc in the reverse of an object creation.
## Code: 12A
```
// NAME - AKALP SARKAR
// PRN- 23070123116
// EXPERIMENT - 12(A) 

#include<iostream> 
#include<string>
using namespace std; 
class Data {
    string name;
    int roll_no;
    char dept[50];
    char division;

    public:
    Data() {
        cout<<"Name: ";
        cin>>name;
        cout<<"Roll Number: ";
        cin>>roll_no;
        cout<<"Department: ";
        cin>>dept;
        cout<<"Division: ";
        cin>>division;
    }
    void display() {
        cout<<"\n"<<"DETAILS:"<<"\n"<<name<<"  "<<roll_no<<"  "<<dept<<"  "<<division<<"\n";
    }
};
int main() 
{
    Data d1;
    d1.display();
} 
```
## Output:
![Output12A](https://github.com/user-attachments/assets/92fb077e-ac69-4cd3-a23f-d0914f06b918)


## Code: 12B
```
// NAME - AKALP SARKAR
// PRN - 23070123116
// EXPERIMENT - 12(B)

#include<iostream>
using namespace std;
class Num
{
    public:
    Num(int c, int d)
    {
        if(c>d)
        {
            cout<<c<<" is greater.";
        }
        else 
        {
            cout<<d<<" is greater.";
        }
    }
};
int main()
{
    Num n1(4,3);
} 
```

## Output:
![Output12B](https://github.com/user-attachments/assets/666fed4e-341f-45fc-9941-f8ec48bbfcc3)

## Code:12C
```
// NAME -AKALP SARKAR
// PRN - 23070123116
// EXPERIMENT - 12(C) 

#include<iostream>
using namespace std;
int count=0;
class destruct{
    public:
    destruct()
    {
        count++;
        cout<<"Number of objects created: "<<count<<"\n";
    }
    ~destruct()
    {
        count--;
        cout<<"Number of objects destroyed: "<<count<<"\n";
    }
};
int main()
{
    destruct aa,bb,cc;
    {
        destruct dd;
    }
    return 0;
}
```
## Output:
![Output12C](https://github.com/user-attachments/assets/9499d1da-1976-4e86-91a8-c99383123583)

### Conclusion:
I learnt about constuctors and its types, destructors and performed various programs based on that.
