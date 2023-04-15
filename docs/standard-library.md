# Standard Library Reference

## Basic I/O

``` read_line() -> String ``` : Read a line from the standard input

``` print(s: String) ``` : Print a string to the standard output without a newline

``` println(s: String) ``` : Print a string to the standard output with a newline

```  read_file(path: String) -> Result<String> ``` : Read the entire contents of a file

```  write_file(path: String, contents: String) -> Result<()> ```  : Write a string to a file

## Math functions and constants

``` PI: Float ``` : The mathematical constant π (pi)

``` E: Float ``` : The mathematical constant e (Euler's number)

``` sqrt(x: Float) -> Float ``` : Calculate the square root of x

```  sin(x: Float) -> Float ``` : Calculate the sine of x (in radians)

```  cos(x: Float) -> Float ``` : Calculate the cosine of x (in radians)

## String manipulation

```  concat(s1: String, s2: String) -> String ``` : Concatenate two strings

```  length(s: String) -> Int ``` : Get the length of a string

```  substring(s: String, start: Int, end: Int) -> String ``` : Get a substring from start to end

## Data structures and algorithms

```  List ``` : Generic list type with methods such as append, remove, length, etc.

```  Dict ``` : Generic dictionary type with methods such as insert, remove, keys, etc.

``` sort<T>(list: List<T>, cmp: Fn(T, T) -> Int) -> List<T> ``` : Sort a list using a comparison function

## Networking and concurrency

``` TcpStream ``` : A TCP connection type with methods for reading and writing data

``` spawn<F: FnOnce()>(f: F) -> JoinHandle ``` : Spawn a new thread to run a function

## Time and date handling

``` now() -> DateTime ``` : Get the current date and time

``` duration_from_now(dt: DateTime) -> Duration ``` : Calculate the duration between now and a given DateTime

## System interaction

``` env::get_var(key: String) -> Option<String> ``` : Get the value of an environment variable

```  fs::create_dir(path: String) -> Result<()> ``` : Create a new directory
