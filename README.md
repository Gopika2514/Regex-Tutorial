# Regex Tutorial 

In this tutorial, we will be taking a brief look into what Regex (regular expressions) are and how they work. While regular expressions may seem to be overwhelming at first glance,
just like with any language, they can be broken down into its most simple parts and easily understood.

## Summary

Regex (short for regular expression) is a string of text that allows you to create search patterns that match, manage, and locate text. An example code snippet of regex shows as following:
```
/[\w._%+-]+@[\w.-]+\.[a-zA-z]{2,4}/
```
* A regular expression used to match an e-mail address

Regular expressions can also be used from the command line and within text-editors to find text within a file. 




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

## Anchors
Anchors are characters within the regular expression that allow the user to match strings that begin with or ends with (or both) certain characters. 

* `^` - matches any string that start with the anterior word
* `$` - matches a string that end with preceeding word before the character
* Examples:
```
^Hello          matches any string starting with `Hello`
World$          matches any string ending with `World`
^Hello World$   matches exact string
goodbye         matches any string that has the exact text `goodbye` in it
```



## Quantifiers
Qunatifiers are characters within the regular expression that specify how many instances a character, group, or character class must be represented in the input to be matched.

Examples of Quanitifers are as follows:

* `*` - matches a string that has the anterior followed by zero or more of the last character
* `+` - matches a string that has the anterior followed by one or more of the last character
* `?` - matches a string that has the atnerior follwoed by zero or one of the last character
* `{}` -  matches a string that has the anterior followed by how ever many the number in the brackets of the last character in the string
* `()*` - matches a string that has any anterior characters followed by zero or more copies of the string within the brackets

* Examples:
```
xyz*        matches a string that has xy followed by zero or more z
xyz+        matches a string that has xy followed by one or more z

```

## Grouping Constructs
Examples of Grouping are as follows:
* `()` - parentheses creates a capture group
* `(?:)` - using `?:` disables the capturing group
* `(?<>)` - using `?<>` puts a name to the group


### Bracket Expressions
Bracket Expressions are characters enclosed by a bracket `[]` matching any single character within the brackets. 

Examples of Bracket Expressions are as follows: 
* `[]` - matching any single character within the brackets
* `[]%` - matching the string inside the brackets before the `%`
* `[^]` - matching any string that has not a letter from within the brackets 

[xyz]         matches a string that etiher has x or x y or x z (same as x|y|z)
[x-y]         similar to case above

## Character Classes
Character Classes (Character Set) tells the regex engine to match only one out serveral specific characters, such as digits, words, or whitespace

Examples of Character Classes are as follows:

* `\d` - matches a single character that is a digit
* `\w` - matches a word character (any alphanumeric character plus underscore)
* `\s` - matches a whitespace character (including tabs and line brakes)
* `.` - matches any character
```
\d    matches a single any digit 0-9
\w    matches a single any character that is a-z
\s    matches ` `
.     matches any character
\D    matches a single non-digit character
\W    matches a single any non-character that is a-z
\S    matches a single non-` `
```

## The OR Operator
OR Operators (Alternation Operator) matches on of a choice of regular expressions: if you put the character(s) representing the alternation operator between any two characters in the regular expression, the result matches the union of the strings that those two characters match.

Examples of OR Operators are as follows:

* `(|)` - matches a string that has any anterior characters followed by the characters on the left or right of the vertical bar
* `[]` - matches a string that has any anterior characters without any characters within the brackets

## Flags
Flags are optional parameters that we can add to a plain expression to make it search in a different way. Each flag is denoted by a single alphabetic character, and serves different purposes in modifying the expression's searching behavior.

Examples of Flags are as follows:
* `g` - Global, does not return after the first match, which restarted any subsequest searches from the end of the previous match (Makes the expression search for all occurences)
* `m` - Multi-line, when enabled the Anchors (^ $) will match the start and end of a line, rather than the whole string

/Hello/g   matches all `Hello` in the test

## Character Escapes
Character Escape (Character Set) tells the regex engine to match only one out serveral specific characters, such as digits, words, or whitespace
* `\d` - matches a single character that is a digit
* `\w` - matches a word character (any alphanumeric character plus underscore)

```
\d    matches a single any digit 0-9
\w    matches a single any character that is a-z
\s    matches ` `
.     matches any character
\D    matches a single non-digit character
\W    matches a single any non-character that is a-z
\S    matches a single non-` `
```


## Author

Myself, Gopika and I am a full-stack bootcamp student. 
Feel free to check out more of my work. My GitHub account is linked below

Github Profile: http://github.com/Gopika2514

Gist link: https://github.com/Gopika2514/Regex-Tutorial/blob/main/gist-template.md
