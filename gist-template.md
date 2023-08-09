# Regex Tutorial: Matching a URL

A regular expression (regex), is a combination of characters that form a unique search pattern. They can be used dynamically and are more unique because they can search for a broader range of strings. Regex's typically consist of special characters to define the search criteria. This method would allow for a much quicker and broader range of strings set in the code that a developer may want to change, rather than a singular and defined string.

## Summary

This tutorial will breakdown the elements contained in a regex for finding URL(s).
The following regex will be used in this example to further the understanding of how regex's work and how to easily translate them.

Regex: /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

Anchors are the beginning and end points of our regex that enclose our defined search criteria.
The starting anchor, a caret symbol (^), defines what is at the start of our string search.
The ending anchor, a dollar sign ($), defines what is at the end of our string search.

For our example, /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/, the (^) is stating that the beginning of this regex starts as (https://), and the ($) is defining the endpoint of the search criteria.

### Quantifiers

Quantifiers are essentially questions/statements bundled into special character(s).

In our example, the (?) quantifier at the beginning of our regex, is stating that the URL can have any of the following pieces ( h, ht, htt, http, or https) in our search criteria.

### Grouping Constructs

Grouping constructs are the parts of the expression held together by the ()s. This is so that particular instances of the regex are a constant variable within the expression that will only change within the parameters that are preset inside of the contruct itself.

Following the previous example, (https?:\/\/) is a constructed grouping of a quantifier and separate variables to allow the statement to search for (https://). Another construct defined in this expression is ([\da-z\.-]+), which could translate to (1a.-).

### Bracket Expressions

Bracket expressions are encapsulated inside the []s. Typically, inside of the brackets is a range of characters that are being sought out, such as alphanumeric figures.

For example, ([\da-z\.-]+) is a construct containing a bracketed expression. The expression stated is in search of a digit (\d), letters between a to z (a-z), and it could also contain (.-).

### Character Classes

Character classes are variables that contain a set range of characters that can fill the regex.

Taking the previous example, inside of ([\da-z\.-]+), it may seem like the (\)s are just a way to separate the regex, however, they associate themselves with what comes after (\). So, it would actually be read (\d) and this is a classification for digits and (\.) allows for a literal (.) to be within the URL. 

### The OR Operator

This doesn't necessarily mean that all parts of the string, in a bracket expression, is required to be a part of the URL. It just means that within ([a-z\.]{2,6}) that the required result is has an alphabet (in this example, it is also case sensitive) between 2-6 total characters.

### Flags

Flags create an exception to wrapping the regex in slash characters (\). They are inserted at the end of the regex but unfortunetly, we don't have one in this example.

### Character Escapes



## Author

GitHub - https://github.com/Ren-kun235
Email - changleng651@gmail.com

### Sources

- https://coding-boot-camp.github.io/full-stack/computer-science/regex-tutorial
- https://www3.ntu.edu.sg/home/ehchua/programming/howto/Regexe.html
- https://regexr.com/ [to be able to translate code and have an easier time reading it]
