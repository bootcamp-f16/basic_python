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

### Truthiness Exercises/Examples
```python
True and True
False and True
1 == 1 and 2 == 1
"test" == "test"
1 == 1 or 2 != 1
True and 1 == 1
False and 0 != 0
True or 1 == 1
"test" == "testing"
1 != 0 and 2 == 1
"test" != "testing"
"test" == 1
not (True and False)
not (1 == 1 and 0 != 1)
not (10 == 1 or 1000 == 1000)
not (1 != 10 or 3 == 4)
not ("testing" == "testing" and "Zed" == "Cool Guy")
1 == 1 and (not ("testing" == 1 or 1 == 0))
"chunky" == "bacon" and (not (3 == 4 or 3 == 3))
3 == 3 and (not ("testing" == "testing" or "Python" == "Fun"))
```

### Basic Ifs
```python
people = 20
cats = 30
dogs = 15

if people < cats:
    print "Too many cats! The world is doomed!"

if people > cats:
    print "Not many cats! The world is saved!"

if people < dogs:
    print "The world is drooled on!"

if people > dogs:
    print "The world is dry!"

dogs += 5

if people >= dogs:
    print "People are greater than or equal to dogs."

if people <= dogs:
    print "People are less than or equal to dogs."

if people == dogs:
    print "People are dogs."
```

### If & Elif
```python
people = 30
cars = 40
trucks = 15


if cars > people:
    print "We should take the cars."
elif cars < people:
    print "We should not take the cars."
else:
    print "We can't decide."

if trucks > cars:
    print "That's too many trucks."
elif trucks < cars:
    print "Maybe we could take the trucks."
else:
    print "We still can't decide."

if people > trucks:
    print "Alright, let's just take the trucks."
else:
    print "Fine, let's stay home then."
```

###Lists & Loops
```python
the_count = [1, 2, 3, 4, 5]
for number in the_count:
    print("This is count {}".format(number))
    
new_list = []
for i in range(0, 6):
    print("Adding {} to the list.".format(i))
    # append is a function that lists understand
    new_list.append(i)

print(new_list)
```


###While Loops
```python

i = 0
numbers = []

while i < 6:
    print("At the top i is {}".format(i))
    numbers.append(i)

    i = i + 1
    print "Numbers now: ", numbers
    print("At the bottom i is {}".format(i))


print "The numbers: "

for num in numbers:
    print num
```

###Manipulating Lists
```python
ten_things = "Apples Oranges Crows Telephone Light Sugar"

print "Wait there are not 10 things in that list. Let's fix that."

stuff = ten_things.split(' ')
more_stuff = ["Day", "Night", "Song", "Frisbee", "Corn", "Banana", "Girl", "Boy"]

while len(stuff) != 10:
    next_one = more_stuff.pop()
    print "Adding: ", next_one
    stuff.append(next_one)
    print("There are {} items now.".format(len(stuff))

print "There we go: ", stuff

print "Let's do some things with stuff."

print stuff[1]
print stuff[-1] # whoa! fancy
print stuff.pop()
print ' '.join(stuff) # what? cool!
print '#'.join(stuff[3:5]) # super stellar!
```

###Slice
```python
word = 'Python'
word[0]  # character in position 0
'P'

word[5]  # character in position 5
'n'

word[-1]
'n'

word[0:2]
'Py'

word[2:5]
'tho'

word[:2]  
'Py'

word[4:]
'on'

word[-2:]
'on'

word[::1]
'Python'

word[::-1]
'nohtyP'
```

### Dictionaries
```python
stuff = {'name': 'Zed', 'age': 39, 'height': 6 * 12 + 2}
print stuff['name']
print stuff['age']
print stuff['height']
stuff['city'] = "San Francisco"
print stuff['city']
stuff[1] = "Wow"
print stuff
del stuff['city']
print stuff
```

###Tuples
```python
 t = 12345, 54321, 'hello!'
 t[0] # 12345
 t # (12345, 54321, 'hello!')
 t[0] = 88888 # ERROR
```

###Learning to Speak Object Oriented
```
class
Tell Python to make a new type of thing.
```
```
object
Two meanings: the most basic type of thing, and any instance of some thing.
```
```
instance
What you get when you tell Python to create a class.
```
```
def
How you define a function inside a class.
```
```
self
Inside the functions in a class, self is a variable for the instance/object being accessed.
```
```
inheritance
The concept that one class can inherit traits from another class, much like you and your parents.
```
```
composition
The concept that a class can be composed of other classes as parts, much like how a car has wheels.
```
```
attribute
A property classes have that are from composition and are usually variables.
```
```
is-a
A phrase to say that something inherits from another, as in a "salmon" is-a "fish."
```
```
has-a
A phrase to say that something is composed of other things or has a trait, as in "a salmon has-a mouth."
```


###Basic Classes
```python
class Foo:
    def __init__(self, val):
        self.val = val
    def printVal(self):
        print(self.val)
        
obj1 = Foo(1)
obj2 = Foo(2)
print(obj1.printVal())
print(obj2.printVal())
```
