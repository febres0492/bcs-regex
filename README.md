# Regex Password Strength Validation

Regular expressions are powerful tools for pattern matching in strings.  
This tutorial breaks down a regex pattern used for validating strong passwords.

<br>

## Summary

This pattern checks if a password contains at least one lowercase letter, one uppercase letter, one digit, and one special character, with a length of 8 characters at least.

Here is the regex pattern:  
```
^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)(?=.*[@$!%*?&])[A-Za-z\d@$!%*?&]{8,}$
```
<br>

| Regex Part | Description |
|------------|-------------|
| [![start](https://img.shields.io/badge/^-blue)](#anchors) | Ensures the match starts at the beginning of the string. |
| [![lowercase](https://img.shields.io/badge/-%28%3F%3D.*%5Ba--z%5D%29-blue)](#look-ahead-and-look-behind) | Ensures there is at least one lowercase letter. |
| [![uppercase](https://img.shields.io/badge/-%28%3F%3D.*%5BA--Z%5D%29-green)](#look-ahead-and-look-behind) | Ensures there is at least one uppercase letter. |
| [![digit](https://img.shields.io/badge/-%28%3F%3D.*%5Cd%29-red)](#look-ahead-and-look-behind) | Ensures there is at least one digit. |
| [![special](https://img.shields.io/badge/-%28%3F%3D.*%5B%40%24%21%25%2A%3F%26%5D%29-purple)](#look-ahead-and-look-behind) | Ensures there is at least one special character. |
| [![characters](https://img.shields.io/badge/-[A--Za--z%5Cd%40%24%21%25%2A%3F%26]%7B8%2C%7D-orange)](#quantifiers) | Matches any letter (uppercase or lowercase), digit, or specified special character, at least 8 times. |
| [![end](https://img.shields.io/badge/$-blue)](#anchors) | Ensures the match ends at the end of the string. |


<br>

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

<br>

## Regex Components

### Anchors  

Anchors are used to make sure the regex matches from the start or end of a string.

`^`: Asserts the position at the start of the string.  
`$`: Asserts the position at the end of the string.  
In our regex, `^` ensures the match starts at the beginning, and `$` ensures it ends at the end.

<br>

### Quantifiers  

Quantifiers specify how many times an element in a regex should be matched.

`{8,}`: Matches 8 or more of the preceding token.
In our regex, `{8,}` ensures the password is at least 8 characters long.

<br>

### OR Operator  

The OR operator `|` is not used in this regex.

<br>

### Character Classes  

Character classes match any one of the characters inside them.

- `[a-z]`: Matches any lowercase letter.  
- `[A-Z]`: Matches any uppercase letter.  
- `\d`: Matches any digit.  
- `[@$!%*?&]`: Matches any of the specified special characters.  

<br>

### Flags  

Flags are optional parameters to modify regex behavior. This regex does not use any flags.  

<br>

### Grouping and Capturing  

Grouping and capturing are used to create subpatterns and capture parts of the match.

- `(?=.*[a-z])`: positive look-ahead to ensure at least one lowercase letter.
- `(?=.*[A-Z])`: positive look-ahead to ensure at least one uppercase letter.
- `(?=.*\d)`: positive look-ahead to ensure at least one digit.
- `(?=.*[@$!%*?&])`: positive look-ahead to ensure at least one special character.

<br> 

### Bracket Expressions

Bracket expressions are used to specify some characters to match.

- `[A-Za-z\d@$!%*?&]`: matches any letter (uppercase or lowercase), digit, or specified special character.

<br>

### Greedy and Lazy Match

Greedy and lazy matching control how much text is matched. This regex uses greedy matching by default, as indicated by the absence of ? after the quantifiers.

<br>

### Boundaries

Boundaries specify word boundaries. This regex does not use any boundary assertions like `\b`.

<br>

### Back-references

Back references are not used in this regex.

<br>

### Look-ahead and Look-behind

Look-ahead assertions ensure certain patterns are present in the string.

- `(?=.*[a-z])`: Ensures at least one lowercase letter.
- `(?=.*[A-Z])`: Ensures at least one uppercase letter.
- `(?=.*\d)`: Ensures at least one digit.
- `(?=.*[@$!%*?&])`: Ensures at least one special character.

<br>

## Author
This tutorial was created by Carlos Febres, a passionate developer with a love for coding and sharing knowledge. For more tutorials and code, visit my GitHub profile.

[![Go to Profile >>](https://img.shields.io/badge/Go_to_Profile_>>-darkgreen?style=for-the-badge)](https://github.com/febres0492)  

