Checking a Character is a vowel or consonant in Python
Here, in this section we will discuss the program to check the entered character is a vowel or consonant in python. In Python string is an array representation of Characters python does not have a character data type. A single character is a string of length [1].
Vowels:- A character is considered as a vowel when it belongs to the set of characters like { ‘A’ , ‘E’ , ‘I’ , ‘O’ , ‘U’ }

Character is a vowel or consonant in C

Working:-
Take character input from the user
Check if Input is a lowercase of upper case vowel
If yes then print vowel
If not then print consonant
Can also additional check if it’s a non-character item
We will discuss various methods to do the same thing.

C++ program to check whether Character is a vowel or consonant
Method 1
Now in here we will see how we can identify whether a character is a vowel or consonant using the Java programming language.
Python Code
Run
c = 'a'

# checking for vowels
if c == 'a' or c == 'e' or c == 'i' or c == 'o' or c == 'u' or c == 'A' or c == 'E' or c == 'I' or c == 'O' or c == 'U':
    print(c, "is a vowel")  # condition true input is vowel
else:
    print(c, "is a consonant")  # condition true input is consonant
Output
a is a vowel
Related Pages
Juggling algorithm for array rotation
 
Balanced Parenthesis Problem
 
Check whether a character is a alphabet or not

Find the ASCII value of a character

Length of the string without using strlen() function

Method 2
The issue with the previous method was that we were not checking if the user entered a non-alphabet character like ‘3’ or ‘%’ etc. We will see an alternate approach and also handle this non-alphabet case.
Python Code
Run
def isLowercaseVowel(c):
    # returns 1 if char matches any of below
    return c == 'a' or c == 'e' or c == 'i' or c == 'o' or c == 'u'


def isUppercaseVowel(c):
    # returns 1 if char matches any of below
    return c == 'A' or c == 'E' or c == 'I' or c == 'O' or c == 'U'


c ='f'

# show error message if c is not an alphabet
if not c.isalpha():
    print("Non alphabet")
elif isLowercaseVowel(c) or isUppercaseVowel(c):
    print(c, "is a Vowel")
else:
    print(c, "is a consonant")
Output
f is a consonant
Method 3
The above method has two separate functions of upper case vowels and lowercase vowels we can reduce that down to one single method using an inbuilt function that converts any lowercase case charter to uppercase.
Python Code
Run
# single function for both uppercase and lowercase
def isVowel(c):
    # converts to uppercase if it wasn't already
    c=c.upper()
    # returns true if char matches any of below
    return c == 'A' or c == 'E' or c == 'I' or c == 'O' or c == 'U'


c = 'f'

# show error message if c is not an alphabet
if not c.isalpha():
    print("Non alphabet")
elif isVowel(c):
    print(c, "is a Vowel")
else:
    print(c, "is a consonant")
Output
f is a consonant
