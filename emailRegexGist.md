# Email Matching with Regex

Have you ever wanted to quickly find an email. Well there's a way to do it without just typing in email and trying to find the email afterwards. Using Regex, or Regular Expressions, you can make an expression that will automatically find the email address for you.

## Summary

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/. This may look weird for people who have never seen a Regex before but this is what one would look like if you wanted to look for email addresses. There are multiple parts to this Regex such as the anchors, the quantifiers, the grouping constructs, character escapes, or operator, character classes, and flags. 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Escapes](#character-escapes)
- [Character Classes](#character-classes)
- [Author](#author)

### Anchors

 In the regex you see "^" and "$" which are used as anchors. The "^" anchor is used to begin the Regex with any character or number in front of it. The "$" anchor signifies the end of the Regex. These anchors can have a range of options in between them or specific characters. In this case what would be in between our Regex, /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/, is a range of characters and numbers, a few literals, and a quantifier before we close out the Regex.

### Quantifiers

 Before we close our Regex we will want to specify our character length for our domain extension. You may have noticed the {2,6} in our Regex, which is called a quantifier. This quantifier sets a limit to the character length, in our case a min of 2 and a max of 6, to set the limit of the domain extension. We do this since we can have a range of endings from .com, .co, .edu, .org, etc.

### Grouping Constructs

 We can look for different things for different parts by using grouping constructs. A group can be created by having something within parentheses. So having (a-z)@(a-z) would mean we're looking for a range of letters between a-z before stopping looking for an @ and then looking for another set of characters within the range of a-z.

### Bracket Expressions

You might be wondering how we are setting the range for this regex? We set the range using brackets. [a-z] would be a range of lower case a to lower case z. Because the regex is case sensitive if we wanted to include upper case letters and numbers we would do something like this [A-Z0-9]. In our case [a-z0-9_\.-] would mean we are looking for anything with in a range of lower case a through z, 0 through 9, hyphen, periods, and underscores (which is denoted with [_\.-])

### Character Classes

 Character classes are used to denote a certain character/s. For example in our own email regex, @([\da-z\.-]+), the \d is used to denote any number and is another way of calling for a range between 0-9. There are other flags that we don't use specifically in our email regex but can still be useful like \w standing for [A-Za-z0-9_] and many others.

### Character Escapes

 Sometimes we want to use something like "()" or "." as literals in our Regex. We can do this by adding a "\" before them so that the Regex knows that we want to use them as literals. As an example from our email regex, \.([a-z\.]{2,6})$/, the \. is used as a way to denote that we want to use the period as a literal and look for it.


### Author

Author: Abraam Ibrahim
GitHub: https://github.com/EvoL1e
