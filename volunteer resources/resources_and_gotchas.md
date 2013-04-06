Volunteer resources
===================

##Refreshing your python skills

[Learn Python the Hard Way](http://learnpythonthehardway.org/)

[Introduction to Computer Science 101](https://www.udacity.com/course/cs101)

[Codecademy python track](http://www.codecademy.com/tracks/python)



## Python Cheat Sheets

Good for quickly getting up to speed with common Python code structure and data types:

[Python Cheat Sheet](http://www.cogsci.rpi.edu/~destem/gamedev/python.pdf)

[Annotated Simple Python Program](http://www.pythonforbeginners.com/wp-content/uploads/2012/10/python_cheatsheet1.png)

##Python gotchas

As a friend put it:

"The problem is that python is good, except where it does stupid things. Python programmers mostly trip over the stupid things fairly quickly, right themselves, and work around them forever, and forget that they are stupid." – Aquarion


    1. Tuples are immutable.
    2. Case Matters.
    3. Integer division trucates. (__import__ future, float cast)
    4. Classes have to inherit object to be derivable from.
    5. Type of bracket plethora-rama.
    6. Unicode.
    7. List string concatenation with .join().
    8. Shallow copies of dicts (.deepcopy())
    9. Default arguments in Python (dragons).
    10. Tabs vs Spaces.
    11. == vs is.
    12. Dictionaries are unordered.
    13. Scope, particularly scope in loops.

##Common errors confusing to beginners

###  "invalid syntax" on valid syntax

Often you'll see an error like this:

```python
  File "test.py", line 5
    print "hello"    
        ^
SyntaxError: invalid syntax
```

Which is confusing because the statement looks perfectly okay. The error is often with the previous line which was syntactically complete (typically either mismatched brackets or an if statement missing a ":") such as the following:

```python
count = (1   #missing closing bracket
print "hello"
```

```python
if count == 1 # missing ":" 
    print "hello"
```

### TypeError: 'str' object does not support item assignment

```python
>>> a = 'hello vorld'
>>> a[6]='w'
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'str' object does not support item assignment
```

Python strings are immutable, so once created they can't be changed. If you want to change their content you need to create a new string.

```python
>>> a[:6] + 'w' + a[7:]
'hello world'
```

### TypeError: cannot concatenate 'str' and 'int' objects

```python
>>> count = 20
>>> "count " + count
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: cannot concatenate 'str' and 'int' objects
```

If you want to concatenate non-string items to a string you need to convert them to strings first. The way to get the standard string representation of an object is to use the str() function:

```python
>>> "count " + str(count)
```
