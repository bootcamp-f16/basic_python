# basic_python


#Shell Based Examples

###Print
```python
print "Hello World!"
```

###Math
* + plus
* - minus
* / slash
* * asterisk
* % percent
* < less-than
* > greater-than
* <= less-than-equal
* >= greater-than-equal


### Formatted Printing
```python
name = 'Zed A. Shaw'
height = 74 # inches

print "He's %d inches tall." % height
print "Let's talk about %s." % name
print("His name is {} and his height is {}".format(name, height))
```


###Iput
```python
name = input("What is your name?" )
print(name)
```


### Defining Functions
```python
def print_none():
    print "I got nothin'."
    
def print_one(arg1):
    print "arg1: %r" % arg1
    
def print_two(arg1, arg2):
    print "arg1: %r, arg2: %r" % (arg1, arg2)

def print_two_again(*args):
    arg1, arg2 = args
    print "arg1: %r, arg2: %r" % (arg1, arg2)

print_none()
print_one("First!")
print_two("Zed","Shaw")
print_two_again("Zed","Shaw")
```


### Functions can return something

```python
def add(a, b):
    print("ADDING {} + {}").format(a, b))
    return a + b

def subtract(a, b):
    print("SUBTRACTING {} - {}").format(a, b))
    return a - b

def multiply(a, b):
    print("MULTIPLYING {} * {}").format(a, b))
    return a * b

def divide(a, b):
    print("DIVIDING {} / {}").format(a, b))
    return a / b


print "Let's do some math with just functions!"

age = add(30, 5)
height = subtract(78, 4)
weight = multiply(90, 2)
iq = divide(100, 2)

print("Age: {}, Height: {}, Weight: {}, IQ: {}").format(age, height, weight, iq))


# A puzzle for the extra credit, type it in anyway.
print "Here is a puzzle."

what = add(age, subtract(height, multiply(weight, divide(iq, 2))))

print "That becomes: ", what, "Can you do it by hand?"
```

###Calling Functions
```python
def break_words(stuff):
    """This function will break up words for us."""
    words = stuff.split(' ')
    return words

def sort_words(words):
    """Sorts the words."""
    return sorted(words)

def print_first_word(words):
    """Prints the first word after popping it off."""
    word = words.pop(0)
    print word

def print_last_word(words):
    """Prints the last word after popping it off."""
    word = words.pop(-1)
    print word

def sort_sentence(sentence):
    """Takes in a full sentence and returns the sorted words."""
    words = break_words(sentence)
    return sort_words(words)

def print_first_and_last(sentence):
    """Prints the first and last words of the sentence."""
    words = break_words(sentence)
    print_first_word(words)
    print_last_word(words)

def print_first_and_last_sorted(sentence):
    """Sorts the words then prints the first and last one."""
    words = sort_sentence(sentence)
    print_first_word(words)
    print_last_word(words)
```

### Truthiness
* and
* or
* not
* != (not equal)
* == (equal)
* >= (greater-than-equal)
* <= (less-than-equal)
* True
* False


NOT |	True?
--- | --- 
not False | True
not True |	False

OR | True?
--- | --- 
True or False	| True
True or True	| True
False or True	| True
False or False |	False

AND	| True?
--- | --- 
True and False | False
True and True	| True
False and True	| False
False and False	| False

NOT OR | True?
--- | --- 
not (True or False)	| False
not (True or True)	| False
not (False or True)	| False
not (False or False)	| True

NOT AND	| True?
--- | --- 
not (True and False)	| True
not (True and True)	| False
not (False and True)	| True
not (False and False)	| True

!=	| True?
--- | --- 
1 != 0	| True
1 != 1	| False
0 != 1	| True
0 != 0	| False

==	| True?
--- | --- 
1 == 0	| False
1 == 1	| True
0 == 1	| False
0 == 0	| True

