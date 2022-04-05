- [1. Basics of Programming](#1-basics-of-programming)
  - [1.1. Introduction](#11-introduction)
    - [1.1.1. What is programming?](#111-what-is-programming)
    - [1.1.2. What are types of programming](#112-what-are-types-of-programming)
  - [1.2. Terminology](#12-terminology)
    - [1.2.1. Documentation](#121-documentation)
    - [1.2.2. Library](#122-library)
    - [1.2.3. Comment](#123-comment)
    - [1.2.4. Data](#124-data)
    - [1.2.5. Whitespace](#125-whitespace)
    - [1.2.6. Variable](#126-variable)
    - [1.2.7. Constant](#127-constant)
    - [1.2.8. Type](#128-type)
    - [1.2.9. Functions](#129-functions)
    - [1.2.10. Argument](#1210-argument)
    - [1.2.11. Operators](#1211-operators)
    - [1.2.12. Arrays](#1212-arrays)
    - [1.2.13. Object](#1213-object)
    - [1.2.14. Class](#1214-class)
    - [1.2.15. Recursion](#1215-recursion)
    - [1.2.16. Algorithm](#1216-algorithm)
    - [1.2.17. Conditionals](#1217-conditionals)
    - [1.2.18. Loops](#1218-loops)
    - [1.2.19. IDE](#1219-ide)

# 1. Basics of Programming
This guide will teach you basics of programming.

## 1.1. Introduction

### 1.1.1. What is programming?

Programming is developing instructions for a computer to perform a particular task / program.

### 1.1.2. What are types of programming

This bifurcation depends on what basis you want to bifurcate them.

Differentiating them on the basis of problem solving approach,

- Functional Programming
  - In this approach, everything is like a mathematical function. The output of a function purely relies on the arguments passed to it and does not depend up on anything preceding the function. This relies on conditional recursion to reach the result.
  - The output of a function is always the same, given the same exact arguments to the function.
  - Parallel execution is fully supported since data is immutable.
  - Order of execution of statements does not matter.
  - Recursion is used for iteration.
- Object Oriented Programming (OOP)
  - In this approach, everything is represented as an object with methods and attributes to do everything.
  - Parallel execution is not supported since data is mutable.
  - Order of execution of statement matters.
  - Loops are used for iteration.
- Procedural Programming
  - In this approach, step by step instructions are provided. This relies on iteration, i.e. Repeating steps a certain number of times to achieve the end result.
  - In this approach, everything is represented as a simple series of steps.
  - Order of execution of statement matters.
  - Repetition is used for iteration.
## 1.2. Terminology

### 1.2.1. Documentation
Shortly and commonly known as docs, these are text that describe the program. These are mostly written by the Developers as a manual user. Most libraries and languages have docs which are the official source of information about the library.

### 1.2.2. Library

A library is a program someone else wrote, which allows us to import that program into our program, basically giving our program "super powers".

### 1.2.3. Comment

Comments are ignored by compiler. They are typically used to put instructions about the program, description about various parts of program, document about the program, meta information about the program, etc.

They are also used to temporarily stop specific lines of program from running.

### 1.2.4. Data
Not to be confused with information, Data is useful part of information.

### 1.2.5. Whitespace

Whitespaces are any characters that you can type but cannot see.

These are:
spaces, tabs and new-lines
In most programming languages these are represented as follows

| Whitespace | Representation |
| :--------: | :------------: |
|   space    | *empty space*  |
|    tab     |       \t       |
|  new line  |       \n       |

### 1.2.6. Variable

A variable is used to store data inside a program. The value of a variable is the data it has stored and the identifier or the name is how the program and the programmer recognizes it. The value of a variable can be changed by the programmer using his program, unless this variable is declared as a constant variable (explained next chapter).

The identifier or name of a variable does not change inside a program.

### 1.2.7. Constant

A constant is just like a variable except that it's value cannot be changed.

### 1.2.8. Type

Type or Data Type is how we can bifurcate different data. Like number and character are different types because they are different.

There are different types in different languages, like C has float and int as different types whereas in javascript these are simple numbers, in C we have characters and string distinctly, but in javascript we have simply strings.

Typical Basic Data Types:
|   Type    |                    Description                     |           Examples           |
| :-------: | :------------------------------------------------: | :--------------------------: |
|  Number   |               A numerical data type                |        6, 9, 1.2, -2         |
|  String   |                A set of characters                 | "Hello", "6 boxes", "9", "*" |
|  Boolean  |                Either true or false                |      true, false, 0, 1       
|
| undefined |           Anything that hasn't been given a value  |          undefined           
|
|   null    |            As the name says, a null value.         |             null             

Some languages use null as a replacement to undefined, But I did not mention that this is the case for all programming languages and was just a general representation of data types.


### 1.2.9. Functions

Functions are reusable pieces of code. They are used to modularize the program / perform a specific task.

These can have arguments (aka parameters) that can be passed to these from where they are being called.

When we call a function it evaluates.

A function may or may not return some data.
For example - a function that recieves 2 parameters as arguments and returns the average: a function that returns a value.

Function that does not return a value:
a function that recieves 2 parameters as arguments and displays the average somewhere - but does NOT return any value. 

### 1.2.10. Argument

This is the information passed to a function, It is also known as parameter.

### 1.2.11. Operators

Operators perform operations on variables.
List of operators:
|   Operator       |                    Description                     |           Examples           |
| :-------:        | :------------------------------------------------:     | :--------------------------: |
|     +            |               Operation for addition                   |         1+2, 3+5
|
|     -            |            Operation for subtraction                   | 3 - 2, 6 - 1, 5 - 3 
|
|     %            |returns the remainder or signed remainder of a division | 6 % 3 = 0, 5 % 2 = 1, 18% 4 = 2 
|
|     /            |           Operator for division                        | 6 / 6 = 1, 4 / 2 =  2    
|
|   null           |            As the name says, a null value.             |             null  


### 1.2.12. Arrays

These are collection of data having the same data type.

A list is generally a collection of data independent of their data type.

Depending on language you can also store many different data types into an array.

A language may also call an array as a list and vice-versa.

### 1.2.13. Object
An object (aka Dictionary or dict) is a key-value pair of data.

### 1.2.14. Class

A class is like an advanced object. It has methods (functions) and attributes (values).

It's attribute denotes it's state and it's method denotes it's behavior.

### 1.2.15. Recursion

When a function calls itself it's called a recursion, We may use conditional recursion to simplify the way we solve a specific problem.

### 1.2.16. Algorithm

A specific set of steps to solve a particular problem

### 1.2.17. Conditionals

These are types of statements that, on evaluation, give a boolean value.

### 1.2.18. Loops
Loops run a specific set of statements as long as a given conditional statement is true.

### 1.2.19. IDE

Integrated Development Environments are softwares used to make programming simpler. It involves many features such as Syntax Highlighting, Compiler Integration, Language Server, Debugger, Autocompletion.
