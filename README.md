# C++ Programming Language
Author: Kimberly Silva-Lopez

## History
Bjarne Stroustrup created the object-oriented programming language C++ in 1979 at Bell Laboratories as an addition to the C language. Stroustrup started working on C++ in 1982 as a replacement for C with Classes. It had additional features, including operator overloading, references, constants, virtual functions, and function names. The main applications for the programming language C++ include system programming, game development, and application software development

## C++ Installation 
### IDE Installation
The programming IDE I have chosen to install C++ on is Virtual Studio Code. To download, click [here](https://code.visualstudio.com/download)

### Setting Up C++ In Visual Studio Code on Windows 11
1. We first need to download the MinGW C++ compiler for Windows 11. Here is an [installation link.](https://techdecodetutorials.com/downloads/mingw.exe)
2. Open your downloads folder and double-click to begin the installation process
3. Choose the extraction location of the C++ compiler by typing "C:\\" and click extract.
4. Now we have to set up our environment variables:
   - Copy the location of the bin folder from the MinGW directory, it should say "C:\MinGw\bin".
   - In your Windows search bar, type 'Environment Variables' and press enter.
   - Click on the 'Environment Variables' button
   - Select 'Path' variable and click 'edit'
   - Click 'New' and paste: C:\MinGw\bin
   - Press 'OK'
5. Now we have to verify if the compiler is working:
   - Open a Windows Command Prompt
   - In the command prompt, type 'g++ --version' and press enter to see the version of MinGW g++.
6. Install C++ extensions in VS Code
   - Open up Visual Studio Code, click on the extensions button on the side bar, type C++ and select the first option from Microsoft, and install.
   - Now search 'Code Runner' in the extensions search bar and install the option from Jun Han

## Hello, World! 
Create a new file in Visual Studio Code and save it as HelloWorld.cpp
Type this code into your file.
```
#include<iostream>
int main() {
    cout << "Hello World!";
    return 0;
}
//this is your first C++ program, use '//' for single line comments
/*use this syntax to comment
multiple line comments*/
```
To run your program, press: Ctrl + Alt + N

## Naming Requirements and Naming Conventions
Common naming conventions: 
- Camel Case
- Snake Case
- Underscores

C++ uses these valid characters for naming variables: 
- uppercase letters
- lowercase letters
- digits
- underscores

Case Sensitivity: 
- ‘myVar’ and ‘myvar’ would be treated as different variables

Keywords: 
- Variable names can’t be the same as C++ reserved keywords

Naming conventions are not enforced by the compiler more so, they are defined by community standards. Compilers can give warnings if a variable isn’t yet initialized, but that is not related to naming convention. 

Although naming conventions is not enforced, it is good practice to follow established conventions for consistency and readability. 

## Keywords
This is also known as reserved words, there is a total count of 95 reserved words. They’re always written in short lowercase letters. (for example, void, int, public, etc.)

| asm  | double | new  | switch |
| ------------- | ------------- | ------------- | ------------- |
| auto  | else  | operator  | template  |
| break  | enum  | private  | this  |
| case  | extern  | protected  | throw  |
| catch  | float  | public  | try  |
| char  | for  | register  | typedef  |
| class  | friend  | return  | union  |
| const  | goto  | short  | unsigned  |
| continue  | if  | signed  | virtual  |
| default  | inline  | sizeof  | void  |
| delete  | int  | static  | volatile  |
| do  | long  | struct  | while  |

## Variable Declaration For Common Data Types
```
#include <string>
#include <iostream>
#include <list>
#include <map>
using namespace std;

int main(){
    //int
    int x = 5;

    //string
    string testString = "This is a string.";
    cout << testString << endl;

    //floating-point number
    float number = 2.5;
    cout << "The floating number value is: " << number << endl;

    //boolean
    //note: the numeric value of true is 1 and the numeric value of false is 0 
    int x1 = 2, x2 = 4;
    bool num1, num2;
    num1 = x1 == x2;
    num2 = x1 < x2;

    cout << "Bool num1 is: " << num1 << endl;
    cout << "Bool num2 is: " << num2 << endl;

    //arrays
    //to declare an array you must specify the data type and the size of the array
    //arrays are zero-indexed, meaning the first element will use index 0, and then we increment by 1
    int array[2];
    array[0] = 5;
    int arrayNum = array[0];
    cout << "Our array value is: " << arrayNum << endl;

    //lists
    //lists are part of the C++ library, you can utilize this by adding '#include <list>' in the header
    list<int> nameList{1,2,3,4,5};
    for (auto i: nameList) {
        cout << i << ' ';
    }

    //dictionary
    //'maps' work just like dictionaries, they work like a container that stores values which have a unique key.
    //Each value within this container has a special key.
    //to use maps, you must add '#include <map>' in your header.
    
    //creating a map
    map<string, int> mapExample;
    mapExample["One"] = 1;
    mapExample["Two"] = 2;
    mapExample["Three"] = 3;

    //examples and further information: https://favtutor.com/blogs/cpp-dictionary
    return 0;
}
```

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
### While Loop
- While loops continue as long as the specified condition is true. Initialization and update steps are coded outside of the loop
```
int i = 0;
while (i < 5){
++i;
}

```
Here is an example of a while loop that will print out "Hello World!"
```
#include <iostream>

int main(){
    //we initialize our expression
    int x = 1;
    //create our while loop and test the expression
    while (x < 5) {
        cout << "Hello World!\n";
        x++;

    }
    return x;
}
```

### For Loop
- For loops will continue to execute as long as the condition is true.
```
for (int i = 0; i < 5; ++i) {
   	 // Code to be executed in each iteration
}

```

Here is an example of a for loop that will repeat a condition
```
#include <iostream>

int main(){
    int x;
    //blank expression so that it runs as an infinite loop
    for (;;){
        cout << "Hello World Forever!\n";
    }
}
```

### do-while loop
- The do-while loop is similar to the while loop but it makes sure that the loop body is executed at least once before checking the loop condition
```
do{
//insert the code that you desire to be executed for each iteration
//update the condition
} while(condition);

```
Here is an example of a do-while loop that will print out "Hello World!"
```
#include <iostream>

int main() {
    //initialize our expressions
    int x = 1;
    do{
        cout << "Hello World!\n";
        x++;
    //as long as x is less than 5, we will see that the output is "Hello World" x 4
    } while (x < 5);

    return 0;
}
```


## Syntax for Declaring Functions
Function declaration tells the compiler about a group of statements within a function. It tell the compiler the function name, what it returns, and any parameters that are within that function. 

The general syntax would look like this:
```
return_type function_name(parameters){
	body of the function
}
```
## Function Placement Rules
There are no rules in C++ about function placement. C++ allows a function to be placed anywhere in the code file and the order in which these functions appear won’t necessarily determine how each function is executed. Although it’s important to define a function before they are called so that you don’t receive any compiler warnings and the compiler knows about the functions before executing them. 

### Function that multiplies two values
```
int multiply(int a, int b){
    return a * b;
}

int main(){
    int a, b, total;
    cout << "Enter two numbers: ";
    //stores num1 and num2
    cin >> a >> b;
    //multiplication process and stores the result in total
    total = multiply(a,b);
    cout << "Total: " << total;
    return 0;
}
```

## Recursive Functions
C++ does support recursive functions. A recursive function is a function that calls itself repeatedly until a certain condition is met.

```
int factorial(int n){
    //base case: factorial of 0 is 1
    if (n ==0 || n ==1) {
        return 1;
    } else {
        return n * factorial(n - 1); 
    }
}

int main(){
    int num = 5; 
    cout << "Factorial of " << num << " is: " << factorial(num) << endl;
    return 0;
}
```

## Multiple Parameters and Data Types
Functions in C++ can accept multiple parameters. You can define parameters as char, int, double, or other data types. Because you can declare each parameter independently, you don’t necessarily need to use the same data type for all but they must be specified.

The general syntax for this would:
```
return_type function_name (type1 parameter1, type2 parameter2…){
	//function body
}
```
## Returning Multiple Values
C++ does not directly allow us to return multiple values at the same time but programing allows us to do so by using pointers, using structures, and using arrays. 

Pointers
- Using pointers, we pass the argument with their address and make changes to their values by using pointers so that the values are changed.

Structures
- Using structures, it is a user-defined datatype that will use two integer values and store the greater and smaller values into those variables and then use them. 

Arrays
- Using arrays only works when returned values are of the same type. When an array is passed as an argument, the base address is passed to the function and any changes made to the copy of the array, it’ll change the value of the original array.

## Pass-By-Reference? Pass-By-Value?
C++ supports pass-by-reference and pass-by-value. 

**Pass by reference**

References in C++ is used when you pass a variable by reference in a function to the original variable and any changes that are being made to the parameter that’s inside the function will directly change the original variable value.

**Pass by value**

The function receives a copy of the variable when a variable is passed to a function in C++. Any changes that are made to the parameter inside of the function will not change the original value outside of the function.

Here we have a function that tests a pass-by-value and pass-by-reference function
```
#include <iostream>

//create our pass-by-value function
void passByVal(int x){
    //using this function will mean that the changes inside the function won't affect the original value
    x = 10;
}

void passByRef(int &y){
    //changes within the function will directly affect the original value 
    y = 20;
}

int main(){
    int val1 = 2;
    int val2 = 4;
    //call your functions
    cout << "Value before passByVal: " << val1 << endl;
    passByVal(val1);
    cout << "Value after passByVal: " << val1 << endl;
    
    cout << "Value before passByRef: " << val2 << endl;
    passByRef(val2);
    cout << "Value after passByRef: " << val2 << endl;

    return 0;
}
```

## Storing Arguments, Parameters, and Local Variables
Arguments

Arguments are passed to a function and stored by value or by reference. By value they are copied into the functions parameters space on the stack. By reference the address of the variable is passed which allows the function to access the original data of the variable.
```
void exampleFunction(int arg) {
    // 'arg' is a copy of the original value
}
```
```
void exampleFunctionByReference(int& arg) {
    // 'arg' is a reference to the original value
}
```
Parameters

Parameters are stored on a stack. Once a function is called, the values of the arguments are passed to the function and space is allocated for the parameters on the stack.
```
void function(int parameter){
	//parameter is now stored on the stack
}
```

Local Variables

Local variables are stored on a stack. Once a function is called, space can be allocated for local variables, these are declared within the function body.
```
void function(){
	Int localVar; //localVar is stores on the stack
}
```
Dynamically Allocated Variable

Variables that are created with dynamic memory allocation using ‘new’ or ‘malloc’ will be stored in the heap. 
```
int* dynamicAllocVar = new int; //stored in heap
```
## Scoping Rules

The scoping rules in C++ determines the extent of a program code and which variables can be accessed, declared, or worked with. 

Local Scope

These are variables declared within a code block that have a local scope and are only visible within that specific block.
```
void exampleFunction() {
    int localVar; // Local variable
    // ...
} // localVar's lifetime ends here
```

Function Scope

Variables with a function scope are visible throughout the entire function.

Glocal Scope

These are variables that are declared outside of a function or class are within the Global Scope. They’re visible throughout the entire program and their lifetime ends at the end of the program. 

Block Scope

Variables that were declared in a loop or conditional block fall within the Block Scope. With each iteration of a loop, a new scope for the variable is created within the loop body and their lifetime ends once the loop has finished executing. 

## Side Effects in C++
Side effects is when there is an observable behavior of a function or expression other than its return value, such as taking input or generating a different output or changing the value of variables. Side effects are possible in C++ and there aren’t inherent guard rails against them, because C++ allows functional and imperative programming styles, there’s a flexibility in designing functions or operations that can ultimately lead to side effects in the program.

Some methods to lessen the chance of side effects:
- Create pure functions that only depend on its input parameters and will produce an output that doesn’t modify the external state.
- Immutability by avoiding modifying variables when possible.
- Local Scoping by limiting the scope of variables to minimize their visibility. It’s also encouraged that users use local variables whenever appropriate.
- Minimize the use of Global variables so that variables can’t be modified by multiple functions.

## Boolean Values

A boolean value represents a truth value such as true or false, these variables are a special type of memory that is stored in a computer only as true or false. C++ uses the ‘bool’ data type that represents two possible values: ‘true’(1) and ‘false’(0):
```
bool isTrue = true;
cout << isTrue; //will output true(1)
bool isFalse = false;
cout << isFalse; //will out false(0)
```

## Conditional Statements

C++ uses ‘if’ statements:
```
if (condition){
	//code that is execute if the condition is true 
}
```
Here is an example of a one-condition 'if' statement 
```
#include <iostream>

int main(){
    //declares an integer variable
    int num;
    //asks user input for an integer
    cout << "Enter an integer: ";
    cin >> num;
    //if/else condition, as long as the number inputted is divisible by 2, it is an even number
    if (num % 2 == 0){
        cout << num << " is even" << endl;
    } else{
        cout << num << " is odd" << endl;
    }

    return 0;
}
```

C++ has else statements that can be executed if the condition is false:
```
if (condition){
	//code that is executed if the condition is true
} else {
	//code that is executed if the condition is false
}
```
Here is an example of a multi-condition if/else statement
```
#include <iostream>

int main(){
    int x, y;
    cout << "Enter a value for x: " << endl;
    cin >> x;

    cout << "Enter a value for y: " << endl;
    cin >> y;

    //our multi condition if/else statement
    if(x > 0 && y < 5){
        cout << "Both conditions are met, x is greater than 0 and y is less than 5." << endl;
    }else{
        cout << "At least one condition is false." << endl;
    }
    return 0;
}
```

C++ also uses the else if statement:
```
if (condition1){
	//code that is executed if the condition is true
} else if (condition2) {
	//code that is executed if condition1 is false and condition2 is true
} else{
 	// code that is executed if neither condition1 and condition2 is true
}
```
Here is an example of an if/elif/else statement
```
#include <iostream>

int main(){
    int num;
    cout << "Enter a number: ";
    cin >> num;

    if (num > 0){
        cout << "This number is a positive number." << endl;
    }else if(num < 0){
        cout << "This number is negative." << endl;
    } else{
        cout << "This number is 0." << endl;
    }
    return 0;
    
}
```

C++ also uses switch statements that perform multi-way branching based on the value of the expression:
```
switch (expression){
	case value1:	
		//code executed if expression == value1
		break;
	case value2:
		//code executed if expression ==value2
		break;
	default: 
		//code executed if none of the expressions match the case
}
```
Here is a calculator program that uses switch case statements
```
#include <iostream>

int main(){
    int x, y;
    char oper;
    cout << "What operator would you like (+, -, *, /): " << endl;
    cin >> oper;

    cout << "Enter a number for x: " << endl;
    cin >> x;
    cout << "Enter a number for y: " << endl;
    cin >> y; 

    switch (oper){
        case '+':
            cout << x << " + " << y << " = " << x + y;
            break;
        case '-':
            cout << x << " - " << y << " = " << x - y;
            break;
        case '*':
            cout << x << " * " << y << " = " << x * y;
            break;
        case '/':
            cout << x << " / " << y << " = " << x / y;
            break;
    }
    return 0;
}
```
## How Does C++ Delimit Code Blocks

C++ uses curly braces {} to code block under each condition, typically each condition will be encased within the curly braces but switch statements will have every case within that one curly brace.

## Short Circuit Evaluation

Short-circuit evaluation is a behavior in which the second part of a logical expression is not evaluated if the result of the logical expression can be determined by the first part. Short circuiting in C++ occurs when a logical expression evaluates ‘&&’ (AND) and ‘||’ (OR) logical operators.
```
#include <iostream>

int main(){
    int x = 5;
    int y = 10;
    //short-circuit logic statement with '&&' operators
    if (x > 0 && y/ x > 2){
        cout << "Both conditions are true." << endl;
    } else{
        cout << "At least one condition is false." << endl;
    }
    return 0;
}
```

## The 'Dangling Else' Problem
The “dangling else” problem is a potential ambiguity in programming that uses multiple ‘if’-’else’ statements. It’s when a programmer loses track of code indentation and makes it unclear where an else part matches with the if statement
C++ deals with this problem by using a rule called the “matching ‘else’ rule” in which it specifies that an ‘else’ code block will be associated with the closest proceeding unmatched ‘if’ statement.
 The use of curly braces is highly encouraged to avoid indicate what ‘else’ belongs to which ‘if’ and avoid confusion.

## Switch/Case Statements

C++ uses ‘break’ to exit a switch statement after a case has been evaluated and executed. Without the use of the ‘break’ statement, this will allow the control to flow through the other cases within the program which can cause confusion. The statement ‘continue’ is not applicable for ‘switch’ statements because the ‘continue’ statement is used in loops(‘for’ and ‘while’ loops) to skip the rest of the loop body and continue on to the next iteration.

## Loop Code Block Variables vs Function Code Blocks

Variables that are declared within loops and functions both have block scope which means their visibility is limited to the block in which they were declared. They are the same in order to keep variables within their own scopes so to avoid compilation errors. 

## Objects

C++ is an object-oriented programming language. Objects are instances of classes or structs and they’re used to model and manipulate data and perform operations. 

The ‘class’ keyword is used to define a class with variables and member functions. You can also use the ‘struct’ keyword which, similarly to ‘class’, has a public member variable by default. The difference between ‘class’ and ‘struct’ is that with ‘struct’ the variables are public by default and with ‘class’ they’re private.

Here is an example code using classes, objects, and inheritance:

```
#include <iostream>
#include <string>
using namespace std;

//PLP5 create an object
class Simmons{
    //give object class attributes 
    //access specifier
public: 
    //data members
    //our variable, a string 'stormy'
    std::string stormy;
    //our function that will print out our sentence
    void printname(){ cout << "Stormy is: " << stormy << endl; }
};

class SimmonsInheritance: public Simmons{
public:
    //extra data member
    std::string extraInfo;
    //and extra member function
    void printExtraInfo(){
        cout << "Is Stormy Simmon's mascot? " << extraInfo << endl;
    }
};

int main(){
    //creating our object within main that will inherit from our first object
    SimmonsInheritance object1;

    //object that is instantiated and modified that we're giving to our functions
    object1.extraInfo = "Yes!!!!! ";
    object1.stormy = "a Shark!";

    //calling our functions
    object1.printExtraInfo();
    object1.printname();
    return 0;
}
```

## Naming Conventions For Objects

There are no strict naming conventions that are enforced but there are common practices that are used when it comes to object naming conventions. 
- CamelCase - capitalizing the first letter of each word except the first word
- snake_case -  all lowercase letters with underscores separating words
- Prefixes or suffixes
- Avoiding single letter names for objects
- Constants are recommended to be in UPPERCASE to distinguish them from other variables
- Choosing descriptive names to make sure that the purpose of an object is clear

## Standard Methods
C++ has standard methods that are referred to as “special member functions” that define how objects behave in certain conditions within a program. 

Some of these key special member functions:
- Constructor - called when an object is created and it’s used to initialize an object’s state
```
class ExampleClass {
public:
		ExampleClass(); //this is a default constructor
		ExampleClass(int x, y); //constructor with parameters
	};
```

- Destructor - used when an object is out of scope and is used to release resources held by the object
```
class ExampleClass {
public:
		~ExampleClass(); //destructor
	};
```

- Copy Constructor - used to create new objects as a copy of an already existing object
```
class ExampleClass {
public:
		ExampleClass(const ExampleClass& other); //copy constructor
	};
```

## Inheritance
C++ supports inheritance and having multiple inheritances. Users are able to create new classes based on existing classes thus inheriting their properties and behaviors. To inherit more than one class, the user must separate the base classes with commas in the class declaration.
```
class ExampleClass : public ExampleClass2, public ExampleClass3 {
public:
	void ExampleFunc(){
		//code
	}
};
```

## Overloading Methods

Non-virtual functions

The method resolution relies on the object's static type (compile-time binding) if the function in the base class is not defined as virtual. In this instance, if the object belongs to the base class type, the version of the method in the base class will be called; otherwise, the version in the derived class will be invoked.

Virtual Function 

The dynamic type of the object determines the method resolution (runtime binding) if the function in the base class is designated as virtual. In this instance, even though the object is of the base class type but points to an object of the derived class, the version of the method in the derived class will be invoked.

## Access Specifiers

Access Specifiers control the visibility of members in a class when programming
- ‘public’ - public members of the base class become public members of the derived class
- ‘private’ - public and protected members of the base class become private members of the derived class
- ‘protected’ - public and protected members of the base class become protected members of the derived class
```
class ExampleClass {
public:
    // public members
private:
    // private members
protected:
    // protected members
};
```
## References

“C Loops.” GeeksforGeeks, GeeksforGeeks, 13 Jan. 2017, www.geeksforgeeks.org/cpp-loops/


“Short Circuiting in c and Linux.” GeeksforGeeks, GeeksforGeeks, 8 July 2020, www.geeksforgeeks.org/short-circuiting-in-c-and-linux/


‌“C++ Switch...Case Statement (with Examples).” Programiz.com, 2015, www.programiz.com/cpp-programming/switch-case. 
‌

“C++ Switch.” W3schools.com, 2023, www.w3schools.com/cpp/cpp_switch.asp


“Dangling Else Ambiguity.” GeeksforGeeks, GeeksforGeeks, 24 Dec. 2021, www.geeksforgeeks.org/dangling-else-ambiguity/


“How to Split a String in c c Python and Java.” GeeksforGeeks, GeeksforGeeks, 4 Feb. 2016, www.geeksforgeeks.org/how-to-split-a-string-in-cc-python-and-java/

‌



‌
‌




