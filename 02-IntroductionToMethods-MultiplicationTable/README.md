# Breaking up Code into Methods

## Method Basics

- Print 5 Table
- Print 6 Table

> Isn't this too much work? Can we do this in an easier way?

- printMultiplicationTable(5);
- printMultiplicationTable(6);

Basic Syntax 

ReturnType nameOfTheMethod() {
  //Body of the method
  //What do we want to do in the method?
}

- Method
   - Piece of code
   - Has a name!
   - Can have inputs
   - Can have output called return value

```java
void sayHelloWorldTwice() {
     System.out.println("Hello World");
     System.out.println("Hello World");
 }
```

## Method Arguments

Why do we need to create two different methods for sayHelloWorldTwice() and sayHelloWorldThrice()?  What if I need to sayHelloWorldFourTimes()?

sayHelloWorld(5), sayHelloWorld(2)

````java
ReturnType nameOfTheMethod(Type argumentName) {
  //Body of the method
  //What do we want to do in the method?
}

Notes
- Type argumentName - int numberOfTimes

void sayHelloWorld(int numberOfTimes) {
  System.out.println("Hello World");
}

void sayHelloWorld(int numberOfTimes) {
  System.out.println("Hello World");
  System.out.println(numberOfTimes);
}

void sayHelloWorld(int numberOfTimes) {
  for(int i=1; i<=numberOfTimes; i++)
    System.out.println("Hello World");
}
````

Exercises 
 - Create a method - printNumbers(int n) to print numbers from 1 to n!
 - Create a method - printSquaresOfNumbers(int n) to print squares of numbers from 1 to n!

## Getting back to the problem at hand

```java
void printMultiplicationTable() {
    for(int i = 1;i <= 10;i++)
       System.out.printf("%d * %d = %d", 5 , i , 5 * i ).println();
}

void printMultiplicationTable(int number) {
    for(int i = 1;i <= 10;i++)
      System.out.printf("%d * %d = %d", number , i , number * i ).println();
}
```

## Method - Multiple & Return Parameters

Exercise:
- Method to return sum of two numbers

# Introduction to Java Platform

Before JShell, you cannot execute a statement directly. You had to write a class -> compile it -> execute it.

## Introduction to Class and Objects

Before we can compile Java code, we need a class. 
- Class is a Template ex: Country
- Objects are instances of classes ex: India, USA

In Java, all methods must be in a class. 
- Methods in JShell work a little different

class Planet {
}

Planet earth = new Planet();
Planet venus = new Planet();

## Create a Method in a Class

class Planet {
            void revolve() {
                 System.out.println("Revolve");
            }
       }

- Create a class Country with a member method comingSoon() printing "Coming Soon!" to the console.

class Country {
          void comingSoon() {
             System.out.println("Coming Soon");
          }
       }
