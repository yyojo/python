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
### String Methods and Functions
A method in Python behaves similarly to a function. Methods actually are functions that are called using dot notation. For example, **lower()** is a string method that can be used like this, on a string called "sample string": sample_string.lower().

Methods are specific to the data type for a particular variable. So there are some built-in methods that are available for all strings, different methods that are available for all integers, etc.

<img width="814" alt="Screen Shot 2022-08-05 at 10 40 32 PM" src="https://user-images.githubusercontent.com/109002901/183149188-99417b08-d4cb-4542-91bd-3af87e9d20e3.png">

**len()** is a built-in Python function that returns the length of an object, like a string. The length of a string is the number of characters in the string. This will always be an integer.

There is an example above, but here's another one:

```py
print(len("ababa") / len("ab"))
2.5
```

We will be using the **format()** string method a good bit in our future work in Python, and you will find it very valuable in your coding, especially with your print statements.

We can best illustrate how to use format() by looking at some examples.

```py
print("Mohammed has {} balloons".format(27))
# output: Mohammed has 27 balloons

animal = "dog"
action = "bite"
print("Does your {} {}?".format(animal, action))
# output: Does your dog bite?

maria_string = "Maria loves {} and {}"
print(maria_string.format("math", "statistics"))
output: Maria loves math and statistics
```

A helpful string method when working with strings is the **.split()** method. This function or method returns a data container called a list that contains the words from the input string. We will be introducing you to the concept of lists in the next video.

The split method has two additional arguments (sep and maxsplit). The sep argument stands for "separator". It can be used to identify how the string should be split up (e.g., whitespace characters like space, tab, return, newline; specific punctuation (e.g., comma, dashes)). If the sep argument is not provided, the default separator is whitespace.

True to its name, the maxsplit argument provides the maximum number of splits. The argument gives maxsplit + 1 number of elements in the new list, with the remaining string being returned as the last element in the list. 

### Type and Type Conversion
You have seen four data types so far:

* int
* float
* bool
* string

The function **type()** can be used to check the data type of any variable you are working with. To convert a variable type to certian type: **type_name(variable)**

### Debugging Code
Everyone gets "bugs," or unexpected errors, in their code, and this is a normal and expected part of software development. We all say at one time or another, "Why isn't this computer doing what I want it to do?!"

So an important part of coding is "debugging" your code, to remove these bugs. This can often take a long time, and cause you frustration, but developing effective coding habits and mental calmness will help you address these issues. With determined persistence, you can prevail over these bugs!

Here are some tips on successful debugging that we'll discuss in more detail below:

Understand common error messages you might receive and what to do about them.
Search for your error message, using the Web community.
Use print statements.

Understanding Common Error Messages
There are many different error messages that you can receive in Python, and learning how to interpret what they're telling you can be very helpful. Here are some common ones for starters:

* "ZeroDivisionError: division by zero." This is an error message that you saw earlier in this lesson. What did this error message indicate to us? You can look back in the Quiz: Arithmetic Operators section to review it if needed.
* "SyntaxError: unexpected EOF while parsing" This message is often produced when you have accidentally left out something, like a parenthesis. The message is saying it has unexpectedly reached the end of file ("EOF") and it still didn't find that right parenthesis. This can easily happen with code syntax involving pairs, like beginning and ending quotes also. Take a look at the two lines of code below. Executing these lines produces this syntax error message:

```py
greeting = "hello"
print(greeting.upper
```

* "TypeError: len() takes exactly one argument (0 given)" This kind of message could be given for many functions, like len in this case, if I accidentally do not include the required number of arguments when I'm calling a function, as below. This message tells me how many arguments the function requires (one in this case), compared with how many I gave it (0). I meant to use len(chars) to count the number of characters in this long word, but I forgot the argument.

```py
chars = "supercalifragilisticexpialidocious"
len()
```

**Search for Your Error Message**

Software developers like to share their problems and solutions with each other on the web, so using Google search, or searching in StackOverflow, or searching in Udacity's Knowledge forum are all good ways to get ideas on how to address a particular error message you're getting.

