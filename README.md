## Official site
https://www.python.org/

## Technical features
* An object-oriented programming language, comparable to Perl, Ruby, Scheme, or Java.
* Elegant sintax, making the programs you write easier to read.
* Easy-to-use language that makes it simple to get your program working.
* Comes with a large standard library that supports many common programming tasks.
* There is a bundled development environment called IDLE.
* Runs anywhere.

### Python keywords
```True```, ```False``` and ```None``` are written as it is, ALL THE OTHERS are written in lowercase.

### Identifiers
Same rules as Java, C#, etc.

### Python is case-sentitive

### Multi-line statement
```\``` explicit line continuation:

```python
a = 1 + 2 + 3 + \
    4 + 5 + 6 + \
    7 + 8 + 9 +
```

```()```, ```[]``` and ```{}``` implied line continuation

```python
a = (1 + 2 + 3
    4 + 5 + 6
    7 + 8 + 9)
```

### Multiple statements in a single line
We use ```;```

```a = 1; b = 2; c = 3```

### Identation
To define a block of code, Python uses identation.

```python
for i in range(1, 11):
    print(i)
    if i == 5
        break
print('finish')
```

Output: 
> 1, 2, 3, 4, 5, 'finish'

### Comments
Use **#** to comment something in the code 

### Multi-line comments
You can use **triple quotes** like ''' or """

### Docstring
It's a string that occurs as the first statement in a module, function, class, or method definition. We must write what a function/class does in the docstring.
We use triple quotes to write docstrings.

```python
def double(num)
    """ Function to double the value """
    return num * 2
print(double._doc_)
```

Output: 
>"Function to double the value"

### Variables
We don't need to declare a variable before using it.

#### Multiple assigments
```a, b, c = 5, 3.2, "Hello"```

```x = y = z = "same value"```

### Data types
Every value in Python has a data type.
Everything is an object in Python programming.
*data types* are actually classes and *variables* are instance(object) of these classes

* integers - ```int```
* floating point numbers ```float```
* complex numbers ```complex```

```python
a = 5
print(a, "is of type", type(a))
a = 2.0
print(a, "is of type", type(a))
a = 1 + 2j
print(a, "is complex number?", isinstance(1 + 2j, complex))
```

Output:

> 5 is of type <class 'int'>

> 2.0 if of type <class 'float'>

> (1 + 2j) is complex number? True

#### Integers
Can be any length (limited by the memory available)

#### Floating point numbers
Is acurate up to 15 decimal places

#### Complex numbers 
Are written in the form: **x + yj**, where **x** is the real part and **y** is the imaginary part

```python
a = 12345678901234567890
print(a)
b = 0.1234567890123456789
print(b)
c = 1 + 2j
print(c)
```

Output:

> 1234567890123456789

> 0.12345678901234568

> (1 + 2j)

! **b** got truncated at the final of floating point numbers

### List - ```use []```
Ordered sequence of items. 

```python
a = [1, 2.2, 'python']
```

```python
a = [5, 10, 15, 20, 25, 30, 35, 40]
# a[2] = 15
print("a[2] = ", a[2])
# a[0:3] = [5, 10, 15]
print("a[0:3] = ". a[0:3])
# a[5:] = [30, 35, 40]
print("a[5:] = ", a[5:])
```

Output:

> a[2] = 15

> a[0:3] = [5, 10, 15]

> a[5:] = [30, 35, 40]

#### Lists are mutable
Value of the elements of a list can be altered

```python
a = [1, 2, 3]
a[2] = 4
print(a)
```

Output: 
> [1, 2, 4]

### Python Tuple - ```use ()```
Ordered sequence of items.

#### Tuples are immutable
* are used to write protected data
* faster than list as it cannot change dynamically

#### It's defined within parentheses

```python
t = (5, 'program', 1 + 3j)
```

```python
t = (5, 'program', 1 + 3j)
print("t[1] =", t[1])
print("t[0:3] =", t[0:3])
t[0] = 10
```

> t[1] = program

> t[0:3] = (5, 'program', (1 + 3j))

Error:

> Traceback (most recent call last):
File "<stdin>", line 4, in <module> t[0] = 10
TypeError: 'tuple' object does not support item assignment

### Strings
* Sequence of unicoe characters
* We can use ```'``` or ```"```
* Multi-line Strings, we can use ```'''``` or ```"""```

```python
s = 'Hello world'
print("s[4] = ", s[4])
print("s[6:11] = ", s[6:11])
s[5] = 'd'
```

Output:

> s[4] = 0

> s[6:11] = world

> Traceback(most recent call last): File "<stdin>", line 4, in <module> s[5] = 'd'
TypeError: 'str' object does not support item assignment

**! strings are immutable**

### Python set - ```use {}```
Unordered collection of unique items

```python
a = {5, 2, 3, 1, 4}
print("a = ", a)
print(type(a))
```

Output:

> a = {1, 2, 3, 4, 5}

> <class 'set'>

#### Set eliminate duplication
```python
a = {1, 2, 3, 4, 5}
print(a)
```

Output:
> {1, 2, 3}

#### There is no indexing

```python
a = {1, 2, 3}
print(a[1])
```

Output:

> Traceback(most recent call last)
File "<stdin>", line 3, in <module>
print (a[1])
TypeError: 'set' object does not support indexing

### Python dictionary - ```use {}```
Unordered collection of key-value pairs
* Generally used when we have a huge amount of data. Dictionaries are optimized for retrieving data

```python
d = {1:'value', 'key': 2}
print(type(d))
print("d[1] = ", d[1])
print("d['key'] = ", d['key'])
print("d[2] = ", d[2])
```

Output:

> <class 'dict'>

> d[1] = value

> d['key'] = 2

> Traceback(most recent call last):
File "<stdin>", line 5, in <module>
print("d[2] = ", d[2])
KeyError: 2

### Convertion through data types

#### Float to int
It will truncate the value to make it close to 0
```python
print(int(10.6))
print(int(-10.9))
```

Output:
> 10

> -10

#### String

```python
print(float('2.5'))
print(str(25))
print(int('1p'))
```

Output:
> 2.5

> 25

> Traceback(most recent call last):
File "<string>", line 3, in runcode
File "<interactive input>", line 1, in <module>
ValueError: invalid literal for int() with base 10: '1p'

