# How to Match a URL with Regex

Matching a URL is a common task for regular expressions. the regular exprression shown will match any string that conforms to the following pattern: A regular expression pattern is composed of simple characters, such as /abc/, or a combination of simple and special characters, such as /ab*c/ or /Chapter (\d+)\.\d*/.

## Summary

In this tutorial, I will be exploring a regular expression that matches URL's. I will explain the different parts of the regex and how it works. The code snippet for the regex is shown below.
/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]_)_\/?$/

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

The expression I'm using to match URL's consists of several different parts, each with a specific meaning and purpose. Anchors, quantifiers, character classes, and groupings are just some of the elements that make up the expression. For example, the `https` are all characters that are part of a capturing group. Then at the beginning and end you have `<` and `$` meaning it is the beginning and end of a string.

### Anchors

The anchor tags are unique in that they match a position within a string, not a character.
They will be at the beginning `^` and end of the regex `$` as well as noting boundaries .

### Quantifiers

Quantifiers indicate that the preceding token must be matched a certain number of times. By default, quantifiers are greedy, and will match as many characters as possible. Group one of the capturing group `(https?:\/\/)` indicates it wants a substring of https wi a character for matching ':' and two escape characters `\/\/`

### OR Operator

The OR operator, represented by the `|` character, is used to match either of two alternatives. For example, the regular expression.

### Character Classes

Character classes match a character from a specific set. There are a number of predefined character classes and you can also define your own sets. this can be seen in the range `[\da-z\.-]`

### Flags

in the universe of regular expressions and how they can be used to modify the searching behavior of given patterns.
A flag is an optional parameter to a regex that modifies its behavior of searching. Flags are `i, g, s, m, y, u`
Of all the flags detailed, you'll find only the `i` and `g` flags to be easily understandable.

### Grouping and Capturing

Capturing in our case will be the sections `(https?:\/\/)`, `([\da-z\.-]+)`, `([a-z\.]{2,6})`, `([\/\w \.-]_)`.
these capturing groups, groups multiple tokens together and creates a capture group for extracting a substring or using a back reference.

### Bracket Expressions

Bracket expressions can be used to match a single character or collating element.
these can be spotted with anotations similar to `[a-z]`, this would match any character in the square brackets.

### Greedy and Lazy Match

By default, a quantifier tells the engine to match as many or as constrained instances of its quantified token or subpattern as possible. This behavior is called greedy or lazy. . `Greedy` means match longest possible string. `Lazy` means match shortest possible string. Our current URL search will be greedy due to the `+`.

### Boundaries

Boundaries are used to specify where a match can occur. The most common boundary will be the word boundary `\b`.
this boundary allows you to perform a “whole words only” search using a regular expression in the form of `\bword\b`.

## Author

Jack Nowaczewski - an eager developer looking for the next big break!
