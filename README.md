# Regular Expressions Tutorial by YggdrasilJL

In this tutorial, you will learn more about how the components of regular expressions work.

<a id='regex'></a>

For example, here is a regular expression to validate a password:

```js
const passwordRegex =
  /(?=(.*[0-9]))(?=.*[\!@#$%^&*()\\[\]{}\-_+=~`|:;''<>,./?])(?=.*[a-z])(?=(.*[A-Z]))(?=(.*)).{8,}/;
```

That regex checks for a complex password with at least 8 characters, at least 1 number, at least 1 uppercase letter, at least 1 lowercase letter, and at least 1 special character.

## Summary

Regular expressions are used in many applications, commonly in web development for checking user input, for example, you can use regular expressions to validate email addresses, phone numbers, and URLs. This tutorial will teach you about the individual components of regular expressions.

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

## More Practical Examples

### Phone Number Format
---
```js
const phoneNumberRegex = /^(\d{3})-(\d{3})-(\d{4})$/;
```

### Email Format
---
```js
const emailRegex = /^([a-zA-Z0-9_\-\.]+)@([a-zA-Z0-9_\-\.]+)\.([a-zA-Z]{2,5})$/;
```

## Regex Components

### Anchors
---
Anchors are used to match the beginning or end of a string. The most common anchors are ^ and $.
```js
// Match a string that starts with 'Hello'
const startsWithHello = /^Hello/;

// Match a string that ends with 'World'
const endsWithWorld = /World$/;
```
This is not necessary in the regex [above](#regex) because its designed to check if a string meets specific criteria so it doesn't need to be interested in where the string starts or ends.

### Quantifiers
---
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

> Matches between n and m occurrences, {8,} is used in the regex [above](#regex) (matches 8 or more occurrences).

### OR Operator
---
The OR operator <span style='color: #cd5c5c;'>**|**</span> is used to check if one of the conditions is met, very similar to the OR operator in JavaScript.

#### For example:

In the regex [above](#regex), it is used to match special characters, Shown here:

```
[\!@#$%^&*()\\[\]{}\-_+=~`|:;''<>,./?]
```

### Character Classes
---
Character classes are used to check if a character matches a specific set of characters. In the regex [above](#regex), it is used to matches any uppercase letter <span style='color: lightgreen;'>[A-Z]</span>, lowercase letter <span style='color: lightgreen;'>[a-z]</span>, or number <span style='color: lightgreen;'>[0-9]</span>.

### Flags
---
Flags are used to modify the behavior of a regex. Here is a list of some flags:

g – Global, match more than once

m – Force $ and ^ to match each newline individually

i – Make the regex case insensitive

s – Make the regex dot match newline

```js
// Match all occurrences of 'tree' in a case-insensitive manner
const treeRegex = /tree/gi;
```

There is no flags used in the regex [above](#regex), meaning it uses the default behavior.

### Grouping and Capturing
---
Parentheses <span style='color: lightgreen;'>(...)</span> are used to group parts of a expression together, seen in the regex [above](#regex).

### Bracket Expressions
---
Bracket expressions <span style='color: lightgreen;'>[...]</span> are used to specify a range of characters, seen in the regex [above](#regex).

### Greedy and Lazy Match
---
Greedy quantifiers <span style='color: lightgreen;'> (\*, +, {})</span> are used to match as many characters as possible, seen in the regex [above](#regex).

Lazy quantifiers <span style='color: lightgreen;'>(\*?, +?, {n, m}?)</span> are used to match as few characters as possible, there is no example of this used in the regex [above](#regex).

```js
// Greedy match: Matches the LONGEST string that starts with 'a' and ends with 'b'
const greedyMatch = /a.*b/;

// Lazy match: Matches the SHORTEST string that starts with 'a' and ends with 'b'
const lazyMatch = /a.*?b/;

```

### Boundaries
---
Boundaries <span style='color: lightgreen;'>\b</span> are used to specify where a regex should match,

```js
// Match "cat" as a whole word
const treesWholeWord = /\btrees\b/;
```

there is no example of this used in the regex [above](#regex).

### Back-references
---
Back-references <span style='color: lightgreen;'>(\1, \2, ...)</span> are used to match a specific group,

```js

```

there is no example of this used in the regex [above](#regex).

### Look-ahead and Look-behind
---
Look-ahead <span style='color: lightgreen;'>(?=)</span> checks if a pattern is ahead the current position, there is no example of this used in the regex [above](#regex).

look-behind <span style='color: lightgreen;'>(?<=)</span> checks if a pattern is behind the current position, in the regex [above](#regex), look-aheads are used to reinforce the specific conditions.

## Author

<span style='color: lightgoldenrodyellow;'>**- Jacob Lowther**</span>

Hey! Congratulations on finishing this tutorial! You've now learned the essential components of regular expressions, and you're ready to start using them in your own projects.

To see more, check out [My GitHub!](https://github.com/yggdrasiljl)