Copy and paste the error message into your web browser search tab, or in Knowledge, and see what others suggest about what might be causing it.
You can copy and paste the whole error message, with or without quotes around it.
Or you can search using just key words from the error message or situation you're facing, along with some other helpful words that describe your context, like Python and Mac.

**Use Print Statements to Help Debugging**

Adding print statements temporarily into your code can help you see which code lines have been executed before the error occurs, and see the values of any variables that might be important. This approach to debugging can also be helpful even if you're not receiving an error message, but things just aren't working the way you want.

We'll suggest particular occasions to use this approach in upcoming helpful places in this course.

## Data Structures
----
### Lists and Membership Operators
A **list** is one of the most common and basic data structures in Python.
You saw here that you can create a list with square brackets. Lists can contain any mix and match of the data types you have seen so far.

```py
list_of_random_things = [1, 3.4, 'a string', True]
```

This is a list of 4 elements. All ordered containers (like lists) are indexed in python using a starting index of 0. Therefore, to pull the first value from the above list, we can write:

```py
>>> list_of_random_things[0]
1
```

Alternatively, you can index from the end of a list by using negative values, where -1 is the last element, -2 is the second to last element and so on.

```py
>>> list_of_random_things[-1] 
True
>>> list_of_random_things[-2] 
a string
```

**Slice and Dice with Lists**

You saw that we can pull more than one value from a list at a time by using slicing. When using slicing, it is important to remember that the lower index is **inclusive** and the upper index is **exclusive**.

```py
>>> list_of_random_things = [1, 3.4, 'a string', True]
>>> list_of_random_things[1:2]
[3.4]
```
If you know that you want to start at the beginning, of the list you can also leave out this value.

```py
>>> list_of_random_things[:2]
[1, 3.4]
```

This type of indexing works exactly the same on strings, where the returned value will be a string.

```py
>>> list_of_random_things[1:]
[3.4, 'a string', True]
```

**in and not in**

We can also use in and not in to return a bool of whether an element exists within our list, or if one string is a substring of another.

```py
>>> 'this' in 'this is a string'
True
>>> 'in' in 'this is a string'
True
>>> 'isa' in 'this is a string'
False
>>> 5 not in [1, 2, 3, 4, 6]
True
>>> 5 in [1, 2, 3, 4, 6]
False
```

**Mutability and Order**

**Mutability** is about whether or not we can change an object once it has been created. If an object (like a list or string) can be changed (like a list can), then it is called mutable. However, if an object cannot be changed with creating a completely new object (like strings), then the object is considered immutable.

```py
>>> my_lst = [1, 2, 3, 4, 5]
>>> my_lst[0] = 'one'
>>> print(my_lst)
['one', 2, 3, 4, 5]
```

As shown above, you are able to replace 1 with 'one' in the above list. This is because lists are **mutable**.
However, the following does not work:

```py
>>> greeting = "Hello there"
>>> greeting[0] = 'M'
```

This is because strings are **immutable**. This means to change this string, you will need to create a completely new string.
There are two things to keep in mind for each of the data types you are using:
* Are they mutable?
* Are they ordered?

**Order** is about whether the position of an element in the object can be used to access the element. **Both strings and lists are ordered**. We can use the order to access parts of a list and string.
However, you will see some data types in the next sections that will be unordered. For each of the upcoming data structures you see, it is useful to understand how you index, are they mutable, and are they ordered. 

### List Methods
Useful Functions for Lists:
* **len()** returns how many elements are in a list.
* **max()** returns the greatest element of the list. How the greatest element is determined depends on what type objects are in the list. The maximum element in a list of numbers is the largest number. The maximum elements in a list of strings is element that would occur last if the list were sorted alphabetically. This works because the the max function is defined in terms of the greater than comparison operator. The max function is undefined for lists that contain elements from different, incomparable types.
* **min()** returns the smallest element in a list. min is the opposite of max, which returns the largest element in a list.
* **sorted()** returns a copy of a list in order from smallest to largest, leaving the list unchanged.
* **join()** is a string method that takes a list of strings as an argument, and returns a string consisting of the list elements joined by a separator string.

```py
name = "-".join(["García", "O'Kelly"])
print(name)
# output: García-O'Kelly
```

