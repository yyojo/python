# Python Fundamentals
----


## Data Types and Operators 
---
### Arithmetic Operators

*  Addition:  +
*  Subtraction:  - 
*  Multiplication:  *
*  Division:  /
*  Mod (the remainder after dividing):  %
*  Exponentiation:  **
*  Divides and rounds down to the nearest integer:  //

```py
print(3 + 5) # 8
print(1 + 2 + 3 * 3) # 12
print(3 ** 2) # 9
print(9 % 2) # 1
```

### Variables 
In any case, whatever term is on the left side, is now a name for whatever value is on the right side. Once a value has been assigned to a variable name, you can access the value from the variable name.

The following two are equivalent in terms of assignment:

```py
x = 3
y = 4
z = 5
```

and: 

```py
x, y, z = 3, 4, 5
```

However, the above isn't a great way to assign variables in most cases, because our variable names should be descriptive of the values they hold.

Besides writing variable names that are descriptive, there are a few things to watch out for when naming variables in Python.

1. Only use ordinary letters, numbers and underscores in your variable names. They can’t have spaces, and need to start with a letter or underscore.

2. You can’t use Python's reserved words, or "keywords," as variable names. There are reserved words in every programming language that have important purposes, and you’ll learn about some of these throughout this course. Creating names that are descriptive of the values often will help you avoid using any of these keywords. 

3. The pythonic way to name variables is to use all lowercase letters and underscores to separate words

<img width="800" alt="Screen Shot 2022-08-05 at 9 55 02 PM" src="https://user-images.githubusercontent.com/109002901/183143049-74ebd262-2869-4187-adb9-b16d5cbdbfc2.png">

### Integers and Floats 
There are two Python data types that could be used for numeric values:

int - for integer values
float - for decimal or floating point values
You can create a value that follows the data type by using the following syntax:

```py
x = int(4.7)   # x is now an integer 4
y = float(4)   # y is now a float of 4.0
```

You can check the type by using the type function:

```py
>>> print(type(x))
int
>>> print(type(y))
float
```

Because the float, or approximation, for 0.1 is actually slightly more than 0.1, when we add several of them together we can see the difference between the mathematically correct answer and the one that Python creates.

```py
>>> print(.1 + .1 + .1 == .3)
False
```

### Booleans, Comparison Operators and Logical Operators
The bool data type holds one of the values **True** or **False**, which are often encoded as **1** or **0**, respectively.

There are 6 comparison operators that are common to see in order to obtain a **bool** value:

Comparison Operators:

<img width="493" alt="Screen Shot 2022-08-05 at 10 15 44 PM" src="https://user-images.githubusercontent.com/109002901/183145762-518e74f8-4caa-4387-a4cd-55400b19dfef.png">

And there are three logical operators you need to be familiar with:

<img width="691" alt="Screen Shot 2022-08-05 at 10 16 27 PM" src="https://user-images.githubusercontent.com/109002901/183145883-fb890843-467d-4363-bc49-c83e9b8a58b2.png">

### Strings
Strings in Python are shown as the variable type **str**. You can define a string with either double quotes " or single quotes '. If the string you are creating actually has one of these two values in it, then you need to be careful to assure your code doesn't give an error.

```py
>>> my_string = 'this is a string!'
>>> my_string = "this is also a string!"
```

You can also include a \ in your string to be able to include one of these quotes:

```py
>>> this_string = 'Simon\'s skateboard is in the garage.'
>>> print(this_string) # Simon's skateboard is in the garage.
```

If we don't use this, notice we get the following error:

```py
>>> this_string = 'Simon's skateboard is in the garage.'

/* 
 File "<ipython-input-20-e80562c2a290>", line 1
    this_string = 'Simon's skateboard is in the garage.'
                         ^
SyntaxError: invalid syntax
*/
```

There are a number of other operations you can use with strings as well. 

```py
>>> first_word = 'Hello'
>>> second_word = 'There'
>>> print(first_word + second_word)

HelloThere

>>> print(first_word + ' ' + second_word)

Hello There

>>> print(first_word * 5)

HelloHelloHelloHelloHello

>>> print(len(first_word))

5
```

**len()** is a built-in Python function that returns the length of an object, like a string. The length of a string is the number of characters in the string. This will always be an integer.

There is an example above, but here's another one:

```py
print(len("ababa") / len("ab"))
2.5
```

### Type and Type Conversion
You have seen four data types so far:

* int
* float
* bool
* string

The function **type()** can be used to check the data type of any variable you are working with. To convert a variable type to certian type: **type_name(variable)**
