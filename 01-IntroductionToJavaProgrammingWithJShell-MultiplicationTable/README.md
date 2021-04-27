## Learning Programming
- Problem Solving Skills
- Concepts
- Language Specifics

## JShell

- Java REPL Read Eval Print Loop
- Type in one line of code (or multiple) and see output
- Makes learning Fun
- Introduced in Java 9

## Concepts
- JShell
- Statements
- Expressions
- Variables
- Literals
- If Statement
- For Loop
- Method/Function

## Naming a Variable/Method
- Combination of letters, numbers, $ and under-score(_)
- Cannot start with a number
- Cannot be a keyword
- No limit on length of identifier
- CamelCase

## Variables Types
- byte  b = 5;             //8  bits - 128 to 127
- short   s = 128;         //16 bits - 32,768 to 32,767 
- int     i = 40000;      //32 bits -  2,147,483,648 to 2,147,483,647
- long  l = 222222222; //64 bits -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807
- float   f = 4.0f;          //32 bits NOT VERY PRECISE - don’t use for financials
- double  d = 67.0; //64 bits NOT VERY PRECISE - don’t use for financials
- char  c = 'A';             //16 bits '\u0000' to '\uffff'
- boolean isTrue = false;  //true or false

## Launch JShell

JShell
- [x] Java REPL Read Eval Print Loop
- [x] Type in one line of code (or multiple) and see output
- [x] Makes learning Fun
- [x] Introduced in Java 9

## First Challenge

Our first challenge is to get the computer to print a multiplication table for us. 

```
5 * 1 = 5
5 * 2 = 10
5 * 3 = 15
5 * 4 = 20
5 * 5 = 25
5 * 6 = 30
5 * 7 = 35
5 * 8 = 40
5 * 9 = 45
5 * 10 = 50
```

## Launching JShell

Launch JShell

/exit to exit

Relaunch

## Multiplication Table - Step By Step
- [x] How to break it down?
- [x] Where do we start?
- [x] Calculate 5 * 5
- [x] Print 5 * 5 = 25
- [ ] Do this 10 Times

## First Java Expressions

Let's get the computer to do a few calculations for us to get started.

> 10 + 5
15

> 10 * 5
50

> 10 - 5
5

> 10 - 5 * 2 //Think about this!



Terminology - operand, operator, literal
Numeric Operators -> + - / * /
What we are using are expressions to perform operations on numbers. +, *, - are operators.  
The numbers are called Literals.

A few puzzles
- 1 + 2 //Notice the spaces - Programming Languages do not worry about spaces - for the most part!
- 1+2//No spaces
- 5/2
- 5*2 + 2

###### Exercise
- Write an expression to calculate number of minutes in a day.
- Write an expression to calculate number of seconds in a day.

## More Operators and Precedence
- 1 + 5 * 2
- 5 % 2
- 5 / 2


## Printing output
```
System.out.println("Welcome to Programming World");
```

### Method Call
- This is a method call. We are calling a method. The syntax to call a method is method_name(value)
- In this example
	- method_name is System.out.println
	- value we want to print is "Welcome to Programming World"
- System.out.println is an inbuilt method provide by Java. It prints the value passed to it to the console i.e. the screen in JShell!

### Double Quotes
Any thing in double quote is considered as text. This is called a String Literal.

> System.out.println(Welcome to Programming World) != System.out.println("Welcome to Programming World")

Puzzles
- Different Case - System.out.println("welcome to programming world")

###### Exercise
- Print "Hello World"
- Print "5 * 3"

## Text vs Expression

> System.out.println("5 * 6");//Doesn't work

> System.out.println(5 * 6);//30

## More advanced prints

I want to print 5 table in this format 
5 * 1 = 5

We have to write - System.out.println("5 * 1 = 5")

This is not fun. Computer is not calculating it for us! How to get it to calculate and print the value for us?

We will use a new function printf.

