# Regex Tutorial Homework 17.

## Introductory paragraph

This is my homework-17 writing about Regex expressions.  
I had an option of choosing between: Matching a hex value, Matching an email, Matching a URL, matching an HTML tag.  
I have decided to explain and give tutorials on how to match an Email address using Regular expression.

## Summary

According to MDN, "Regular expressions are patterns used to match character combination in strings. In JavaScript, regular expressions are also objects. These pattersn are used with the exec() and test() methods of RegExp, and witht he match(), matchAll(), replace(), replaceAll(), search(), and split() methods of String.

Email matching regex. This is what I'll be using to do this HW.

`Matching an Email: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

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

According to rexegg.com, it defines anchors as following: "Anchors belong to the family of regex tokens that don't match any characters, but that assert something about the string or the matching process. Anchors assert that the engine's current position in the string matches a well-determined location: for instance, the beginning of the string, or the end of a line."

Anchors represent a position at the beginning and at the end of the text. In this case, it would be `^` and `$`.

    ^ is the anchor at the beginning of input.
    $ is the end of the input.

The rest of the code inside the opening and closing anchors is where the action happens (Matching email address).

### Quantifiers

According to MDN, quantifiers is defined as "Indicate numbers of characters or expressions to match. In our email matching case, the quantifier in this regex includes the + operator.  
The + operator will connect useers email name + email domain/address + .com.

Additional quantifier in this example is {2,6}. This quanitifer lets match range of 2 - 6 characters for the character set of [a-z\.].

`Matching an Email: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
