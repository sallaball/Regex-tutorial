# Regex Tutorial

This is a tutorial explaining the specifics of regex so that we can understand the search pattern the regex defines.

## Summary

Regex is a sequence of characters that define a search pattern. Typically, the patterns are used by string-searching algorithms for finding or finding and replacing operations on strings. It can also look for input validations. This is a technique commonly used in theoretical computer science.


Below you will find explanations for the different terms/elements.


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

The ^ and $ are anchors that fix a regex match to the beginning (^) or ending ($) of a line of text. In essence, they are the beginning and ending of a string.

### Quantifiers

with Quantifiers, you are trying to find how many times something happens or how many of a thing there are. Quantifiers include: ?,*,+,{}. The *,+ and {} found in regular expressions are considered quantifiers. The '?' indicates the expression to match 0 or 1 time.
For example: {6} (Hex Triplet Format) and {3} (Shorthand Hex Format), this tells you that the length of the component preceding these should be 6 for {6} and 3 for {3}.

### OR Operator

Defined using the | element. It indicates that either of the components that are separated with the | can be true/used. It basically could be described as the this OR that.

### Character Classes

Tells us what type of characters to expect. For example, [a-g] searches for letters between a and g, and [0-9] searches numbers between 0 and 9.

### Flags

'i' means the search is case-insensitive: no difference between A and a,
'g' means the search will look for all matches,
'm' is multiline mode and affects the behavior of ^ and $ byt making it where they match not only at the beginning and end of string, but also start/end of line.
's' enables "dotall" mode that allows a dot to match newline character,
'u' Unicode support: enables correct processing of surrogate pairs,
'y' is "sticky" mode: seach exact position in the text

### Grouping and Capturing

Example: ([a-z0-9_\.-]+) where the () group together the [a-z0-9_\.-] bracket expression with the + quantifier. This matches any letter or number a-z or 0 to 9, accepts underscores, periods and dashes.

### Bracket Expressions

Matches any character in the square brackets. For example [nN] [oO] matches no, nO, No, and NO. gr[ae]y matches both spellings of the word 'grey'; that is, gray and grey.

### Greedy and Lazy Match

Greedy match tries to match an element as many times as possible. A lazy match does the opposite by trying to match an element as few times as possible. Lazy match can be turned into greedy match by adding a ?.

### Boundaries

Word boundary, exhibited with a (\b) it is equivalent to an anchor. It tells the user that this is a word boundary. It is a way to declare here a word/this is a word boundary. Example “fish” within the parenthesis is a word. If a particular regex declared, with anchors, “this is the first of a regex string,” using a ^ carrot, or the end of a string with the dollar sign, then a space or place is being declared. \b asks the programing language to look for that whole word. for example, if we said, please find the entire word “fish.” There are more complexities involved, but that’s a basic idea

### Back-references

Back-reference is typically a \ followed by a single-digit. It is a command that refers to something that already happened, or a previous part of amatched regular expression. For example, if you have multiple groups in one pair of parentheses, you can refer to a specific group with the \ and the number of group. "\1" would refer to the first group in the parentheses.

### Look-ahead and Look-behind

* (?=ABC) is a postive lookahead and it matches a group after the main expression without including it in the result.

* (?!ABC) is a negitive lookahead and it specifies a group that can not match after the main expression (if it matches, the result is discarded)

* (?<=ABC>) is a postive lookbehind and matches a group before the main expression without including it in the result.

* (?<!ABC) is a negitive lookbehind and Specifies a group that can not match before the main expression (if it matches, the result is discarded).

Lookaheads and lookbehinds forces the main expressions to be what you have defined it as. Without it being exactly what it is it will not be accepted as a valid input.

## Author

Salla Ball: student at SMU full stack web development bootcamp

https://github.com/sallaball 
