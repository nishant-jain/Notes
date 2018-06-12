- Created by Guido Van Rossum in the early 1990s
- Guide for python 3
- Python Interpreter
- Interpreted language - Interpreter receives a command, evaluates it, and then reports the result of the command. Compilation doesn’t happen.
- .py suffix for python files
- Syntax relies on whitespaces and indentations
- Comments - # this is a comment

###Objects in Python

- Object oriented language and classes form the basis of all types

#####Identifiers, objects and assignment statements

- Identifiers - Variables in other languages
- temperature = 98.6
- Temperature is the identifier
- Mapped to object(98.6)
- Case sensitive, can’t begin with a number
- Similar to a pointer in C
- Associated with the memory address of the object which it refers
- Can be assigned to “None” object(similar to null in JS)
- Dynamically typed(unlike java/C++) - no advance association of identifier with a data type
- Objects on the other hand, have a definite type (98.6 is float)
- Alias - associating another identifier to existing object (temp = 98.6. Temp and temperature both point to 98.6 now)
- Assignment by reference, so changes to one alias reflect in the next
- Although if assignment done again via = operator, the alias breaks 
- Ex - temperature = temperature + 5 
- New values: Temp -> 98.6, and temperature -> 103.6

#####Creating and using objects

- Instantiation - process of creating a new instance
- By invoking the constructor of the class (Widget() for class Widget)
- Or by literal form (temp = 98.6 for floats, “98.6” new instance of the float )
- Or functions which return a new instance of a class (for ex- sorted())
- Syntax for calling methods - either use sorted(data) (where data is passed as a param) or data.sorted() (member functions) 
- Accessors - similar to getters 
- Mutators - similar to setters

#####Python’s built-In classes

Immutable classes - classes whose values are fixed upon instantiation and cannot be changed subsequently. Ex- float
Bool, int, float, list, tuple, str, set, frozenset, dict
Most of them support literal forms of initialization(like 98.6) and all of them support traditional constructors
Bool Class
Takes values True or False
Default constructor : bool() - returns False
bool(string) - returns False if empty
bool(number) - returns False if 0
Int Class
Numeric type
Chooses internal representations according to the magnitude of the value
 Default constructor - int() returns 0
Can also be used to typecast from other types
“3” will be converted to 3, if passed as param to int
For base conversion, use int(num, base) ( ex- int(‘7f’, 16) evaluates to 127)
Float class
Floating point, fixed precision representation
Precision like double in java/c++
Default constructor - float() returns 0.0
“3.14” will change to 3.14 float value
Sequence types: list, tuple, and string
Collection of values where order is significant
No concept of char type(like java/c++), ‘c’ is just string with length 1
List Class
Stores sequence of objects
Referential structure - stores a sequence of references to its elements
Can have different types of objects - [1, ‘two’, None] is a valid list
Zero indexed, and are like arrays
Can dynamically increase and decrease in size
[] - empty list
Constructor list() - produces empty list
list(‘hello’) - produces [‘h’,’e’,’l’,’l’,’o’]
Tuple class
Immutable sequence
() - empty tuple
One element tuple - (17,) [because (17) will be taken as a paranthesized numeric expression]
Str class
Immutable sequence of characters
Unicode
Supports both single and double quotes
Use backslash to escape
Triple quotes can be used for multiline strings, no need to escape newlines
“Hello”, ‘hello’, ‘’’hello’’’, “””hello””” - all are valid strings
Set and frozenset class
Collection of elements, without duplicates, and without order
Based on hash tables
O(1) lookups for finding membership of keys
No order maintained
Only immutable types can be added to set
Set of sets and set of lists are not allowed
Frozenset - immutable form of set class
{17}, {‘red’, ‘green’, ‘blue’} are valid sets
{} - does not represent empty set, but represents an empty dictionary(historical reasons)
Default constructor - set() produces an empty set, expects an iterable as input
set('hello') produces set(['h', 'e', 'l', 'o'])
Dict class
Represents dictionary/mapping, key to value map
{} - represents empty dictionary
{‘a’:1, ‘b’:2} - valid dictionary
dict(pairs) with pairs = [( ga , Irish ), ( de , German )] can be used to generate dict

#####Expressions, operators, and precedence
Logical operators
not, and, or
‘and’ and ‘or’ operators short circuit
Equality operators
‘is’ same identity
Evaluates to True only if a and b are aliases for the same object 
‘is not’  different identity 
‘==’  equivalent
Gives true for different objects with values that are deemed equivalent
‘!=’ not equivalent
Comparison operators
< , > , <= , >=
Arithmetic operators
+, -, *, /, //, %
/ - true division
// - integer division
Python supports the pair of operators // and % to perform the integral calculations, with expression 27 // 4 evaluating to int value 6 (the mathematical floor of the quotient), and expression 27 % 4 evaluating to int value 3, the remainder of the integer division
Bitwise operators

For the rest, read chapter 1. This is too tedious and too basic.
This is till section 1.3 of the book “Data structures and algorithms in python” by goodrich, tamassia and goldwasser. Will add stuff to tech notes which is something I don’t know/or find really important.
