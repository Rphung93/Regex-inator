# Computer Science for JavaScript Challenge: Regex Tutorial #17

Hello, my name is Ricky and I'm new to the coding world, but I am going to do my best to explain what I've learned and apply it to the terms below.

## Regex Summary: Email Address Validation
const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;

###Explanation:

This regular expression (emailRegex) is designed to validate email addresses. Here's a breakdown of the components:

^: Asserts the start of the string.
[^\s@]+: Matches one or more characters that are not whitespace (\s) or the "@" symbol.
@: Matches the "@" symbol.
[^\s@]+: Matches one or more characters that are not whitespace (\s) or the "@" symbol.
\.: Matches the dot (.) in the email domain.
[^\s@]+$: Matches one or more characters that are not whitespace (\s) or the "@" symbol until the end of the string ($).
This regular expression ensures that an email address follows a standard format with a local part, the "@" symbol, a domain part, and a top-level domain (TLD). It does not allow spaces within the email address.
Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

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
Anchors are used to match positions in the text rather than characters. Common anchors include ^ which denotes the start of a line and $ which denotes the end of a line.
^Start of the line
End of the line$

### Quantifiers
Quantifiers specify how many instances of the preceding element should be matched. Common quantifiers include * (zero or more), + (one or more), and ? (zero or one).
\d+ matches one or more digits
[a-z]* matches zero or more lowercase letters

### OR Operator
The | symbol represents the OR operator, allowing you to match either of two alternatives.
cat|dog matches either 'cat' or 'dog'

### Character Classes
Character classes allow you to match any one of a set of characters. They are denoted by square brackets.
[aeiou] matches any vowel

### Flags
Flags modify how a regular expression behaves. Common flags include i for case-insensitive matching and g for global matching.
/apple/i matches 'apple' case-insensitively

### Grouping and Capturing
Parentheses are used for grouping and capturing. They define a subexpression and capture the matched result.
(\d{3})-(\d{2})-(\d{4}) captures a date in the format XXX-XX-XXXX

### Bracket Expressions
Bracket expressions are similar to character classes, providing a way to match one of a specified set of characters.
[0-9] matches any digit

### Greedy and Lazy Match
Quantifiers are greedy by default, matching as much as possible. Adding ? after a quantifier makes it lazy, matching as little as possible.
.*? matches any character (lazy)
.* matches any character (greedy)

### Boundaries
\b represents a word boundary. It matches the position between a word character (as defined by \w) and a non-word character.
\bword\b matches the whole word 'word'

### Back-references
A back-reference refers to a previously captured group. It allows you to match the same text again.
(\w+) \1 matches repeated words (e.g., 'apple apple' or 'dog dog')

### Look-ahead and Look-behind
Look-ahead and look-behind assertions allow you to assert that a pattern is or isn't followed or preceded by another pattern without including it in the match.
\w+(?=\s) matches a word followed by a space (positive look-ahead)

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
