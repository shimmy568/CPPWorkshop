# C++ For Beginners Part1

## Installation (Ubuntu only)

> sudo apt-get install g++

You can then build and execute your program using

```bash
g++ -o main hello.cpp
./main
```

## Installation (Windows)

These are ordered by how difficult they are to setup

- Online CPP debugger: https://www.onlinegdb.com/online_c++_debugger
- Code Blocks: http://www.codeblocks.org/
- Visual Studio: https://visualstudio.microsoft.com/vs/community/
- MinGW (closest to what I'll be using): https://www.mingw-w64.org/

## Part 1

### Hello World and Comments

```cpp
#include <iostream> // This is including the libraries that we'll need to input and output data to the console

// This is the main function, this is the starting point for all C++ programs
int main()
{
  // This is a inline comment, any text after the "//" will be ignored on the compiler

  /*
    This is a block comment, anything between will be ignored by the compiler

    Hello :)
  */

  std::cout << "Hello, World!" << std::endl;
  std::cout << "This is a new line" << std::endl;

  std::cout << "This is what happens if you don't add a newline. ";
  std::cout << "This will be printed on the same line as the last." << std::endl;

  std::cout << "You can also make a new line like this\n";
  std::cout << "See?" << std::endl;

  // This return exits the main function. Returning anything other than 0 means the program ran into an error
  return 0;
}
```

In C++ you can have as much or as little whitespace as you want. As long as you have a ";" at the end of the "line" the compiler doesn't really care. For example you could write a hello world program like.

```cpp
#include <iostream>

int main(){std::cout<<"Hello, World!"<<std::endl;return 0;}
```

But that makes the code nearly impossible to read. So unless you're doing code golf (trying to code an algorithm with as little chars as possible) please please don't do this.

#### Resources

- https://www.w3schools.com/cpp/cpp_comments.asp
- https://www.tutorialspoint.com/cplusplus/cpp_comments.htm

### Variables

You can make a variable in C++ with the format `type variableName = value;`

```cpp
#include <iostream>
#include <string>

int main()
{

  // Basic Variable types
  int a; // Stores whole numbers, e.g. 123, -534, 1235
  int a2 = 5; // Stores whole numbers, e.g. 123, -534, 1235
  double b = 3.4; // Stores floating point numbers (numbers with decimal points) e.g. 2.5, -3.234
  char c = 'a'; // Stores be any letter or symbol, e.g. 'a', 'B', '@'
  bool d = true; // Can either be "true" or "false", nothing else
  bool d1 = false; // Can either be "true" or "false", nothing else
  std::string e = "hello"; // Stores text

  std::cout << "The value of 'a2' is " << a2 << std::endl;
  std::cout << "The value of 'd' is " << d << std::endl;
  std::cout << "The value of 'd1' is " << d1 << std::endl;
  std::cout << "The value of 'e' is " << e << std::endl;

  int f, g, h; // Declare multiple variables of the same type on the same line
  f = g = h = 20; // Set multiple variables to the same value
  int i = 50, j = 60, k = 70; // You can also set values to each variable as you declare it

  std::cout << "The sum of 'i' 'j' 'k' is " << i + j + k << std::endl;

  return 0;
}
```

#### Resources

- https://www.w3schools.com/cpp/cpp_variables.asp
- https://www.w3schools.com/cpp/cpp_variables_multiple.asp
- https://www.tutorialspoint.com/cplusplus/cpp_data_types.htm
- https://www.tutorialspoint.com/cplusplus/cpp_variable_types.htm

### Math Operators

```cpp
#include <iostream>

int main()
{
  int sum1 = 10 + 50; // Using the addition operator (+), we add 10 and 50 and put it into sum1
  int sum2 = sum1 + 20 // We take the value stored in sum1 and add 20 to, then store it in sum2
  int sum3 = sum1 + sum2; // Now we add sum1 and sum2

  std::cout << "sum1: " << sum1 << ", sum2: " << sum2 << ", sum3: " << sum3 << std::endl;

  // Subtraction
  std::cout << "50 - 60 = " << 50 - 60 << std::endl;

  // Multiplication
  std::cout << "5 * 6 = " << 5 * 6 << std::endl;

  // Division
  std::cout << "20 / 5 = " << 50 / 60 << std::endl;

  // Modulo (remainder from division)
  std::cout << "20 % 3 = " << 20 % 3 << std::endl;

  // Order of operators happens here too (BEDMAS / PEDMAS)
  std::cout << "10 + 5 * 5 = " << 10 + 5 * 5 << std::endl;

  // Brackets baby
  std::cout << "(10 + 5) * 5 = " << (10 + 5) * 5 << std::endl;

  // Assignment operators
  int a = 20;

  a += 10; // Is the same as "a = a + 10"
  std::cout << "a = " << a << std::endl;

  a -= 5; // Is the same as "a = a - 5"
  std::cout << "a = " << a << std::endl;

  a *= 2; // Is the same as "a = a * 2"
  std::cout << "a = " << a << std::endl;

  a /= 5; // Is the same as "a = a / 5"
  std::cout << "a = " << a << std::endl;

  a %= 2; // Is the same as "a = a % 2"
  std::cout << "a = " << a << std::endl;



  return 0;
}
```

#### Resources

- https://www.w3schools.com/cpp/cpp_operators.asp
- https://www.w3schools.com/cpp/cpp_operators_assignment.asp

### Comparison Operators

```cpp
#include <iostream>

int main()
{
  int a = 10, b = 20, c = 10;

  // Equals
  std::cout << (a == c) << std::endl; // Returns 1 (true) a is equal to c

  // Not Equals
  std::cout << (a != c) << std::endl; // Returns 1 (true) a is equal to c

  // Less than
  std::cout << (a < b) << std::endl; // Returns 1 (true) a is less than b

  // Greater than
  std::cout << (a > b) << std::endl; // Returns 0 (false) a is not greater than b

  // Greater than equals
  std::cout << (a >= c) << std::endl; // Returns 1 (true) since a is greater than or equal to c

  // Less than equals
  std::cout << (a <= b) << std::endl; // Returns 1 (true) since a is less than or equal to b

  return 0;
}
```

#### Resources

- https://www.w3schools.com/cpp/cpp_operators_comparison.asp
- https://en.cppreference.com/w/cpp/language/operator_comparison

### Logical Operators

#### AND (&&) operator table

| a     | b     | a && b |
| ----- | ----- | ------ |
| false | false | false  |
| false | true  | false  |
| true  | false | false  |
| true  | true  | true   |

#### OR (||) operator table

| a     | b     | a && b |
| ----- | ----- | ------ |
| false | false | false  |
| false | true  | false  |
| true  | false | false  |
| true  | true  | true   |

#### NOT (!) operator table

| a     | !a    |
| ----- | ----- |
| false | true  |
| true  | false |

#### Code

```cpp
#include <iostream>

int main()
{
  bool a = true, b = false, c = true;

  // And operator (both sides need to be true for the whole thing to be true)
  std::cout << "true && false = " << true && false << std::endl; // false (0) since both sides of && aren't true
  std::cout << "a && c = " << a && c << std::endl; // True (1) since both a and c are true

  // Or operator (only one of the sides needs to be true for the whole thing to be true)
  std::cout << "true || false = " << true || false << std::endl; // True since one side is true
  std::cout << "false || false = " << true || false << std::endl; // False since both sides are false

  std::cout << "!true = " << !true << std::endl; // False since we just negated true

  // Using all operators at once
  std::cout << "!((a || b) && c) = " << !((a || b) && c) << std::endl; // Evaluates to false

  return 0;
}
```

#### Resources

- https://www.w3schools.com/cpp/cpp_operators_logical.asp
- https://www.tutorialspoint.com/cplusplus/cpp_logical_operators.htm
- https://en.cppreference.com/w/cpp/language/operator_logical

### User Input (finally)

```cpp
#include <iostream>
#include <string>

// This makes the current namespace std, this lets the compiler know we want to use the std namespace so we don't have to prefix all std resources with std::
using namespace std;

// << is the stream insertion operator. It is used to insert data into a stream
// >> is the stream extraction operator. It is used to extract data from a stream

int main()
{
  int x, y;
  int sum;
  cout << "Type a number: ";
  cin >> x; // Getting input as an int
  cout << "Type another number: ";
  cin >> y;
  sum = x + y;
  cout << "Sum is: " << sum << endl;

  string name;
  cout << "Type your name: ";
  cin >> name; // Getting input as a string
  cout << "Hello there " << name << endl;

  return 0;
}
```

#### Resources

- https://www.tutorialspoint.com/cplusplus/cpp_namespaces.htm
- https://www.w3schools.com/cpp/cpp_user_input.asp

### If statements

Username password program method 1 (only if's)

```cpp
#include <iostream>
#include <string>

using namespace std;

int main()
{
  string username, password;
  cout << "username: ";
  cin >> username;
  cout << "password: ";
  cin >> password;

  if (username != "bobby") {
    cout << "USERNAME IS WRONG" << endl;
    return 0; // Exit the main function
  }

  if (password != "password123") {
    cout << "PASSWORD IS WRONG" << endl;
    return 0; // Exit the main function
  }

  cout << "Access granted" << endl;

  return 0;
}
```

Username password program method 2 (if and else)

```cpp
#include <iostream>
#include <string>

using namespace std;

int main()
{
  string username, password;
  cout << "username: ";
  cin >> username;
  cout << "password: ";
  cin >> password;

  if (username == "bobby" && password == "password123") {
    cout << "Access granted" << endl; // If condition is true this runs
  } else {
    cout << "Either username or password is wrong" << endl; // If condition is false this runs
  }

  cout << "Exiting now..." << endl; // Continues running after both the if and else

  return 0;
}
```

Username password program method 3 (if, else if, and else)

```cpp
#include <iostream>
#include <string>

using namespace std;

int main()
{
  string username, password;
  cout << "username: ";
  cin >> username;
  cout << "password: ";
  cin >> password;

  if (username != "bobby") {
    cout << "USERNAME IS WRONG" << endl;  // If condition is true this runs
  } else if (password != "password123") {
    cout << "PASSWORD IS WRONG" << endl;  // If first condition is false and second condition is true this runs
  } else {
    cout << "Access granted" << endl; // If all conditions are false this runs
  }

  cout << "Exiting now..." << endl;

  return 0;
}
```

#### Resources

- https://www.tutorialspoint.com/cplusplus/cpp_if_statement.htm
- https://www.w3schools.com/cpp/cpp_conditions_elseif.asp

### While loops

```cpp
#include <iostream>
#include <string>

using namespace std;

int main()
{
  int a = 0;

  // The loop will run again and again as long as the condition is true
  while (a < 10) {
    cout << "a = " << a << ", a * a = " << a * a << endl;
    a++; // This is the increment operator, it will add 1 to a. Same as doing a += 1 or a = a + 1
  }

  return 0;
}
```

#### Resources

- https://www.w3schools.com/cpp/cpp_while_loop.asp
- https://www.tutorialspoint.com/cplusplus/cpp_while_loop.htm

### Part 1 Practice

Do these if you're looking to try out the stuff we learned in part 1. These simple programs should only need the stuff we've learned so far to make. If you run into any issue you can't solve on your own feel free to message me on discord (ghost-flu#5725).

#### Odd or even

Welcome a user then ask them for a number between 1 and 1000.

When the user gives you the number, you check if it's odd or even and then you print a message letting them know.

#### Rock paper scissors game

Have two users enter either rock paper or scissors and output the winner between them

#### BONUS: Palindrome checker

You will need to use some stuff we didn't cover. You will need to be able to get the [length of a string](https://www.w3schools.com/cpp/cpp_strings_length.asp), and [get a character in the string](https://www.w3schools.com/cpp/cpp_strings_access.asp). Along with loops, which we did cover.

Ask the user to give you five words. Then check if each of the five words is a palindrome.

A palindrome is a word that remains the same whether it's read forward or backward.

Example:

- madam is a palindrome.
- so is malayalam.
- But not geeks.
