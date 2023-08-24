# Regex Tutorial by YggdrasilJL

In this tutorial, you will learn more about how the components of regular expressions work.

<a id="regex"></a>

For example, here is a regular expression to validate a password:

```js
const passwordRegex =
  /(?=(.*[0-9]))(?=.*[\!@#$%^&*()\\[\]{}\-_+=~`|:;"'<>,./?])(?=.*[a-z])(?=(.*[A-Z]))(?=(.*)).{8,}/;
```

That regex checks for a complex password with at least 8 characters, at least 1 number, at least 1 uppercase letter, at least 1 lowercase letter, and at least 1 special character.

## Summary

Regular expressions are used in many applications, commonly in web development for checking user input, For example, you can use regular expressions to validate email addresses, phone numbers, and URLs. This tutorial will teach you how to use regular expressions in JavaScript.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors

Anchors are used to match the beginning or end of a string. The most common anchors are ^ and $.

This is not necessary in the regex [above](#regex) because its designed to check if a string meets specific criteria so it doesn't need to be interested in where the string starts or ends.

### Quantifiers

Regex quantifiers are used to check how many times you should match a character or group. 

Here is a list of quantifiers:

    * (Asterisk)

> Matches zero or more occurrences.

    + (Plus):
    
> Matches one or more occurrences.

    ? (Question Mark)

> Matches zero or one occurrence.

    {n}:

> Matches exactly n occurrences.

    {n, m}:

> Matches between n and m occurrences.


### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

I am currently in a full-stack web development bootcamp, my goal is to become a front-end engineer. I love learning new things and sharing them with others. Thank you for reading!

- [My GitHub](https://github.com/yggdrasiljl)
