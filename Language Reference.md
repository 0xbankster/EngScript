# Introduction:

## Brief overview of EngScript

### EngScript is a modern programming language designed to facilitate seamless collaboration between humans and large language models (LLMs) like ChatGPT. 

It combines the simplicity and readability of Python, the performance and safety of Rust, and the concurrency model of Go. EngScript aims to maximize human readability by adopting an English-like syntax, making it easy for developers to write, read, and maintain code.

### Goals and design principles

The primary goals and design principles of EngScript include:

- **Readability**: EngScript uses an English-like syntax to make the code more understandable and accessible to a wider audience, including non-programmers and LLMs.
- **Performance**: EngScript leverages a hybrid approach with an interpreter and Just-In-Time (JIT) compilation to provide both rapid development capabilities and improved execution performance.
- **Safety**: EngScript is implemented in Rust, a language known for its safety guarantees and memory efficiency, ensuring the language implementation is robust and reliable.
- **Concurrency**: EngScript incorporates a concurrency model inspired by Go, enabling efficient parallel and concurrent execution of code.
- **Cross-platform compatibility**: EngScript is designed to support multiple platforms, including Windows, macOS, Linux, and WebAssembly, making it accessible to a wide range of users and devices.
- **Collaboration**: EngScript aims to facilitate effective collaboration between humans and LLMs, fostering an environment where both can work together to develop high-quality software.

### Applications and target audience

EngScript is a versatile language suitable for a variety of applications, including but not limited to:

- Web development
- Data processing and analysis
- Machine learning and artificial intelligence
- Automation and scripting
- Desktop applications
- Networking and distributed systems

The target audience for EngScript includes:

- Developers seeking an easy-to-read and efficient language for their projects
- Non-programmers who want to learn programming or collaborate with LLMs more effectively
- Researchers and AI practitioners working with large language models
- Educators and students in computer science and related fields

## Getting Started

### Installation and setup

To install and set up EngScript, follow these steps:

1. Ensure you have the Rust compiler and Cargo installed on your system. You can download and install them from the official Rust website.
2. Clone the EngScript repository:

``` git clone https://github.com/0xbankster/engscript.git ```

1. Navigate to the repository directory:

``` cd engscript ```

2. Build the EngScript compiler or interpreter:

``` cargo build --release ```


3. Add the EngScript binary to your system's PATH, or create a symlink to the binary in a directory within your PATH.

### Running EngScript programs

To execute an EngScript program, open a terminal or command prompt and run the following command:

``` engscript run path/to/your_program.eng ```

Replace `path/to/your_program.eng` with the path to your EngScript source file.

### Basic "Hello, World!" example

Here's a simple EngScript program that demonstrates how to output "Hello, World!" to the console:

``` 
begin program 
display "Hello, World!" 
end program 
```

To run this example, save the code in a file called `hello_world.eng`, and then execute the following command in your terminal or command prompt:

``` engscript run hello_world.eng ```

This should display "Hello, World!" in your terminal or command prompt.

### Syntax and Semantics

#### Variables and data types

EngScript supports several basic data types:

- Int: Integer numbers (e.g., -2, 0, 42)
- Float: Floating-point numbers (e.g., 3.14, -0.001)
- Bool: Boolean values (True or False)
- String: Sequences of characters (e.g., "Hello, World!")
- Char: Single characters (e.g., 'a', 'Z', '%')
- List: Ordered collections of elements (e.g., [1, 2, 3], ["apple", "banana", "cherry"])
- Dict: Collections of key-value pairs (e.g., {"one": 1, "two": 2, "three": 3})
- Tuple: Fixed-size, ordered collections of elements (e.g., (1, "two", 3.0))
- Option: Represents optional values, either Some(value) or None
- Result: Represents the result of a computation, either Ok(value) or Err(error)


### Variable declaration and assignment:

``` 
declare x as Int
x is 10

declare name as String
name is "Alice" 
```

### Operators
### EngScript provides various operators for different operations:

Arithmetic: +, -, *, /, %

Comparison: ==, !=, <, >, <=, >=

Logical: and, or, not

Bitwise: &, |, ^, ~, <<, >>

Assignment: is, +=, -=, *=, /=, %=, &=, |=, ^=, <<=, >>=

Operator precedence and associativity are similar to those in most programming languages, such as Python and C++.


### Control structures
### if/else statements:

```
if x > 0
    display "x is positive"
else if x < 0
    display "x is negative"
else
    display "x is zero"
```

### for and while loops:
```
declare sum as Int
sum is 0

for i in range 1 to 10
    sum += i

declare n as Int
n is 1

while n <= 100
    display n
    n *= 2
```

_____________________

BELOW UNEDITED

Pattern matching with match:

match value
    when "start"
        display "Starting the process"
    when "stop"
        display "Stopping the process"
    when "pause"
        display "Pausing the process"
    otherwise
        display "Unknown command"

Functions
Defining and calling functions:

function greet(name as String) as String
    return "Hello, " + name + "!"

declare greeting as String
greeting is greet("Alice")
display greeting

Function arguments and return values:

function add(a as Int, b as Int) as Int
    return a + b

declare result as Int
result is add(2, 3)
display result

Anonymous functions and closures:

declare numbers as List of Int
numbers is [1, 2, 3, 4, 5]

declare squared as List of Int
squared is map(numbers, function (x as Int) as Int
                    return x * x
                )
Error handling
Handling errors with Result and Option
EngScript uses the Result and Option types to handle errors and represent optional values, respectively.

Result:

function divide(a as Float, b as Float) as Result of Float
    if b == 0.0
        return Err("Division by zero")
    return Ok(a / b)

declare result as Result of Float
result is divide(10.0, 2.0)

match result
    when Ok(value)
        display "Result: " + value
    when Err(error)
        display "Error: " + error

