# Regex Tutorial - Breaking Down the FUNdementals in Email Validation

A regex or "regular expression" is a sequence of characters used to define a search pattern that will return matches and/or non-matches usually based on user input.  Examples include validating email addresses, credit card numbers, url addresses, user names, phone numbers and more.  These examples require user input to be in a certain format, so the regex can function to weed out sequences that don't fit the required pattern.
In this tutorial I will break down a commonly used regex to help better understand how the patterns fit together.  
<br>
<br>

## Summary

Regex at first glance is just a jumble of all the letters, numbers, and special characters you can find on your computer keypad. As a beginner programmer you can see patterns, but what does it all mean?

 Below I have outlined the highly used email validation regex to better equip you in understanding the different parts that make up the whole.

## Table of Contents

- [Regex Email Validation Code](#regex-email-validation-code)
- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Author](#author)
- [Acknowledgements](#acknowledgements)

## Regex Email Validation Code
  Using this email validation code from class: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`, we can break down each component to better understand how each fits into the whole.

### Anchors
Anchors define sections of the expression as the beginning or end. They are used to identify the start, end or boundary of a string, line, or word.  In our example above we see two anchors: `^ ` which indicates the beginning of the string and `$` to idicate the end of the string.

### Quantifiers
Quantifiers define how many instances of a character, group, or character class must be present in the user input to be validated. The `{2,6}` quantifier above requires that the 2nd portion of the domain name (i.e. yahoo, gmail, gov) be at minimum 2 and maximum 6 characters.

### Character Classes
A character class is a set of defined characters within square brackets. In our expression, `[a-z0-9_\.-]` defines the possible characters that would be valid for the local-part of the user's email before the @ symbol.
In addition the `[\da-z\.-]` and `[a-z\.]` components define the possible characters that are valid in the domain name (eg. hotmail.com) before and after the `.` that separates them.

### Bracket Expressions
Most programmers (even beginners!) are familiar with the square brackets `[]`. Used in regex they do exactly what you think thay might - they contain and define a character class that the regex must look to match for validation. Used in our example, the brackets contain the letters, numbers, and/or symbols that are valid in that particular section of the email address.

### Greedy and Lazy Match
In regex, using the `+` as a greedy match, we see in our email validator that the first set of parenthases inludes the bracket expression then the `+` outside the bracket.   This plus sign will require (greedy) that the first section will be followed by the @ symbol used in all valid email addresses.  Following that logic you can the the `+` symbol used again to require the second section of the address be followed by the period used in the regex, and then the final section of the email address.


## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)

## Acknowlegements
https://cheatography.com/davechild/cheat-sheets/regular-expressions/
https://support.workiva.com/hc/en-us/articles/4407304269204-Regular-expression-operators


