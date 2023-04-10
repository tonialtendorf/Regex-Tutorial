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
- *: the * character means that the pattern matches zero or more times

### OR Operator
The OR operator specifies that the regular expression engine should match either the code before the | or the code after the |. In the HTML regex: 
- >(._)<\/\1> matches a closing HTML tag that matches the opening tag: ([a-z]+).
- the (|) character specifies the OR operators
- \s+\/> matches a self-closing HTML tag that ends with />

### Character Classes
A character class defines a set of characters. In the HTML regex, the below is the character classes:
- `[^<]`: this character class matches any character that is not a <. THis is because the < symbol is used to start an html tag

### Flags
There are no flags specified in this regular expression.

### Grouping and Capturing
The HTML regex: /^<([a-z]+)([^<]+)_(?:>(._)<\/\1>|\s+\/>)$/ is split up by three groups- each defined and split up by parenthesis ().
Group 1- ([a-z]+)- THis group matches one or more lowercase letters between the opening < and the underscore _ character. This group captures the tag name of the HTML tag.
Group 2- ([^<]+)- This group matches one or more characters that are not < between the underscore _ and the closing > tag. This group captures any attributes or other information between the tag name and the closing bracket.
Group 3- (?:>(._)<\/\1>|\s+\/>)- This is a non capturing group that includes 2 alternatives:
- Alternative 1: >(._)<\/\1>
- Alternative 2: \s+\/>

### Bracket Expressions
The bracket character [] represents anything inside the brackets is what we want to match- they outline the characters we want to include. Below are the bracket expressions in the html regex.
- [a-z]+: matches one or more lowercase letters between the < and the underscore character.
- [^<]+: matches one or more characters that are not < between the underscore and the > character
- \s+: matches one or more whitespace characters before the /> closing sequence.
- \/: matches a forward slash character /, which is used to close the opening HTML tag.
- \1: a back reference to the first capturing group ([a-z]+), which matches the same text as previously matched by that group.

### Greedy and Lazy Match
Quantifiers + and * are considered greedy, but adding a ? to them will make them lazy. 

### Back-references
The regex /^<([a-z]+)([^<]+)_(?:>(._)<\/\1>|\s+\/>)$/ uses a back-reference in the form of \1. Using the back reference makes sure that the closing tag matches the opening tag in both name and order, and allows the regular expression to capture the contents of the tag if it is not self-closing.

### Look-ahead and Look-behind
The regex /^<([a-z]+)([^<]+)_(?:>(._)<\/\1>|\s+\/>)$/ does not use look ahead or look behind expressions.

## Author
Toni Altendorf:
 Feel free to contact me at tvohnoutka05@gmail.com.
  Please visit my github profile at [tonialtendorf](https://github.com/tonialtendorf/)

  ## References
  - https://coding-boot-camp.github.io/full-stack/computer-science/regex-tutorial
  - https://www.octoparse.com/blog/using-regular-expression-to-match-html
  - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions
