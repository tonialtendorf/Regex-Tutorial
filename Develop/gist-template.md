# Matching an HTML Tag- Regex Tutorial

Regular expressions are a series of special characters that define a search pattern. This tutorial will focus on matching an HTML tag: /^<([a-z]+)([^<]+)_(?:>(._)<\/\1>|\s+\/>)$/
Navigate to the table of contents to jump to each section to learn more about the regex.

## Summary

This regex tutorial will focus on matching an HTML tag. /^<([a-z]+)([^<]+)_(?:>(._)<\/\1>|\s+\/>)$/
This tutorial will describe how the code works and components that makes up the regex.

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

A regex must be wrapped in (/) characters since it is a literal. Below is the snippet of the regex wrapped in the (/) characters:
/^<([a-z]+)([^<]+)_(?:>(._)<\/\1>|\s+\/>)$/

### Anchors

Anchors do not match a specific character, instead, an anchor matches a position before, after, or between characters.
^ and $ are examples of regex anchors.

The ^ refers to the character right after the ^ character. For example in the HTML snippet: /^<([a-z]+)([^<]+)_(?:>(._)<\/\1>|\s+\/>)$/ : the ^ refers to the start of the code.
The $ refers to the characters before the $ character. For example in the HTML snippet above- the $ refers to the end of the code.

### Quantifiers
Quantifiers set the limits of the string that your regex matches. Quantifiers frequently include the minimum and maximum number of characters that your regex is looking for.

In the matching an html tag regex: /^<([a-z]+)([^<]+)_(?:>(._)<\/\1>|\s+\/>)$/ the following quantifiers are used:
- +: the + character is listed after the a-z and ^< bracket which means that the previous character should match one or more times
- *: the *1* character means that the pattern matches zero or more times

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

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
