# Regular Expression

This will help you understand regular expressions(Regex). The notes here will help you breakdown and understand this regular expression that is used to help determine if the URL is valid.
Regular expressions can help determine if a password or an email is valid by matching certain characters and letters to a string. For example, the regular expression I used will help determine if a URL is valid.

## Summary

The following regex is used to determine URLs that are being used. It will check the format and the characters that are being used.

Valid URL

/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

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

The anchors are the beginning and the end of the regular expression.

/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

The ^ is the start of the string and it ends with the $. The beginning with (https?:\/\/) will validate if the URL is using the HTTPS option.
In the end of this regex, /? matches an optional trailing forward slash at the end of the string.

### Quantifiers

The quantifier determines how many times a specific character or character group is required in order to have a match.
In the code for the URL. ([\da-z.-]+) - This part matches one or more alphanumeric characters, dots, or hyphens.

### Grouping Constructs

Using the URL regex.

/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

(https?://)? - This part matches the optional "http://" or "https://" at the beginning of the string. The s? makes the "s" optional, and :// matches the literal characters "://".
([\da-z.-]+) - This part matches one or more alphanumeric characters, dots, or hyphens.
([/\w .-])* - This part matches zero or more occurrences of a forward slash, alphanumeric characters, spaces, dots, or hyphens. It captures any additional path or query parameters that may follow the domain.

### Bracket Expressions

The [\da-z.-] character class matches any digit, lowercase letter, dot, or hyphen.

### Character Classes

[\da-z.-] character class matches any digit, lowercase letter, dot, or hyphen.

### The OR Operator

The OR operator is not being used but I will use another example.

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

Where the # symbol is must match to the following.
[a-f0-9]{6} which will match a string that is 6 characters, with combinations of a-f letters and numbers 0-9.
| OR Operator
[a-f0-9]{3} will match a string 3 characters long with combinations of a-f letters and 0-9 numbers.

### Flags

The URL regex does not use flags.

/regex/

The slashes determine where the regular expression starts and ends. A flag can be used after the slash to give more for our matching.
-g which means global,
-m which means multiline, it will search line by line instead of a whole.
-i that mean insensitive, will make the regex case-insensitive so it will not capitol letters will match with lowercase.

### Character Escapes

/? - This part matches an optional trailing forward slash at the end of the string.

## Author

Created by:
Bret Kruse
<krusebret@gmail.com>
<https://github.com/BretKruse>
