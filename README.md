# C++ Programming Language

## Naming Requirements and Naming Conventions
C++ uses these valid characters for naming variables: 
1. uppercase letters
2. lowercase letters
3. digits
4. underscores

Variable names can't be the same as C++ reserved keywords and C++ enforces case sensitivity, meaning that 'myVar' and 'myvar' would be treated as different variables.

## Statically or Dynamically typed?
C++ is a statically typed language. Variable types are determined at compile time, which means that variables must explicitly be declared when being defined. Mismatch errors will be caught by the compiler, which helps ensure type safety and better execution in C++ programs.

## Strongly or Weakly typed?
C++ is a strongly typed language. Data type declaration for variables must be declared initially and followed throughout the program’s execution. 

The compiler will ensure that each variable is assigned the correct data type and is checked so that there are no possible data type mismatches. 

## Explicitly or Implicitly typed?
Implicitly typed is completed by the computer, the compiler automatically convers one data type to another based on predefined rules of the online C++ compiler. Explicitly typed is done manually by the programmer in which the programmer is allowed to change the data type variable to another type (typecasting). C++ cannot implicitly convert types thus all C++ constructors should be explicit. 

## Mutable vs Immutable Variables
All variables in C++ are mutable by default. This can be changed by the “const” modifier, which makes a variable immutable in a function. 

## Operators for Each Data Type
Arithmetic operators | Increment(++), Decrement(--)

Binary Operators | Addition(+), Subtraction(-), Multiplication(*), Division(/), Modulo Operation(%)

Relational Operators | Is equal to(==), Greater than(>), Greater than or equal to(>=), Less than(<), Less than or equal to(<=), Not equal to(!=).

Logical Operators | Logical AND(&&), Logical OR(||), Logical NOT(!)

Bitwise Operators | Binary AND(&), Binary OR(|), Binary XOR(^), Left shift(<<), Right shift(>>), One’s complement(~)

Assignment Operators | Assignment Operator(=), Add and Assignment Operator(+=), Subtract and Assignment Operator(-=), Multiply and Assignment Operator(*=), Divide and Assignment Operator(/=)

Ternary or Conditional Operators | Expression1? Expression2: Expression3
This operator determines the answer based on the expression given.

## Mixed Type Operations
Mixed typer operations are allowed, but the behavior of these operations is determined by implicit type conversion. Often when you mix types, the compiler will promote operands. 
(ex: if you mix int and double, int will be promoted to a ‘double’)

## Binding Identifiers, Operators, Functions, and Variables
Identifier names are bound during declaration phase at compile time.
 
Functions and global variables are bound to their addresses when it comes to the linking phase as part of the compilation process. 

Operators are bound at compile time based on the type of operand.

```
#include <iostream>


int main(){
    //will not run because x is not defined and “5” can’t be converted from a chat to an int
    x = “5” + 6;
    //int x = 5 + 6;
    std :: cout << x ;
    return 0;
}

```
## Limitations 
When adding ints and floats:
- There is a chance that values may have precision loss where there may be rounding errors.
- There is also the possibility of promotions (ex: if you mix int and double, int will be promoted to a ‘double’)
  
When storing different types in lists: 
- We use C++ containers like ‘std::list’ or ‘std::vector’ to store elements of the same type.
  
When converting between data types: 
- One should be aware that C++ allows certain implicit type conversions but this can lead to loss of data, so one should be explicit when necessary to avoid any unnecessary data loss.

Other restrictions to be aware of: 
- C++ allows manual memory management using pointers but this is prone to memory leaks or undefined behavior if not used correctly. 
- Attempting to access elements beyond the bounds of an array or vector can lead to undefined behavior. 
- Compatibility with compilers may differ, keep in mind that there are compiler-specific behaviors and standard that may change how code behaves based on different compilers. 

***
## Loops in C++
While Loop
- While loops continue as long as the specified condition is true. Initialization and update steps are coded outside of the loop
```
int i = 0;
while (i < 5){
++i;
}

```
For Loop
- For loops will continue to execute as long as the condition is true.
```
for (int i = 0; i < 5; ++i) {
   	 // Code to be executed in each iteration
}

```
do-while loop
- The do-while loop is similar to the while loop but it makes sure that the loop body is executed at least once before checking the loop condition
```
do{
//insert the code that you desire to be executed for each iteration
//update the condition
} while(condition);

```
