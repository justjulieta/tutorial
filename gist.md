## Title (replace with your title)
This tutorial will go over how one can use regular expressions (as known as regex) to match email addresses using the following expression /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/. Technologies such as Node.js often use these so it comes in handy learning and undertsanding the significance of these.

## Summary
In this regex tutorial, I will explain how to validate an email address using regular expressions. I will break down the components of the regex and explain what each part does. Additionally, I will provide a code snippet in Python to show how to use this regex to validate an email address.

const emailRegex = /^[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Z|a-z]{2,}$/;

const email = "example@email.com";

if(emailRegex.test(email)){
  console.log("Valid email address");
} else {
  console.log("Invalid email address");
}

## Table of Contents
- Anchors
- Quantifiers
- OR Operator
- Character Classes
- Flags
- Grouping and Capturing
- Bracket Expressions
- Greedy and Lazy Match
- Boundaries
- Back-references
- Look-ahead and Look-behind

## Regex Components

# Anchors
An anchor is a special character that is used to match specific positions within a string.

- Start anchor (^): This anchor is used to match the beginning of a string. For example, the regex "^hello" will match any string that starts with "hello".

- End anchor ($): This anchor is used to match the end of a string. For example, the regex "world$" will match any string that ends with "world".

# Quantifiers
These are special characters that are used to specify the number of times a character or group of characters can appear in a pattern. There are several quantifiers in regex, and they are typically used with characters or character classes to match specific patterns.

Examples: 

The asterisk (*) quantifier: This quantifier specifies that the preceding character or group can appear zero or more times. For example, the regex "a*" will match any string that contains zero or more "a" characters.

The plus (+) quantifier: This quantifier specifies that the preceding character or group must appear one or more times. For example, the regex "a+" will match any string that contains one or more "a" characters.


## OR Operator
The OR operator is represented by the vertical bar (|) character and allows you to match one of several possible patterns. It's often used to create more complex patterns by combining multiple subpatterns.

## Character Classes
A character class is a way to match any one of a set of characters. It allows you to specify a group of characters that can be matched by a single character in the input string.

Examples:

Square brackets ([]) character class: This is the most common character class in regex. It allows you to specify a list of characters that can be matched by a single character in the input string. For example, the regex "[abc]" will match any string that contains either "a", "b", or "c".

Dash (-) range character class: This character class allows you to specify a range of characters using a dash (-) between the starting and ending characters. For example, the regex "[a-z]" will match any lowercase letter from "a" to "z".


## Flags
Flags are special options that modify the behavior of the regex pattern. They are added after the closing delimiter of the pattern and are denoted by a single letter.

Examples:

Case-insensitive flag (i): This flag makes the regex pattern case-insensitive. For example, the regex "/hello/i" will match both "hello" and "HELLO".

Global flag (g): This flag allows the regex pattern to match all occurrences of a pattern in the input string, rather than just the first one. For example, the regex "/cat/g" will match all occurrences of the word "cat" in the input string.

## Grouping and Capturing
grouping and capturing allows you to create subpatterns within your main pattern, which can then be referenced or manipulated separately.

Examples:

Parentheses ( ) for grouping: Parentheses can be used to group parts of a pattern together, allowing you to apply quantifiers or alternations to a subpattern. For example, the regex "(abc)+" will match one or more occurrences of the sequence "abc".

Backreferences (\1, \2, etc.) for capturing: Backreferences allow you to refer to a matched subpattern later in the regex pattern. They are created by enclosing a subpattern in parentheses, and then referencing it using \1, \2, and so on. For example, the regex "([a-z])\1" will match any repeated letter, such as "ee" or "ll".

## Bracket Expressions
These allow you to define a character set that matches any one of a set of characters. Bracket expressions are enclosed in square brackets [ ] and can contain:

Character classes: Inside a bracket expression, you can use character classes to match any character that belongs to a particular class. For example, the regex "[aeiou]" matches any vowel character.

Ranges: You can specify a range of characters using the hyphen (-) character. For example, the regex "[a-z]" matches any lowercase letter from "a" to "z".

## Greedy and Lazy Match
These are two different ways of matching patterns that involve quantifiers like *, +, or ?. These quantifiers specify how many times a character or group of characters should be matched.

Greedy matching: By default, regex patterns are greedy, which means they match as much of the input string as possible. For example, the regex pattern ".*" will match any number of characters, including the entire input string.

Lazy matching: Lazy matching, also known as non-greedy or reluctant matching, matches as little of the input string as possible. This is done by appending a question mark (?) to the end of the quantifier. For example, the regex pattern ".*?" will match the smallest possible number of characters, even if it means not matching the entire input string.

## Boundaries
There are four types of boundaries:

Start of line (^): Matches the position at the beginning of a line.

End of line ($): Matches the position at the end of a line.

Word boundary (\b): Matches the position between a word character (as defined by the \w character class) and a non-word character. For example, the regex pattern "\bcat\b" will match the word "cat" but not "caterpillar".

Non-word boundary (\B): Matches the position where there is no word boundary. For example, the regex pattern "\Bcat\B" will match the word "cat" if it appears in the middle of a word, but not at the beginning or end.

## Back-references
A back-reference is a way to match a previously captured group within the same regex pattern. Back-references are denoted by a backslash () followed by the number of the capturing group you want to reference, such as \1, \2, \3, and so on.

## Look-ahead and Look-behind
These assertions are zero-width assertions that allow you to match patterns that are followed by or preceded by certain other patterns, without actually including those patterns in the match.

Positive look-ahead (?=pattern): Matches the current position if it is followed by pattern. For example, the regex pattern "foo(?=bar)" will match "foo" only if it is followed by "bar".

Negative look-ahead (?!pattern): Matches the current position if it is not followed by pattern. For example, the regex pattern "foo(?!bar)" will match "foo" only if it is not followed by "bar".

Positive look-behind (?<=pattern): Matches the current position if it is preceded by pattern. For example, the regex pattern "(?<=foo)bar" will match "bar" only if it is preceded by "foo".

Negative look-behind (?<!pattern): Matches the current position if it is not preceded by pattern. For example, the regex pattern "(?<!foo)bar" will match "bar" only if it is not preceded by "foo".

## Author

GitHub: justjulieta

Repo of this turtorial: https://github.com/justjulieta/tutorial
