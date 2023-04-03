# Regex Tutorial

A regex is short for regular expression and a sequence of characters that defines a specific search pattern. When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string. They are also frequently used to validate input.

## Summary

Here I would like to match email that has been converted to regex, so that I can find email in the text editor.

Matching Email: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

This looks like just a list of symbols, but each one has a meaning.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

The first thing seen in the matching email snippet above is ^. This means beginning so it means email should start with ([a-z0-9_\.-]+) expression. If it’s ^The, it searches any strings that start with The.

The last thing seen is $. It means end, so email should end with ([a-z\.]{2,6}) expression. If it’s end$, it searches any strings that end with end.


### Quantifiers

* is one or more - cde* means cde followed by zero e to more e
+ is one or more - same as above
? is zero or one - cde? means it does not matter if e is contained or not, it matches both cd and cde
{} - if cde{2}, cdee matches.


### Grouping Constructs

() means to create a capturing group. For example, if c(ba), only cba matches. It does not matter if it is in the middle of a string like fdsdcbasfdsf.

?: means to disable a capturing group. When a(?:bc), both abc and a match.

### Bracket Expressions

[] means it matches anything contained in brackets. [abc] matches a, b and c. It is the same expression as a|b|c

[a-c] is the same expression as above.

[a-fA-F0-9] matches any letter from a to f, A to F and 0 to 9).

[^a-zA-Z] matches any letter without a to z and A to Z.

### Character Classes

Character classes are used to distinguish between the different types of characters being searched. This is can be used to diferentiate between letters and integers.

" \ " : These distinguish between the type of character being serached. \d searches for digits, while \D searches everything except for digits. \w searches for all alphanumeric characters, while \W searches for all non-alphanumeric characters (such as $).
" . " : Matches every single character, with the exception of line terminators: \n, \r, \u2028, and \u2029. These are like wildcards. eg. /b.d/ will match 'bid', 'bod', 'bed', 'bad', etc.

### The OR Operator

The OR operator ' | ' was previously defined as a type of grouping construct. Using the OR operator in ^a|b$|c* will match every instance of 'a' starting a string, every 'b' at the end of a string, or all instances of 'c'.

### Flags

Flag is / and it means to create a regex between the slashes. As it is seen at the beginning and the end in the example of matching email regex, the flag is also seen in the search bar when you want to search for a regex.

/g means global search and dot return after the first search.

### Character Escapes

You probably remember seeing ' \ ' previously? This is also way to 'escape' a character. Is used to match 'literally', and allows a previous special charater 'escape' it's usual defined operation. eg. /b*/ finds all occurances of 'b' but what if I was looking for the combo of 'b*'? I would change the expression be adding the escape to /b\*/ allowing us to find the literal "b*"

## Author

Created by SIU TSANG | [SIU TSANG-GitHub](https://github.com/SiuTsang?tab=repositories)
