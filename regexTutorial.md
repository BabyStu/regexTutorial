# Regex Email Matching
Regular expressions are tools for working with text patterns. This tutorial will cover how to create a regex for matching an email.

## Summary

This tutorial will cover each component of the regex, and provide snippets and examples to demonstrate its usage.

This is the email matching pattern:
```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```
## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Character Classes](#character-classes)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

Anchors are used to mark specific positions of the string. The email regex starts with ^ and ends with $, so the entire string is covered.

### Quantifiers

A quantifier determines the number of times a character can be repeated. In the email regex, it uses + and {2,6}. The + means 1 or more characters must be used, and the latter means 2-6 characters. 

```
([a-z0-9_\.-]+)
```
This snippet, could match c.hansen, but not c..hansen, because there must be a matching character between the 2 dots.

```
([a-z\.]{2,6})
```
 This snippet, is able to match ".com" because it is searching for a string of 2-6 characters and accepts letters and periods.

### Grouping Constructs

Parentheses create groups within the pattern. In the email pattern, they're used to separate each part of the email address.

```
([a-z0-9_\.-]+)
```

The above snippet of the email pattern groups the username part of the email.

```
([\da-z\.-]+)
```

This snippet is grouping the domain.

### Character Classes

Character classes are what defines the specific set of characters for matching.

```
[a-z0-9_\.-]
```
In this snippet the class matches: lowercase letters, numbers, underscores, periods, and hyphens. 

### Character Escapes

Character escapes are meant to match special characters (such as but not limited to: \^ , \$ , \| ). The email pattern uses $ and ^ but not as escapes because they're being used to mark the start and end. 

Unfortunately, none of the other special characters in this are used for escaping either

## Author

Written by: Steve Weede

@Github: [BabyStu](https://github.com/BabyStu)


