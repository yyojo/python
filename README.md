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
