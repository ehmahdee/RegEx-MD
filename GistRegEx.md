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

Sections of the expression can be grouped using brackets (`[]`) and parentheses (`()`). This allows the segments to be repeated or edited as a whole portion. The section of `([a-z0-9_\.-]+)` is a grouped construct. 

### Bracket Expressions

Bracket expressions can be used to find and match an individual character from a set. `{2,6}` is a bracket expression that matches 2 to 6 chracters from the preceding set `[a-z\.]`.

### Character Classes

Character classes, like bracket expressions, can be used to match a character from a set. For example `[a-z0-9_\.-]` would match any lowercase letter, number, underscores, dot, or hyphen in the username.
the `\d` is a shorthand that can be used to match any digit.

### The OR Operator

Typically a pipe symbol (`|`) is used as an OR operator. However, in this expression can be OR created by the use of brackets (`[]`) and paretheses. Everything in this expression that is between brackets can be used to create an OR by using a few characters to create a range. The section of `[a-z\.]` denotes that the TLD can contain any letter a through z and/or a `.`. Using both of these tools, you are able to effectively group and compare parts of the expression.

### Character Escapes

Character escapes are used to match special characters that have specific meanings in regular expressions. the backslash `\` in `\.` is used to escape the dot so the expression knows that we're targeting the dot specifically and not the dot's purpose. Other character escapes like `\d` matches any digit.

## Author

Emma Daily is a junior fullstack developer based in Los Angeles. After making the switch from the film industry to programming, she's excited to tackle new creative challenges.

If you have any questions, please email Emma at edaily94@gmail.com or visit her [GitHub profile](https://github.com/ehmahdee) to see her other projects.
