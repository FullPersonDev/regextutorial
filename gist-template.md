# Title: Matching an Email

This tutorial will explain the regular expression, regex for short, to match email addresses.

## Summary

I will describe the regex that helps us validate email addresses by ensuring the provided input follows a set pattern.  I will explain the different parts of the regex, its components, anchors, quantifiers, grouping constructs, bracket expressions, character classes, the OR operator, flags, and character escapes.  Here is a code snipet of our email address regex:

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

## Table of Contents

- [Regex Components](#regex-components)
- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

The regex has the following components and each one of these plays a role in defining the pattern for the regex:
- Literals --> @ and .
- Character Classes --> a-z which is characters a to z; 0-9 which is numbers 0 to 9; and special characters _, `\`, ., -
- Quantifiers --> + and {2,6}
- Grouping Constructs --> ( )
- Anchors --> ^ and `$`

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

### Anchors

The characters ^ and `$` are considered the anchors.  The ^ anchor marks the begining of the string and the `$` signifies the end of the string.  This is why we see the ^ character at the begining and the `$` character at the end of the expression.  These anchors ensure that the regex matches the whole string from begining to end, conforming exactly to the pattern defined.

### Quantifiers

We have a couple of quantifiers in this regex.  The + sign and the {2,6}, let's talk about each one of them and what they mean.  The + sign in the regex means that it matches one or more of the precededing element.  The numbers inside the curly brackets {2,6} establishes the mininum and maximum characters allowed.  In this regex, in the {2,6}, the 2 means that the string must be at least 2 characters long.  The 6, in the {2,6}, means that the string must be no more than 6 characters long.

### Grouping Constructs

We can use parenthesis () to group together parts of the regex when working with more complex regex.  In our case of email regex we see this 3 different times.  First we are checking the user part of the email with `([a-z0-9_\.-]+)`.  Second we are checking the domain of the email with `([\da-z\.-]+)`.  Third we are checking the text after the email domain and period with `([a-z\.]{2,6})`.

### Bracket Expressions

The bracket expressions are used to encapsulate the set of characters that we want to use to match.  The bracket expressions `[a-z0-9_\.-]`, `[\da-z\.-]`, and `[a-z\.]` are our examples that establish the set of characters that we want to match.

### Character Classes

A character class in a regex defines a set of characters, they can occur in the string in any way to match. `\d` matches any numerical digit, this class is equivalent to the bracket expression [0-9].

### The OR Operator

We don't use an OR operator in our regex.  But if we were to use one this is the character for it (|).  If we were to use the OR operator in our regex it could look like this `/^([a-z|0-9|_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` to say we want to match either a-z or 0-9 or the special characters.

### Flags

Our regex does not use flags within the pattern.  Flags are typically added outside the closing delimiter and affter the overall behavior of the regex.

### Character Escapes

The dot '.' is a special character in regex notation.  To match a literal dot in our regex, we need to use a backslash `\`.  This is known as an escaped character.  It is escaped with the backslash; which then ends up lookingn like this `\.`, this will match a literal dot.

## Author

Martin Aguero
Github Profile Link: https://github.com/FullPersonDev
Github Repo Link: https://github.com/FullPersonDev/regextutorial
