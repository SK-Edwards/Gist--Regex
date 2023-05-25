# Title (replace with your title)

Introductory paragraph (replace this with your text)

## Summary

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

Regexes are composed of several different components that work together to define a search pattern. The most common components include anchors, character classes, quantifiers, and alternation.

### Anchors

The characters ^ and $ are both considered to be anchors.

The ^ anchor signifies a string that begins with the characters that follow it.
The $ anchor signifies a string that ends with the characters that precede it. Just as with the ^ character, it can be preceded by an exact string or a range of possible matches.

### Quantifiers

Quantifiers set the limits of the string that your regex matches (or an individual section of the string). They frequently include the minimum and maximum number of characters that your regex is looking for.

### OR Operator

The Or operator (|) allows for matches with multiple requirement patterns outside of a bracket expression.

### Character Classes

A character class in a regex defines a set of characters, any one of which can occur in an input string to fulfill a match. 

### Flags

Flags are placed at the end of a regex, after the second slash, and they define additional functionality or limits for the regex. There are six optional flags that can be used, either separately or together and in any order. 

![*] 

### Grouping and Capturing

Grouping is done using perentheses (()) to form subexpressions which check multiple parts of a string to determine whether or not different sections fulfill different requirements.
 Capturing groups capture the matched character sequences for possible re-use (including a numbered backreference).
 A grouping construct can be made non-capturing by adding the characters ?: at the beginning of an expression inside the parentheses.

### Bracket Expressions

Anything inside a set of square brackets ([]) represents a range of characters that we want to match. These patterns are known as bracket expressions, but they are also known as a positive character group, because they outline the characters we want to include. 
It's also important to note that this pattern does not require the string to meet all of these requirements; it can meet any of them.
A bracket expression can be turned into a negative character group by adding the ^ symbol to the beginning of the expression inside the brackets. 

### Greedy and Lazy Match

Greedy match, meaning the regular expression matches as many occurrences as possible.
Lazy match, this means the reegular expression matches as few occurences as possible.
Quatifiers are inerently greedy but can be made lazy by adding the ? symbol after it. 


### Boundaries

Boundary markers such as ^ and $ allow you to anchor the regex pattern to the beginning and end of the line respectively. Yep, in that light, our anchor is a boundary.
The word boundary \b matches positions where one side is a word character (usually a letter, digit or underscore) and the other side is not a word .character
Word boundaries are useful when you want to match a sequence of letters (or digits) on their own, or to ensure that they occur at the beginning or the end of a sequence of characters.

### Back-references

A backreference allows a previously matched subexpression to be identified subsequently in the same regular expression.

### Look-ahead and Look-behind

Lookaheads and lookbehinds are types of capture groups that traverse text until a certain pattern occurs. A lookahead traverses the string from the beginning of the line. A lookbehind traverses a line from its end.

The metacharacters that indicate a lookahead are: ?= . The metacharacters that indicate a lookbehind are: ?<= .

Lookaheads and lookbehinds don't include the matching pattern that defines their boundary.

![*]

## Author

Shamary Edwards :
