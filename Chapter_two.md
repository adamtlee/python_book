# Chapter 2: Fundamentals of Python

This chapter introduces the core building blocks of Python programming, focusing on how data is stored, manipulated, and interacted with. Understanding these fundamental concepts is crucial for writing any Python program.

## Variables and Data Types
At its heart, programming involves working with data. Variables are essentially named storage locations that hold different kinds of data. Think of them as labeled boxes where you can put information.

## Naming Conventions
Choosing meaningful and consistent names for your variables is good practice. In Python, variable names:

- Must start with a letter or an underscore (_).
- Cannot start with a number.
- Can only contain alpha-numeric characters and underscores (A-z, 0-9, and _).
- Are case-sensitive (e.g., age is different from Age).
- Should ideally be in snake_case (words separated by underscores, all lowercase) for readability, e.g., first_name, total_price.

## Numeric Types
Python offers various numeric data types to represent numbers:

### Integers (int): 

Whole numbers, positive or negative, without a decimal point.

``` python
age = 30
quantity = -100
```

Floating-point numbers (float): Numbers with a decimal point, used to represent real numbers.

``` python
price = 19.99
temperature = 25.5
```

### Strings (str): 
Sequences of characters, enclosed in single quotes (' ') or double quotes (" "). Strings are used to represent text.

``` python
name = "Alice"
message = 'Hello, world!'
````

### Boolean Type
True, False (bool): Represents truth values. Booleans are fundamental for logical operations and control flow.

```python
is_active = True
has_permission = False
```

### Type Conversion
Sometimes you need to change the data type of a variable. Python provides built-in functions for type conversion (also known as type casting):

- int(): Converts a value to an integer.
- float(): Converts a value to a floating-point number.
- str(): Converts a value to a string.


```python
num_str = "123"
num_int = int(num_str)  # num_int will be 123 (integer)

float_val = 3.14
int_val = int(float_val) # int_val will be 3 (integer, truncates decimal)

int_num = 42
str_num = str(int_num)  # str_num will be "42" (string)
```

### Operators
Operators are special symbols that perform operations on variables and values.

Arithmetic Operators
Used for mathematical calculations:

| Operator | Description         | Example   | Result |
| :------- | :------------------ | :-------- | :----- |
| `+`      | Addition            | `5 + 3`   | `8`    |
| `-`      | Subtraction         | `10 - 4`  | `6`    |
| `*`      | Multiplication      | `2 * 6`   | `12`   |
| `/`      | Division            | `15 / 3`  | `5.0`  |
| `%`      | Modulus (remainder) | `10 % 3`  | `1`    |
| `**`     | Exponentiation      | `2 ** 3`  | `8`    |
| `//`     | Floor Division      | `10 // 3` | `3`    |

### Logical Operators
Used to combine conditional statements and return a Boolean result:

- and: Returns True if both statements are True.
- or: Returns True if at least one statement is True.
- not: Reverses the logical state of its operand (makes True False, and False True).

```python
x = 5
y = 10

print(x > 0 and y < 100) # True
print(x == 5 or y == 5)  # True
print(not(x > y))        # True
```

### Assignment Operators
Used to assign values to variables. They are a shorthand for combining an arithmetic operation with an assignment:

| Operator | Example   | Equivalent to |
| :------- | :-------- | :------------ |
| `=`      | `x = 10`  |               |
| `+=`     | `x += 5`  | `x = x + 5`   |
| `-=`     | `x -= 2`  | `x = x - 2`   |
| `*=`     | `x *= 3`  | `x = x * 3`   |
| `/=`     | `x /= 2`  | `x = x / 2`   |
| `%=`     | `x %= 3`  | `x = x % 3`   |
| `**=`    | `x **= 2` | `x = x ** 2`  |
| `//=`    | `x //= 2` | `x = x // 2`  |

### Input and Output
Programs often need to interact with the user or display information.

Getting User Input with input()
The input() function pauses the program execution, displays a prompt to the user, and waits for them to type something and press Enter. The entered text is always returned as a string.

```python
name = input("What is your name? ")
print("Hello, " + name)

age_str = input("How old are you? ")
age = int(age_str) # Convert the input string to an integer
print("You are", age, "years old.")
```

### Formatted Output
Displaying information clearly is important. Python offers several ways to format output:

f-strings (formatted string literals): A modern and highly readable way to embed expressions inside string literals. Prepend the string with f or F.

```python
item = "Laptop"
price = 1200.50
print(f"The {item} costs ${price:.2f}.") # .2f formats to 2 decimal places
```

.format() method: A versatile method for formatting strings using curly braces {} as placeholders.

```python
item = "Keyboard"
price = 75.00
print("The {} costs ${:.2f}.".format(item, price))
```

### Comments
Comments are essential for explaining your code to yourself and others. The Python interpreter ignores them.

Single-line Comments (#)
Start with a hash symbol (#). Anything after # on the same line is a comment.

```python
# This is a single-line comment
x = 10 # Assign 10 to x
```

### Multi-line Comments (Docstrings """ """)
For longer explanations or to describe functions/modules, use triple quotes (""" or '''). These are often referred to as docstrings when used immediately after a function, class, or module definition.

```python
Multi-line Comments (Docstrings """ """)
For longer explanations or to describe functions/modules, use triple quotes (""" or '''). These are often referred to as docstrings when used immediately after a function, class, or module definition.
```