Option:

function find_user(id as Int) as Option of String
    if id == 1
        return Some("Alice")
    return None

declare user as Option of String
user is find_user(1)

match user
    when Some(name)
        display "User found: " + name
    when None
        display "User not found"

Using try and catch for error handling:

try
    declare result as Float
    result is divide(10.0, 0.0)
    display "Result: " + result
catch error as String
    display "Error: " + error

Modules and Libraries
Importing and exporting modules

In math.eng:

export function add(a as Int, b as Int) as Int
    return a + b

export function multiply(a as Int, b as Int) as Int
    return a * b

In main.eng:

import math

declare result as Int
result is math.add(2, 3)
display result

EngScript standard library overview
The EngScript standard library provides a wide range of functionality, including:

Basic I/O (e.g., reading and writing files, console input and output)
Math functions and constants
String manipulation
Data structures and algorithms
Networking and concurrency
Time and date handling
System interaction
Popular third-party libraries and how to use them
EngScript supports the use of third-party libraries for various purposes. Some popular libraries include:

Web frameworks for developing web applications
Database libraries for working with various databases
Libraries for machine learning and data analysis
Libraries for working with various file formats and protocols
To use a third-party library, you will generally need to install it using a package manager and then import it into your EngScript code.

Object-Oriented Programming
Structs
Defining and instantiating structs:

struct Point
    x as Float
    y as Float

declare point as Point
point is Point(1.0, 2.0)

Accessing and modifying struct fields
display "X: " + point.x
display "Y: " + point.y

point.x is 3.0
point.y is 4.0

display "Updated X: " + point.x
display "Updated Y: " + point.y

Enums
Defining and using enums:

enum Color
    Red
    Green
    Blue

declare my_color as Color
my_color is Color.Red

match my_color
    when Color.Red
        display "The color is red"
    when Color.Green
        display "The color is green"
    when Color.Blue
        display "The color is blue"

Traits
Defining and implementing traits:

trait Drawable
    function draw() as String

struct Circle
    radius as Float

impl Drawable for Circle
    function draw() as String
        return "Drawing a circle with radius " + self.radius

declare my_circle as Circle
my_circle is Circle(5.0)

declare my_drawable as Drawable
my_drawable is my_circle

display my_drawable.draw()

Trait inheritance and composition:

trait Shape
    function area() as Float

trait SolidShape
    inherits Shape
    function volume() as Float

trait Printable
    function print() as String

impl Printable for Circle
    function print() as String
        return "Circle with radius " + self.radius
Impls
Implementing methods for structs and enums:

struct Rectangle
    width as Float
    height as Float

impl Rectangle
    function area() as Float
        return self.width * self.height

declare my_rectangle as Rectangle
my_rectangle is Rectangle(3.0, 4.0)

display my_rectangle.area()

Concurrency and Parallelism
Asynchronous functions with async:

async function fetch_data(url as String) as String
    // Simulate a network request
    await sleep(1000)
    return "Data from " + url

async function main()
    declare data as String
    data is await fetch_data("https://example.com")
    display data

main()


Awaiting asynchronous operations with await:
async function download_files(urls as List of String)
    for url in urls
        display "Downloading " + url
        await sleep(1000)
        display "Downloaded " + url

async function main()
    declare urls as List of String
    urls is ["https://example.com/file1", "https://example.com/file2"]

    await download_files(urls)

main()

Concurrency patterns and best practices:

Use lightweight tasks or threads for concurrent execution
Use channels or message passing for communication between concurrent tasks
Avoid shared mutable state and use synchronization primitives when necessary
Memory Management and Safety
Ownership and borrowing in EngScript:

EngScript enforces strict ownership rules to ensure memory safety
Variables have a single owner, and ownership can be transferred (moved) between variables
Borrowing allows temporary access to a variable's data without transferring ownership
There are two types of borrowing: mutable (unique access) and immutable (shared access)
Memory safety guarantees provided by the language:

EngScript prevents data races, dangling pointers, and null pointer dereferences
The borrow checker ensures that references to data are valid and not aliased inappropriately
EngScript enforces strict lifetime rules to ensure that references never outlive the data they point to
Performance optimization techniques:

Use efficient data structures and algorithms
Minimize memory allocations and deallocations
Utilize concurrency and parallelism to make the most of multi-core processors
Interoperability
Interfacing with other languages (e.g., C, C++, Rust):

EngScript can interface with other languages using the Foreign Function Interface (FFI)
Functions written in other languages can be declared with the extern.

keyword and their signatures must match the original functions
To pass data between languages, use appropriate data types and conversions
Foreign Function Interface (FFI) and best practices:

Use a separate module for FFI bindings
Create safe and idiomatic wrappers around unsafe foreign functions
Handle errors and edge cases gracefully
Advanced Topics
Metaprogramming and macros:

EngScript supports metaprogramming through macros, which allow you to generate code at compile time
Macros are powerful but should be used judiciously to maintain code readability and maintainability
Customizing the build process:

EngScript allows you to customize the build process using build scripts and configuration files
Use build scripts to automate tasks such as code generation, linking to external libraries, and setting compiler flags
Debugging and profiling tools:

EngScript provides a variety of debugging and profiling tools to help diagnose and optimize performance issues
Use debuggers to step through code execution and inspect variables
Use profilers to identify performance bottlenecks and optimize resource usage

Appendices
Glossary of terms
Add definitions of important terms and concepts related to EngScript

Language grammar
Provide a formal description of EngScript's syntax using a notation such as Backus-Naur Form (BNF) or Extended Backus-Naur Form (EBNF)

EngScript style guide
Provide guidelines and best practices for writing clean, maintainable, and idiomatic EngScript code
Cover topics such as naming conventions, indentation, commenting, and error handling
