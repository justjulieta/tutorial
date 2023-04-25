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


## Grouping and Capturing


## Bracket Expressions

## Greedy and Lazy Match

## Boundaries

## Back-references

## Look-ahead and Look-behind

## Author
