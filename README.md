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

In our email matching regex expression, you can divide the "sequence" into 3 groups.

    Group #1: [a-z0-9_\.-]+) || This first group will match the user's email name before @ domain address.
    Group #2: [\da-z\.-] || This second group will match the user's email domain or service they are using; such as @google or @yahoo
    Group #3: [a-z\.]{2,6}. || This third will cover the ending of an email address; such as ".com or .net, etc..."

### Bracket Expressions

Bracket expressions is defined as following:  
"A bracket expression is either a matching list expression or a non matching list expression. It consists of one or more expressions: ordinary characters, collating elements, collating symbols, equivalence classes, character classes, or range expressions."

Bracket expressions for this code:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

In our email matching regex expression, Bracket expression includes the following character set `[a-z0-9_\.-]. This is matching any letter a-z (case sensitive) and numbers 0-9 and matches the characters "\_", ".", "."

The [\da-z\.-], this is matching any character a-z (case sensitive) and numbers from 0-9, and characters ".", and "-".

The [a-z\.] matches any characters a-z (case sensitive) and the "." character.

### Character Classes

Character classes ensures that a given sequence of characters matches a larger set of characters.

\*\*\*The character class in this expression is \d, which matches a single characters that is a digit from 0-9. It will only match a single digit such as "4", but not "44".

### The OR Operator

The OR operator in regex is used by the pipe "|". It will match expressions that come before and after in the code, however this is not the case in our email matching code.

### Flags

According to Javascript.info they defined patterns and flags as following:  
"Regular expressions are patterns that provide a powerful way to search and replace in text. In Javascript, they are available via the RegExp object, as well as being intergrated in methods of strings." Also it states that 6 flags are available in Javascript.

i
With this flag the search is case-insensitive: no difference between A and a (see the example below).

g
With this flag the search looks for all matches, without it – only the first match is returned.

m
Multiline mode (covered in the chapter Multiline mode of anchors ^ $, flag "m").

s
Enables “dotall” mode, that allows a dot . to match newline character \n (covered in the chapter Character classes).

u
Enables full Unicode support. The flag enables correct processing of surrogate pairs. More about that in the chapter Unicode: flag "u" and class \p{...}.

y
“Sticky” mode: searching at the exact position in the text (covered in the chapter Sticky flag "y", searching at position)

However in our code, no flags were used in email matching regex example.

### Character Escapes

The backslash in a regular expression precedes a literal character. You also escape certain letters that represent common character classes, such as `\w` for a word character or `\s` for a space.

Character escape was not used in email regex example.

## Author

Jung Nam

### https://gist.github.com/jung0808/015f5876080d8e8279dded154904410f

### https://github.com/jung0808/homework-17-regex-tutorial