* **append()** A helpful method adds an element to the end of a list.

```py
letters = ['a', 'b', 'c', 'd']
letters.append('z')
print(letters)
#output: ['a', 'b', 'c', 'd', 'z']
```

### Tuples
A tuple is another useful container. It's a data type for immutable ordered sequences of elements. They are often used to store related pieces of information. Consider this example involving latitude and longitude:

```py
location = (13.4125, 103.866667)
print("Latitude:", location[0])
print("Longitude:", location[1])
```

Tuples are similar to lists in that they store an ordered collection of objects which can be accessed by their indices. Unlike lists, however, tuples are immutable - you can't add and remove items from tuples, or sort them in place.
Tuples can also be used to assign multiple variables in a compact way.

```py
dimensions = 52, 40, 100
length, width, height = dimensions
print("The dimensions are {} x {} x {}".format(length, width, height))
```

The parentheses are optional when defining tuples, and programmers frequently omit them if parentheses don't clarify the code.
In the second line, three variables are assigned from the content of the tuple dimensions. This is called tuple unpacking. You can use tuple unpacking to assign the information from a tuple into multiple variables without having to access them one by one and make multiple assignment statements.

### Sets
A set is a data type for mutable unordered collections of unique elements. One application of a set is to quickly remove duplicates from a list.

```py
numbers = [1, 2, 6, 3, 1, 1, 6]
unique_nums = set(numbers)
print(unique_nums)
#output: {1, 2, 3, 6}
```

Sets support the **in** operator the same as lists do. You can add elements to sets using the **add** method, and remove elements using the **pop** method, similar to lists. Although, when you pop an element from a set, a random element is removed. Remember that sets, unlike lists, are unordered so there is no "last element".

```py
fruit = {"apple", "banana", "orange", "grapefruit"}  # define a set

print("watermelon" in fruit)  # check for element

fruit.add("watermelon")  # add an element
print(fruit)

print(fruit.pop())  # remove a random element
print(fruit)

/* outputs:
False
{'grapefruit', 'orange', 'watermelon', 'banana', 'apple'}
grapefruit
{'orange', 'watermelon', 'banana', 'apple'} */
```

### Dictionaries and Identity Operators
A **dictionary** is a mutable data type that stores mappings of unique keys to values. Here's a dictionary that stores elements and their atomic numbers.

```py
elements = {"hydrogen": 1, "helium": 2, "carbon": 6}
```

Dictionaries can have keys of any immutable type, like integers or tuples, not just strings. It's not even necessary for every key to have the same type! We can look up values or insert new values in the dictionary using square brackets that enclose the key.

```py
print(elements["helium"])  # print the value mapped to "helium"
elements["lithium"] = 3  # insert "lithium" with a value of 3 into the dictionary
```

We can check whether a value is in a dictionary the same way we check whether a value is in a list or set with the **in** keyword. Dicts have a related method that's also useful, **get**. **get** looks up values in a dictionary, but unlike square brackets, **get** returns None (or a default value of your choice) if the key isn't found.

```py
print("carbon" in elements) # True
print(elements.get("dilithium")) # None
```

Carbon is in the dictionary, so True is printed. Dilithium isn’t in our dictionary so None is returned by get and then printed. If you expect lookups to sometimes fail, get might be a better tool than normal square bracket lookups because errors can crash your program.

**Identity Operators**

* **is** - evaluates if both sides have the same identity
* **is not** - evaluates if both sides have different identities

```py
n = elements.get("dilithium")
print(n is None) # True
print(n is not None) # False
```

<img width="791" alt="Screen Shot 2022-08-06 at 11 13 09 AM" src="https://user-images.githubusercontent.com/109002901/183240725-509d8ce6-3fb9-4adf-8a66-2e9c9515f577.png">

* You can use curly braces to define a **set** like this: {1, 2, 3}. However, if you leave the curly braces empty like this: {} Python will instead create an **empty dictionary**. So to create an empty set, use **set()**.
* A dictionary itself is **mutable**, but each of its individual **keys must be immutable**.

## Control Flow 
----
### Conditional Statements
