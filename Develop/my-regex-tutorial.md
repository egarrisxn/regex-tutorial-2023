# My Regex Tutorial!

This tutorial on **Regular Expression (Regex)** aims to assist you in _comprehending_ and _establishing_ the order of unique characters for _validating_ a search term. A Regex refers to a **sequence of characters** that outlines a particular search pattern. Whether incorporated into code or search algorithm, regular expressions enable the identification of specific character patterns within a string, as well as the identification and substitution of **individual characters** or **sequences of characters** within a string. Moreover, they are commonly employed for validating input data.

## Summary

This tutorial will show you how to harness the power of regular expressions to _manipulate_ text based on specific patterns.

Let us explore how to utilize regex for **matching emails** using the expression `/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$`.

This knowledge can prove valuable when **validating email addresses** in certain applications and technologies.

## Table of Content

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Matching](#greedy-and-lazy-matching)
- [Boundaries](#boundaries)
- [Back References](#back-references)
- [Look Ahead and Look Behind](#look-ahead-and-look-behind)

### Anchors

The regular expression uses the `^` anchor to indicate the start of the string and the `$` anchor to indicate the end of the string. Without enabling the multiline flag, the regular expression will only match until the end of the line.

### Quantifiers

The regular expression employs the `+` operator as a quantifier, connecting the user's email name, email service, and ".com" together. Additionally, the `{2,6}` quantifier allows for a match range of 2-6 characters from the character set `[a-z]`.

## OR Operator

In regular expressions, the OR operator is denoted by the vertical bar `|`. It allows you to specify multiple alternatives for a pattern. For example, the regex `cat|dog` will match either "cat" or "dog".

### Character Classes

The character class in this expression is represented by `\d,` which matches a single digit character from 0-9. It will only match a single digit such as `4` but not `44`.

## Flags

Flags in regex are modifiers that can change how the pattern matching is performed. Some common flags include:

- **i (case-insensitive)**: This flag allows the regex engine to match characters regardless of their case. For example, `/hello/i` would match "hello", "Hello", "HELLO", etc.

- **g (global)**: This flag allows the regex engine to find all matches within the input string, not just the first one.

- **m (multiline)**: This flag alters the behavior of the `^` and `$` anchors, making them match the start and end of lines within the input string, rather than just the start and end of the entire string.

## Grouping and Capturing

The first capturing group, identified as group #1, is `([a-z0-9_.-]+),` which matches the user's email name. The second capturing group, group #2, is `([\da-z.-]+),` which matches the email service. Lastly, capture group #3, represented as `([a-z.]{2,6}),`, captures the ".com" portion.

## Bracket Expressions

The bracket expressions used for email validation consist of the character sets `[a-z0-9_.-]`, which match any case-sensitive letter from a to z, any digit from 0 to 9, and the characters `_`, `-`, and `.`. Similarly, the expression `[\da-z.-]` matches a single digit from 0 to 9, any case-sensitive letter from a to z, and the characters `.` and `-`. Lastly, `[a-z.]` matches any case-sensitive letter from a to z and the character `.`.

## Greedy and Lazy Matching

This regular expression utilizes greedy matching. The `+` quantifier matches as many times as possible while still allowing the expression to return as needed. Similarly, the `{}` quantifier in `{2,6}` for the last capture group also functions greedily.

## Boundaries

Boundaries in regex define the edges of words or strings. There are several boundary types:

- **Word Boundary (\b)**: Matches the position between a word character and a non-word character. For example, `\bcat\b` will match "cat" in "catapult" but not in "concatenate".

- **Start of String (^) and End of String ($)**: These anchors match the start and end of a string, respectively. For example, `^cat` will match "cat" only if it occurs at the start of the string, and `cat$` will match "cat" only if it occurs at the end of the string.

Back references allow you to match the same text as previously matched by a capturing group. They are denoted by `\` followed by the group number. For example, `\1` refers to the first capturing group, `\2` refers to the second capturing group, and so on.

## Look Ahead and Look Behind

Look ahead and look behind assertions are used to match a pattern only if it is followed or preceded by another pattern, without including the other pattern in the match. There are two types:

- **Positive Lookahead (?=pattern)**: Matches the current position only if followed by the specified pattern.
- **Negative Lookahead (?!pattern)**: Matches the current position only if not followed by the specified pattern.
- **Positive Lookbehind (?<=pattern)**: Matches the current position only if preceded by the specified pattern.
- **Negative Lookbehind (?<!pattern)**: Matches the current position only if not preceded by the specified pattern.

# Author

Ethan Garrison

Source: [Github](https://github.com/egarrisxn)

Contact: [Egarrisxn@gmail.com](mailto:egarrisxn@gmail.com)
