
### REGEX TUTORIAL

This gist is a tutorial for a regex expression that matches a valid URL address.

### Summary
This tutorial will cover a step by step deconstruction of a regex that matches a valid URL address.

The regex expression we will be decoding is  ^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$

### Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Character Escapes](#character-escapes)
- [Final Test](#final-test)
- [Author](#author)

### Regex Components

### Anchors
Anchors matchs a position before or after characters.

- `^` - The caret anchor matches the beginning of the text. 
- `$` - The dollar anchor matches the end of the text.

In this case `^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$`, we have one anchor `^`  meaning where to start a matching pattern.

### Quantifiers
In this case `^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$`, we specify how many instances of a character, group, or character class must be present in the string matched.

In the case of `https?` : `https?` 

Matching zero or one string as dictated by the `?` sign after `https`, meaning that the URL can either start with "http" or "https".

In the example of `([\da-z\.-]+)` : `([\da-z\.-]+)` 

Matching one or more instances of the characters in the square brackets `[]`.  matches the group subdomain, domain name and top-level domain of the URL.

Example of `([\/\w \.-]*)*` : `([\/\w \.-]*)*` 

 Matching zero or more instances of the characters in the square brackets `[]` as dictated by the `*` sign after the group. This group matches the path and any query parameters in the URL.

Example `\/?$` : `\/?$`

The `\/?` matches an optional forward slash at the end of the URL, and the `$` anchor matches the end of the text.

### Character Classes
In this case `^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$`, we have [] square brackets, these are used to match different types of characters in order to match what you are looking for.

- `\da-z\.-]` in `([\da-z\.-]+)` matches digits, lowercase letters, period and hyphen.
- `\/\w \.-` in `([\/\w \.-]*)*` matches forward slash, word characters, space, period and hyphen.

### The OR Operator

We don't have any OR operator to match the pattern.


### Character Escapes
We use some escape characters to match the pattern:

- `\/` in `https?:\/\/` and `([\/\w \.-]*)*\/?` matches the forward slash.
- `.` in `([\da-z\.-]+)` and `([a-z\.]{2,6})` is used as an escape character to match the period character itself.

### test
<img width="685" alt="Test" src="https://user-images.githubusercontent.com/104470467/218716603-f2336737-422b-41bb-894e-5cd46c959399.png">


### Author
 Nebiat. 
