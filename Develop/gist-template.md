# Title (Hexidecimal Regex Tutorial)

The following is an explaination of the regular expression or "regex" for matching hexidecimal values: /^#?([a-f0-9]{6}|[a-f0-9]{3})$/

## Summary

Regular expressions are sequences of characters that specify a pattern to match when searching text. These are very useful in programming and can be created to do many different types of character matching.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Boundaries](#boundaries)

## Regex Components

Regular expressions have specific components that are used to define a search. It is important to understand these components and their syntax to use these expressions effectively.

Each regex is contained between two slashes: /regex components/

### Anchors

There are two anchors being used in our hexidecimal regex.

"^": This is the caret symbol, and it asserts the start of the string. It ensures that the pattern following it must appear at the beginning of the string.

"$": This is the dollar sign, and it asserts the end of the string. It ensures that the pattern preceding it must appear at the end of the string.

/^$/

### Quantifiers

"{}": This is a quantifier that specifies exactly how many occurrences of the preceding character or group should be matched.

In this case there are two quantifiers. Each follow [a-f0-9] and indicate that there must be exactly 6 characters in the first option or 3 in the second option in the range of lowercase letters 'a' to 'f' and digits '0' to '9'.

/^{6}{3}$/

### OR Operator

"|": This vertical bar acts as an OR operator in the regular expression. It allows for a choice between two patterns. In the provided regular expression, it separates two alternatives within the capturing group.

[a-f0-9]{6}|[a-f0-9]{3} means [a-f0-9]{6} or [a-f0-9]{3}

### Character Classes

"#?": This expression means that the characters we are searching for may or may not be preceded by a #, but it is optional.

"[]": Character classes define a set of characters, and the regular expression matches any single character that falls within the specified set. The character class is defined inside a bracket expression.

[a-f0-9]: This character class defines a set of characters that includes lowercase letters 'a' through 'f' and digits '0' through '9'. It represents the valid characters for a hexadecimal digit.

### Grouping and Capturing

"()": This is the containing field for a capturing group, indicated by the parentheses (). It defines the values needing to be matched.

In this case, it encompasses two alternatives separated by the | (OR) operator.

([a-f0-9]{6}|[a-f0-9]{3})

### Boundaries

"^" and "$" serve as the boundaries containing our regular expression.

## Author

Garrett Young
github profile: https://github.com/eymerin