- System.out.print("5 * 1 = 5") //No new line
- System.out.println("5 * 1 = 5") //With new line
- System.out.printf("%d * %d = %d", 5, 1, 5 * 1).println() //Avoids all complication around it


## Variables

Our end objective is to print the complete 5 tables. We need to execute 10 statements to get this done right now.

System.out.printf("%d * %d = %d", 5 , 1 , 5 * 1 ).println();
...
System.out.printf("%d * %d = %d", 5 , 6 , 5 * 6 ).println();
...
...
System.out.printf("%d * %d = %d", 5 , 7 , 5 * 7 ).println();

5, 6, 7 are constants (literals). Their values will not change. 

Variables are those things whose values can change during the execution of a program!

Variables have a name, type and value.

Name gives us a way to refer to the variable.

Java is a Strongly Typed Language. That means, you need to tell Java what kind of values you want to store in the variable.

There are two types of literals we looked at until now
- Strings - "Welcome to Programming"
- Numbers - Specifically integers - 5 , 6, 7

Before creating a variable, I need to tell Java what kind of values a variable will store. For now, lets now create a number variable.

> int i = 0; // declaration and initialization

> i = 6; // assignment.

System.out.printf("%d * %d = %d", 5 , 6 , 5 * 6 ).println();

## Basic If Condition

- int team1Goals = 5;
- int team2Goals = 7;

Let's try and write a few conditions.

jshell> team1Goals > team2Goals
$47 ==> false

jshell> team1Goals < team2Goals
$48 ==> true

Let's try to conditionally execute statements.

jshell> if(true)
   ...>  System.out.println("Test");
Test

jshell> if(false)
   ...>  System.out.println("Test");

jshell> if(team1Goals > team2Goals) 
   ...> System.out.println("Team 1 wins");

jshell> if(team2Goals > team1Goals) 
   ...> System.out.println("Team 2 wins");
Team 2 wins

Let's now to print which number is greater

jshell> int number1 = 6;
number1 ==> 6

jshell> int number2 = 7;
number2 ==> 7

jshell> if(number1 > number2)
   ...>   System.out.println("Number1 is greater than number2");

jshell> if(number1 >= number2)
   ...>   System.out.println("Number1 is greater than number2");

jshell> if(number2 > number1)
   ...>   System.out.println("Number2 is greater than number1");
Number2 is greater than number1

jshell> if(number2 >= number1)
   ...>   System.out.println("Number2 is greater than number1");
Number2 is greater than number1

## For Loop - Printing 5 Table from 1 to 10

We currently have this...

```java
int i = 0;

i = 1;
System.out.printf("%d * %d = %d", 5 , i , 5 * i ).println();

i = 2;
System.out.printf("%d * %d = %d", 5 , i , 5 * i ).println();

i = 3;
System.out.printf("%d * %d = %d", 5 , i , 5 * i ).println();

i = 4;
System.out.printf("%d * %d = %d", 5 , i , 5 * i ).println();
```

Can we do better?

````java
int i = 0;
i = i + 1;
System.out.printf("%d * %d = %d", 5 , i , 5 * i ).println();

i = i + 1;
System.out.printf("%d * %d = %d", 5 , i , 5 * i ).println();

i = i + 1;
System.out.printf("%d * %d = %d", 5 , i , 5 * i ).println();

i = i + 1;
System.out.printf("%d * %d = %d", 5 , i , 5 * i ).println();
````

Syntax of a for loop is 

for(initialization;condition;update)
	statement;

For Loop Example 1
```java
for (int i = 0; i < 10; i++) {
    System.out.print(i);
}
//Output - 0123456789
```

Now we want to print our 5 table

```
5 * 1 = 5
5 * 2 = 10
5 * 3 = 15
5 * 4 = 20
5 * 5 = 25
5 * 6 = 30
5 * 7 = 35
5 * 8 = 40
5 * 9 = 45
5 * 10 = 50
```
