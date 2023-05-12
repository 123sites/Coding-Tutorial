⭐ # Coding Tutorial ⭐

This is a tutorial about regex or regexp or regular expressions that are used in coding.  They help with searching and maipulating text strings, specifically with processing text files.  These are expressions that reduce the amount of code needed.  They are used by many different coding languages.

## Summary

The below tutorial describes an email matcher.  It explains how a validator is brokendown and returns strings within a document.  The validator has a username, host name, and domain.  To verify if a given input string is a valid email, it needs to be matched with the following id:
```/^[a-zA-Z0-9.!#$%&'*+/=?^_`{|}~-]+@[a-zA-Z0-9-]+(?:\.[a-zA-Z0-9-]+)*$/```

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

With regex, there is a pattern that must be wrapped in slash characters (/).
Below explains the components of a regex.

### Anchors

Anchors begin and end a string.  Some examples are:
-  `^` is a caret that is used to show the email begins with characters that follow it.
-  `$` is used to show a string ending with characters that comes before it.  
   The `$` also comes before an exact string or range of possible matches.


### Quantifiers

They speicify numbers of characters or expressions to match and sets the limit.  There is often a minimum
and maximum number of characters regex is looking for.  Qualifiers match as many of the patterns that occur
within it as much as possible.  `"Greedy" qualifiers` match as many times within a particular pattern as possible
and `"Lazy" qualifiers` match as few occurences as possible.

`Examples: Being quantified is [a-z0-9_\.-]+ and [da-z\.-]+`
'{2,6} are used to quantify [a-z\.}{2,6}.  This pattern matches a minimum of 2 and maximum of 6.`

`Greedy Qualifiers:`
* `*`    Matches the pattern zero or more times
* `+`    Matches the pattern one or more times, `examples: [a-z0-9_\.-]+ and [da-z\.-]+`
* `?`    Matches the pattern zero or one time
* `{}`   Sets a match limit
- `{n,x}`Matches n minimum and x maximum number of times, `example: {2,6}`

`Lazy Qualifiers:` Add the `?` symbol after it.

### Grouping Constructs

Each group captures parts of data.  The first group `([a-z0-9_\.-\+)` captures the email name.  The second group `([\da-z\.-]+)` captures the user's email provider.  Lastly, `([a-z\.]{2,6})` will capture the top level domain input for the user.


### Bracket Expressions

Characters typed within the brackets `[]`, is a range of characters the are needed to be matched.
The pattern is what is referred to as the "Bracket Expressions" or positive character group.
the `-` is used between alphanumberic characters.  They show a range of possible characters.
For example: `[a-c]` and `[abc]` will be the same.  The `-` and `_` can include an underscore or hyphen. Here are some examples:
-  `[a-zA-Z]`   Lower and uppercase letters.
-  `[0-9]`      Numbers 0-9.
-  `[a-z0-9_-]` Lowercase letters with numbers 0-9 and special charaters of an underscore or a hyphen.

### Character Classes

It determines the types of characters, for example, finding the difference between digits and letters.  For example: `[x-z0-9]`

### The OR Operator

The OR Operator is the `|`.  For example, if you had [abc], you would write it as `(a|b|c)`.
If you had the expression `(abc):(xyz)`, the OR Operaator would convert it to: `(a|b|c):(x|y|z)`.
The strings `abc:xyz` and `acb:xyz`, as well as `a:z`, but not `xyz:abc`.  There were no OR operators
in this email matching regex.

### Flags

This is the exception to the rule of a literal. Flags are put at the end of a regex, after the second dash, define additionalusage for the the regex.  In this email example, there are no flags.  The three most common flags are:
* `m` - Multiline search 
* `g` - Global search
* `i`  - Case-insensitive search

### Character Escapes

Escaping is a way of quoting single characters.  The `\` or backlash in regex is used to signify and escape, so that the expression would not interpret `\{` as the beginning of the qualifier. When special characters, like the \ are used inside bracket expressions, they lose their special significance.  Example: @gmail.com

## Author

[My GitHub Profile](https://github.com/123sites)

I am Chel Freitas, a Full Stack Developer, with a drive to create user-friendly websites that will attract visitors to use their
website!  I have a:
- Bachelor's degree in Education from the University of Arizona.
- Endorsement to teach students whose second language is English and Middle School Science
- I earned certification as a STEM teacher, which included making an ROV and participating in a competition.

After retiring early from teaching.  Over the years, I taught: 
- 6th grade (most subjects) 
- 7-8th grade science, introductory computers, and TV Broadcasting 
- In 1998 and 2008, I was a second language learner, learning in Mexico, through a study abroad program offered
  through the University of Arizona.

I have my own YouTube channel that is about my hobby of researching genealogy, connected to the Azores and travel there.  
Here is a link to my YouTube Channel: [Azores Travel & Genealogy](https://www.youtube.com/channel/UCMNe2clJI6nf-rmXoVg01xw)  

## Sources

Rex Egg - Rex Eats Regular Expressions for Breakfast: https://rexegg.com/

Regular-Expressions.info

Mozilla - Regular Expressions: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions

Chris Bongers - Vanilla JavaScript Email Validation: https://dev.to/dailydevtips1/vanilla-javascript-email-validation-21b3

Coding Bootcamp - Regular Expressions Tutorial: https://coding-boot-camp.github.io/full-stack/computer-science/regex-tutorial

Simpleilearn - How to Do an Email Validation in JavaScript:  https://www.simplilearn.com/tutorials/javascript-tutorial/email-validation-in-javascript

Escaping 5.2 - https://tldp.org/LDP/abs/html/escapingsection.html#:~:text=Escaping%20is%20a%20method%20of,special%20meaning%20for%20that%20character.