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

> a = {1, 2, 3, 4, 5}

> <class 'set'>

#### Set eliminate duplication
```python
a = {1, 2, 3, 4, 5}
print(a)
```

> {1, 2, 3}

#### There is no indexing

```python
a = {1, 2, 3}
print(a[1])
```

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

> 10

> -10

#### String

```python
print(float('2.5'))
print(str(25))
print(int('1p'))
```

> 2.5

> 25

> Traceback(most recent call last):
File "<string>", line 3, in runcode
File "<interactive input>", line 1, in <module>
ValueError: invalid literal for int() with base 10: '1p'

### ```Print()```

Sintax:
```python
print(*objects, sep'', end='\n', file=sys.stdout, flush=false)
```

* objects - value(s) to be printed
* sep - separator between the values
* end - it printed after all values are printed
* file - where the values are printed
* sys.stdout - screen

```python
print(1,2,3,4)
print(1,2,3,4,sep='*')
print(1,2,3,4,sep='#', end='&')
```

> 1 2 3 4

> 1*2*3*4

> 1#2#3#4&

#### Formatting - ```stg.format()```

```python
print('I love {0} and {1}'.format('bread', 'butter'))
print('I love {1} and {0}'.format('bread', 'butter'))
```

> I love bread and butter

> I love butter and bread

```python
print('Hello {name}, {greeting}'.format(gretting='good morning', name = 'John'))
```

> Hello John, Good morning

```python
x = 12.3456789
print('The value of x is %3.2f' %x)
print('The value of x is %3.4f' %x)
```

> The value of x is 12.35

> The value of x is 12.3457

### Input 

Sintax: `input([prompt])`, where prompt is the string we wish to display at the screen

```python
num = input('Enter a number.')
print(num)
```

> Enter a number: 10

> '10'

#### `Eval()`
It evaluate and executes expressions even if the provided input is a string

`int('2+3')`
> error

`eval('2+3')`
> 5

### Import

This basically works similar to other languages.

```python
import math
print(math.p)
```

> 3.141592653589793

We can also import only some attributes and functions

### Operators

* arithmetic operators
* logical operators
    * `and`, `or` and `not`
* assignment operators

### Bitwise operators

Act on operands as if they were string or binary digits. It operates bit by bit, hence the name.

* `&` AND
* `|` OR
* `~` NOT
* `^` XOR
* `>>` right shift
* `<<` left shift

```python
x = 10 (0000 1010)
y = 4 (0000 0100)

x & y = 0 (0000 0000)
x | y = 14 (0000 1110)
~ x = -11 (1111 0101)
x ^ y = 14 (0000 1110)
x >> 2 = 2 (0000 0010)
x << 2 = 40 (0010 1000)
```

### Special operators

#### Identity operators

* `is` and `is not`

Used to check if two values (or variables are located on the same part of the memory).
True if the operands are identical (refer to the same object)

```python
x1 = 5
y1 = 5
x2 = 'Hello'
y2 = 'Hello'
x3 = [1,2,3]
y3 = [1,2,3]
print(x1 is not y1)
print(x2 is y2)
print(x3 is y3)
```

> false

> true

> false

The interpreter locates the values.

#### Membership operators

Used to test wether a value or variable is found in a sequence (string, list, tuple, set and dictionry)

:warning: In a dictionry we can only test for presence of key, not the value

* `in` True if value/variable is found in the sequence
* `not in` True if value/variable is not found in the sequence

```python
x = 'Hello World'
y = {1 : 'a', 2 : 'b'}
print('H' in x)
print('hello' not in x)
print(1 in y)
print('a' in y)
```

> true

> true
Remember, python is case sensitive

> true

> false

### `if`, `else` and `elif` statement
The body of if statement is indicated by identation.
Python interprets non-zero values as true. None and 0 are interpreted as false.

```python
num = 3
if num > 0:
    print(num, "is a positive number.")
print("pineaple")
if num < 0:
    print("don't print this")
print("second pineaple")
```

> 3 is a positive number

> pineaple

> second pineaple

`elif` if a shortcut for `else if`

We can use nested statements, this follows the same rule of identation.

### `for` loop

```python
numbers = [6,5,3,8,4,2,5,4,11]
sum = 0
for val in numbers:
    sum = sum + val
print(sum)
```

### Range function
Generate a sequence of numbers

`range(10)` will generate numbers from 0 to 9 (10 numbers)

`range(start, stop, stepsize)` defining the start, stop and step size

This function does not store all the values in memory, it would be inefficient. So it remembers the start, stop and stepsize and generates the next number to go. To force this function to output all the items, wen can use the function list().

```python
print(range(10))
print(list(range(10)))
print(list(range(2, 8)))
print(list(range(2, 20, 3)))
```

> range(0, 10)

> [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

> [2, 3, 4, 5, 6, 7]

> [2, 5, 8, 11, 14, 17]

We can use range function in for loops to iterate through a sequence of numbers. It can be combined with `len()` function to iterate through a sequence using indexing.

```python
genre = ['pop', 'rock', 'jazz']
for i in range(len(genre)):
    print (genre[i])
```

> pop

> rock

> jazz

