# Week-17-Challenge

This is my week 17 challenge where I explain email regex code.

# RegEx
RegEx stands for regular expression. Simply put by the people at thisdot.co, RegEx are "a set of characters which are used to create patterns that can be used to search, find, replace, or validate text." RegEx characters are usable in all languages (with some characters not being available to use in some languages.)

# Summary

The RegEx I will be describing is the following: ^\w+([.-]?\w+)@\w+([.-]?\w+)(.\w{2,3})+$ This is what a RegEx would look like that matches an email address. It follows the format of an email address and includes character classes to stand for periods, hyphens, and other special characters that may be found in usernames.

Table of Contents
Anchors
Quantifiers
Grouping Constructs
Bracket Expressions
Character Classes
The OR Operator
Flags
Character Escapes
Regex Components
# Anchors
Anchors point at the start and end of a string or line of code. ^ is typically used to start the code and $ to end it. You can see this in the snippet above.

# Quantifiers
Quantifiers help specify amounts of special characters that must be matched. The + quantifier allows one to match 1+ character repetitions. The * allows to match 0+ occurrences. Examples: cat, caat, caaat, caaaaaaaaaaaaaaat, etc (adding infinite amounts of a's but having one minimum) can be described as "ca+t". "ct" will not be matched by "ca+t" because it requires a minimum of one a prior to matching. "ca*t" would match all of those as well as the "ct" due to it being 0+ matching. Other quantifiers used include ? for 0-1 occurrences before the following characters, {n} would be exact number (whatever the value of n is) of occurrences prior, {n,} would be n or more, and {n,m} would be the low and high ends of the allowed occurrences.

# Grouping Constructs
Grouping constructs allow one to group parts of RegEx together and apply quantifiers to them intead of specific characters. The two most used constructs are parentheses and non-capturing parentheses. () group them together and basically makes anything inside the parentheses into the equivalent of one character for example, instead of writing a+b+c+ you would simply need to write (abc)+. The non capturing parentheses looks a little different. In adding a question mark and a colon, as so (?:), you are essentially doing the same thing as the parentheses but not making it a group. This is primarily used for applying a quantifier for anything inside of it but not the whole thing necessarily. Other grouping constructs include square brackets to create character classes for single occurrences and curly braces to specify an exact amount of repeated occurences for example, a{6} would match 6 as but no more and no less.

# Bracket Expressions
As stated before, it just means that it is looking for occurrences of anything within the brackets. [abc] would look for occurences of a, b, or c and [0-9] would look for any occurrences of any number between 0 and 9.

# Character Classes
Character classes are what were stated in the previous example for the number. [a-z] looks for any character between a and z.

# The OR Operator
The OR Operator in regex is the | symbol. It is used to match one expression or another depending on what you put, for example, if one were to use it to make apples|oranges, it would match to either apples or oranges. Another good example is writing (apples|oranges). This will match either apples or oranges.

# Flags
Flags are modifiers that are added at the end of a RegEx to change how the matching works. They're written as a single letter after a /. A good example of this is the /i. Writing /hello/i would match all variations of "hello" including Hello, HELLO, hello, etc.

# Character Escapes
Character escapes are ways to show special characters or patterns as a single character. They're symbolized by a backslash \ followed by a character depending on what you are looking to do. \n would be newline, \r is a return, etc.

# Author
Author: Gustavo Rivera Github: https://github.com/IvaTheKing
