# Character Classes

## Character classes match a character from a specific set. There are a number of predefined character classes and you can also define your own sets

- Character set: [aeiou] Match any character in the set.
- Negated set: [^aeiou] Match any character that is not in the set.
- Range: [a-z] Matches a character having a character code between the two specified characters inclusive.
- Dot: . Matches any character except linebreaks. Equivalent to [^\n\r].
- Match any:[\s\S]  A character set that can be used to match any character, including line breaks, without the dotall flag (s).
- Word: \w Matches any word character (alphanumeric & underscore). Only matches low-ascii characters (no accented or non-roman- characters). Equivalent to [A-Za-z0-9_]
- Not word: \W Matches any character that is not a word character (alphanumeric & underscore). Equivalent to [^A-Za-z0-9_]
- Digit: \d Matches any digit character (0-9). Equivalent to [0-9].
- Not digit: \D Matches any character that is not a digit character (0-9). Equivalent to [^0-9].
- Whitespace: \s Matches any whitespace character (spaces, tabs, line breaks).
- Not whitespace: \S Matches any character that is not a whitespace character (spaces, tabs, line breaks).

# Anchors

## Anchors are unique in that they match a position within a string, not a character

- Beginning: ^ Matches the beginning of the string, or the beginning of a line if the multiline flag (m) is enabled. This matches a position, not a character.
- End: $ Matches the end of the string, or the end of a line if the multiline flag (m) is enabled. This matches a position, not a character.
- Boundary: \b Matches a word boundary position between a word character and non-word character or position (start / end of string).
- Not word boundary: \B Matches any position that is not a word boundary. This matches a position, not a character.

# Quantifiers and Alternation

## Quantifiers indicate that the preceding token must be matched a certain number of times. By default, quantifiers are greedy and will match as many characters as possible.

- Plus: + Matches 1 or more of the preceding token.
- Star: * Matches 0 or more of the preceding token.
- Quantifier: {1, 3} Matches the specified quantity of the previous token. {1,3} will match 1 to 3. {3} will match exactly 3. {3,} will match 3 or more.
- Optional: ? Matches 0 or 1 of the preceding token, effectively making it optional.
- Lazy: ? Makes the preceding quantifier lazy, causing it to match as few characters as possible. By default, quantifiers are greedy, and will match as many characters as possible.
- Alternation: |  Acts like a boolean OR. Matches the expression before or after the |.
