# Regex Tutorial - Matching an Email

The tutorial aims to explain a bit about regular expressions with a primary focus on the:

Matching an Email Regular Expression – /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

This can be useful when validating emails using applications/technologies such as Node (Inqurier), MySql or MongoDB.

![*] 

A regular expression is a sequence of characters that defines a search pattern. This is commonly used to find patterns within a string, find/replace characters within a string or validate input.
This regular expression matches to an email address Which includes a random string of letters and numbers followed by an (@) symbol and a domain name.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)


## Regex Components

### Anchors

The characters `^` and $ are both considered to be anchors.

The `^` anchor signifies a string that begins with the characters that follow it.
The `$` anchor signifies a string that ends with the characters that precede it. Just as with the `^` character, it can be preceded by an exact string or a range of possible matches. 

Signifying the start and end of the email address.

![*]

![*]

### Quantifiers

Quantifiers set the limits of the string that your regex matches (or an individual section of the string). They frequently include the minimum and maximum number of characters that your regex is looking for.

Quantifiers in this regex includes the `+` operator, which will connect the users email name `+` email service + .com.
Another sets the limit to between `2` and `6` lowercase letters in that last group to capture the `.com`.

![*]

### Character Classes

A character class in a regex defines a set of characters, any one of which can occur in an input string to fulfill a match. 
The character class in this expression is `\d`, which matches a single characters that is a digit from `0-9`. It will only match a single digit such as "4", but not "12".

### Grouping and Capturing

Grouping is done using perentheses `()` to form subexpressions which check multiple parts of a string to determine whether or not different sections fulfill different requirements.
 Capturing groups capture the matched character sequences for possible re-use (including a numbered backreference).
 A grouping construct can be made non-capturing by adding the characters `?:` at the beginning of an expression inside the parentheses.
Capturing group #1 in this expression is `([a-z0-9_\.-]+)` that matches the user email name. The second capturing group is `([\da-z\.-]+)` which will match the email service. Then lastly, capture group #3 is `([a-z\.]{2,6})`` to capture the .com.

![*]
![*]
![*]

### Bracket Expressions

Anything inside a set of square brackets `[]` represents a range of characters that we want to match. These patterns are known as bracket expressions, but they are also known as a positive character group, because they outline the characters we want to include. 
It's also important to note that this pattern does not require the string to meet all of these requirements; it can meet any of them.
A bracket expression can be turned into a negative character group by adding the `^`` symbol to the beginning of the expression inside the brackets. 

Bracket expressions for email validation includes the character sets of `[a-z0-9_\.-]`, which is matching any letter a-z and is case senstive. It also matches a character `0-9` and matches the characters "_" , "-" , and "."; `[\da-z\.-]`, which is matching a single digit from `0-9`, any character `a-z` (case senstive), and the characters "." and "-".; `[a-z\.]` matches any character `a-z`lowercase and the character ".".

![*]
![*]
![*]

### Greedy and Lazy Match

Greedy match, meaning the regular expression matches as many occurrences as possible.
Lazy match, this means the reegular expression matches as few occurences as possible.
Quatifiers are inerently greedy but can be made lazy by adding the `?` symbol after it. 


### Boundaries

Boundary markers such as `^` and `$` allow you to anchor the regex pattern to the beginning and end of the line respectively. Yep, in that light, our anchor is a boundary.
The word boundary `\b` matches positions where one side is a word character (usually a letter, digit or underscore) and the other side is not a word .character
Word boundaries are useful when you want to match a sequence of letters (or digits) on their own, or to ensure that they occur at the beginning or the end of a sequence of characters.

## Author

Shamary Edwards :
