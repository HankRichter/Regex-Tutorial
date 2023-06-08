# Matching a Hex Value Regex

This will be a tutorial on how to read and use the regex for matching a hex value.

## Summary

After this tutorial you will be able to know how to use the hex value regex. This can be incorporated in a control+find or within code to find any hex value.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)

## Regex Components

This is our Regex that we will be dissecting in this tutorial.

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

Literal Characters: `#`

Anchors: `^` and `$`

Quantifiers: `?`, `{6}`, `{3}`

OR Operator: `|`

Grouping: `([a-f0-9]{6}|[a-f0-9]{3})`

Bracket Expressions: `[a-f0-9]`

### Anchors

The anchors we use in this Regex are `^` (Start of our string) and `$` (End of our string) at the beginning and end of the Regex.

### Quantifiers

We have a quantifier of `?`. This is after the literal character `#` and is also the character it affects. This will match any result with none or one `#`

Matches:

`#FFF`

Does not match:

`##FFF`

We also have quantifiers `{6}` `{3}`, these work in conjunction with our bracket expressions `[a-f0-9]` to matches the pattern 6 or 3 times. This produces a string with a length of 6 or 3.

### OR Operator

We have an or (`|`) operator between our two bracket expressions `([a-f0-9]{6}|[a-f0-9]{3})`. This is in place because you only need one bracket expression fulfilled to produce a result.

Matches:

`#FFF`

`#H34G4J`

Does not match:

`#FFFF`

`#FF`

### Grouping and Capturing

Our grouping comes with the whole expression after the `#`. This allows us to combine our two bracket expressions with their respective quantifiers.

### Bracket Expressions

Our Bracket Expression is `[a-f0-9]` this will find us matches with any lower case letter a-f or any number 0-9.

Matches:

`#FFF`

`#OOO`

Does not match:

`#!!!`

`#<<<`

## Author

- Github: [HankRichter](https://github.com/HankRichter)
- Email: [hankrichter97@gmail.com](mailto:user@example.com)
