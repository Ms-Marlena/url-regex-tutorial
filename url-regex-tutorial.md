# URL Regex Tutorial

A regex (short for "regular expression") is a pattern written in a specific way to assist with searching for text that follows a certain pattern or format. You can search for things like phone numbers, email addresses, HTML tags, URL addresses, or anything that must be written in a specific format. Regexes transcend programming languages, and do not need to be modified in order to be used from language to language. In addition to searches, regexes provide a way to verify whether user entries on a web page are formatted correctly, or contain the correct composition of characters.

## Summary
This Regex regular expression can be used to match a URL within a document.
I will describe the parts of the regex, as seen below in the table of contents. 
Hopefully, this will explain the regex and help you understand the different parts of a regex expression! 

    /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

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

URL Regex:
    /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
    
### Anchors
All regexes begin and end with a forward slash: / <i>regex here</i> /
The anchors within tell you where the regex string starts and ends.
The caret ^ signifies the beginning, and the dollar sign $ signifies the end.

### Quantifiers * + ? {n} {n, } {n, x} 

https? -the's' can either be present or not, since URLs can begin with 'http' or 'https'. 

\? -the match of (https?:\/\/) can either be present or not, since many URLs are written without the opening 'http://' or 'https://'. 

[\da-z\.-]+ 
The string [\da-z\.-] must have at least 1 or more matching characters. 

[a-z\.]{2,6} 
The characters in the bracket can be matched a minimum of 2 times, up to a maximum of 6 times.

[\/\w \.-]* 
The characters in the bracket: can either be present or not, since URLs are not all the same length.

([\/\w \.-]*)* 
The entire bracket expression ([\/\w \.-]*)* can either be present or not, for the same reason.

\/? 
There could be one forward slash at the end of the URL, or there could be none. 

### OR Operator |
This regex doesn't contain any OR operators.

### Character Classes
This regex contains both **literal** and **meta** characters. 
#### Meta Characters 
All of the quantifiers listed above are meta characters. In addition:

    (https?:\/\/)
    ([\da-z\.-]+)
    ([a-z\.]{2,6})
    ([\/\w \.-]*)
Parentheses designate groups of characters to match exactly, so the first needs to be exactly 'http://' or 'https://'. The others, since they contain **bracket expressions**, must be present (unless otherwise designated by a quantifier), but the characters can vary within the parameters defined within the brackets.

#### Literal Characters

    - when the appears outside of parentheses or brackets, it must be present at that point in the string to match as a URL. 

\. - This '.' turns from a quantifier into a literal character, when preceded by the '\' . 


### Flags
There are no flags in this regex

### Grouping and Capturing ('string') ('?:')
There are no capturing groups in this regex. The groups above, in **Meta Characters**, are non-capturing.

### Bracket Expressions ['string']
[\da-z\.-]+ 
Matches any combination of numbers from 0-9, lower-case letters from a-z, periods, and dashes.

[a-z\.]
Matches any combination of lower-case letters from a-z and periods.

[\/\w \.-]
Matches any combination of forward slashes, upper- and lower-case letters from a-z, numbers from 0-9, and underscores.

### Greedy and Lazy Match
There are no "lazy" matches in this regex. All the quantifiers present are "greedy": they match as many occurrences of patterns as possible, instead of matching the minimum required occurrences of patterns.

### Boundaries
There are no boundaries in this regex.

### Back-references
There are no back-references in this regex.

### Look-ahead and Look-behind
There are no look-aheads or look-behinds in this regex.

## Author
Marlena Hooker Moore
Colorado, USA
https://github.com/Ms-Marlena


