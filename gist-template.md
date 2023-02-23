# Regex Tutorial - Breaking Down the FUNdementals in Email Validation

Regex, or a regular expression, is defined in Wikipedia as:
<br>
"A sequence of characters that specifies a search pattern in text. Usually such patterns are used by string-searching algorithms for "find" or "find and replace" operations on strings, or for input validation. Regular expression techniques are developed in theoretical computer science and formal language theory."
<br>
<br>

## Summary

Regex at first glance is just a jumble of all the letters, numbers, and special characters you can find on your computer keypad. As a beginner programmer you can see patterns, but what does it all mean?

 Below I have outlined the highly used email verification regex to better equip you in understanding the different parts that make up the whole.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Email Validation Components
  Using this email validation code from class: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`, we can break down each component to better understand how each fits into the whole.

### Anchors
Anchors define sections of the expression as the beginning or end. They are used to identify the start, end or boundary of a string, line, or word.  In our example above we see two anchors: `^ ` which indicates the beginning of the string and `$` to idicate the end of the string.

### Quantifiers
Quantifiers define how many instances of a character, group, or character class must be present in the user input to be validated. The `{2,6}` quantifier above requires that the 2nd portion of the domain name (i.e. yahoo, gmail, gov) be at minimum 2 and maximum 6 characters.

### Character Classes
A character class is a set of defined characters within square brackets. In our expression, `[a-z0-9_\.-]` defines the possible characters that would be valid for the local-part of the user's email before the @ symbol.
In addition the `[\da-z\.-]` and `[a-z\.]` components define the possible characters that are valid in the domain name (eg. hotmail.com)before and after the `.` that separates them.

### Bracket Expressions


### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)

## Acknowlegements
https://en.wikipedia.org/wiki/Regular_expression
https://support.workiva.com/hc/en-us/articles/4407304269204-Regular-expression-operators

