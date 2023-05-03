# RegEx-MD

In the following gist I will break down and describe components to match an email in a regex. 

## Summary

The regular expression ```/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/``` matches an email address that consists of a username followed by an "@" symbol, a domain name, and a TLD part. A TLD is short for Top-Level domain and denotes the type of organization the domain belongs to. These include ".com", ".edu", or ".org". 
The username can be any combination of lowercase letters, numbers, underscores, dots, and hyphens.

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

The caret (`^`) achor signifies the beginning of the string. It helps to identify the pattern needed (the username) appears at the start of the regular expression. 
The dollar sign (`$`) anchor ends the string. It ensures that the TLD is the last part in the string and no other characters are included in the expression.
These anchors force the expression to match the string from beginning to end. 

### Quantifiers
 
 There are a couple of quantifiers in this expression. The plus sign expression (`+`) is used to match one or more characters in the username and domain within the email address. In `([a-z0-9_\.-]+) ` the username or domain name can contain any combinations of these characters.
 The range quantifier `{2,6}` is used to match 2 to 6 characters in the TLD. The TLD can have any combination of lowercase letters as long as it is within 2 to 6 characters.

### Grouping Constructs



### Bracket Expressions

### Character Classes

### The OR Operator



### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
