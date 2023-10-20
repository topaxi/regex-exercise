# Regular Expressions Exercises

## Installation

This document is written in Markdown, which is a small and simple formatted language, which can be rendered into a rich document.
To view this document in a more readable way, open it on Github using your browser :)

## Cheatsheet and help

| Tokens                 | Description                                                                                                                  |
| ---------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| `[abc]`                | Match a single character of a, b or c                                                                                        |
| `[^abc]`               | Match a single character **except** a, b or c                                                                                |
| `[a-z]`                | Match a single character in the range of a to z                                                                              |
| `[^a-z]`               | Match a single character **not** in the range of a to z                                                                      |
| `[a-zA-Z]`             | Match a single character in the range of a to z or A to Z                                                                    |
| `.`                    | Match any single character                                                                                                   |
| `\s`                   | Match a single whitespace character                                                                                          |
| `\S`                   | Match a single non-whitespace character                                                                                      |
| `\d`                   | Match a single digit                                                                                                         |
| `\D`                   | Match a single non-digit                                                                                                     |
| `\w`                   | Match a single word character (similar to `[a-zA-Z]` but also includes underscore, umlauts etc.)                             |
| `\W`                   | Match a single non-word character                                                                                            |
| `\b`                   | Match a single word boundary                                                                                                 |
| `\B`                   | Match a single non-word boundary                                                                                             |
| `\n`                   | Match a single newline                                                                                                       |
| `\r`                   | Match a single carriage return (files originating from Windows terminate each line with `\n\r`, all other systems just `\n`) |
| `\t`                   | Match a single tab character                                                                                                 |
| `\p{P}` or `\p{Punct}` | Match a single punctuation character (in Python Regular Expressions)                                                         |
| `[[:punct:]]`          | Match a single punctuation character (in `egrep` or `grep -E` Regular Expressions)                                           |
| `Upsi|Lou`             | Match either Upsi or Lou, note: prefer to use this with parenthesis                                                          |
| `(...)`                | Capture any enclosed token(s), useful to reference back to the captured value or to group tokens with `|` (or)               |
| `^(Upsi|Lou)$`         | Match either Upsi or Lou as the only word on a line (due to start and end tokens)                                            |
| `^(auf|ab)\w+`         | Match a word starting with auf- or ab-                                                                                       |
| `(\w)\1`               | Match two consecutive word characters, `\1` refers to the first group of parenthesis, `\2` would refer to a second group     |
| `\w?`                  | Match zero or one word character                                                                                             |
| `\w*`                  | Match zero or more word characters                                                                                           |
| `\w+`                  | Match one or more word characters                                                                                            |
| `\w{3}`                | Match exactly (any) three word characters                                                                                    |
| `\w{3,}`               | Match three or more word characters                                                                                          |
| `\w{3,5}`              | Match between three or five word characters                                                                                  |
| `^`                    | Start of line or string                                                                                                      |
| `$`                    | End of line or string                                                                                                        |

## Matching simple substrings

### Exercise 1: Matching Words

Write a regular expression to match the word "apple" in the given text.

Text: "I like apples and bananas."

### Exercise 2: Matching Email Addresses

Write a regular expression to match email addresses in the given text.

Text: "You can contact me at john.doe@example.com or jane_smith@email.co.uk."

### Exercise 3: Matching Phone Numbers

Write a regular expression to match phone numbers in the format "(123) 456-7890" in the given text.

Text: "Please call (555) 123-4567 for more information."

### Exercise 4: Matching Dates

Write a regular expression to match dates in the format "DD.DD.YYYY" in the given text.

Text: "The meeting is scheduled for 25.12.2023. Please confirm your attendance."

### Exercise 5: Matching URLs

Write a regular expression to match URLs starting with "http://" or "https://" in the given text. URLs can include letters, numbers, hyphens, and periods.

Text: "Visit our website at http://www.example.com or https://blog.sample-site.net."

### Exercise 6: Matching Hashtags

Write a regular expression to match hashtags (words starting with a #) in the given text.
Text: "I love #programming and #coding challenges."

### Exercise 7: Matching Special Characters

Write a regular expression to match any sequence of special characters in the given text.
Text: "!!??%%%$$ This is a line with some special characters ##\*\*@@".

### Exercise 8: Matching Words with Hyphens

Write a regular expression to match words containing hyphens in the given text.

Text: "The high-level programming language is user-friendly."

### Exercise 9: Matching Words with Apostrophes

Write a regular expression to match words containing apostrophes (e.g., "can't" or "I'm") in the given text.

Text: "I can't believe I'm going to the party tonight."

### Exercise 10: Matching Multiple Words

Write a regular expression to match the words "cat" and "dog" in the given text.

Text: "My cat and dog are best friends."

## Matching with character classes

### Exercise 1: Matching Alphabetic Characters

Write a regular expression to match all alphabetic characters in the given text.

Text: "The quick brown fox jumps over the lazy dog."

### Exercise 2: Matching Digits

Write a regular expression to match all digits in the given text.

Text: "12345 is a sequence of numbers."

### Exercise 3: Matching Alphanumeric Characters

Write a regular expression to match all alphanumeric characters in the given text.

Text: "A7B3x9zY2 is a mix of letters and numbers."

### Exercise 4: Matching Non-Alphanumeric Characters

Write a regular expression to match all non-alphanumeric characters in the given text.

Text: "Special characters: !@#$%^&\*()"

### Exercise 5: Matching Whitespace

Write a regular expression to match all whitespace characters in the given text.

Text: "Tabs\tand spaces are whitespace characters."

### Exercise 6: Matching Word Characters

Write a regular expression to match all word characters (letters, digits, and underscore) in the given text.

Text: "Regex_123 and Python3 are examples of word characters."

### Exercise 7: Matching Punctuation

Write a regular expression to match all punctuation characters in the given text.

Text: "Punctuation marks: .,;?!-"

### Exercise 8: Matching Lowercase Letters

Write a regular expression to match all lowercase letters in the given text.

Text: "The quick brown fox."

### Exercise 9: Matching Uppercase Letters

Write a regular expression to match all uppercase letters in the given text.

Text: "The ABBR is an abbreviation."

### Exercise 10: Matching Alphabetic Characters in a Specific Range

Write a regular expression to match all alphabetic characters between 'm' and 'r' (inclusive) in the given text.

Text: "The summer vacation is marvelous!"

## Matching with anchors

### Exercise 1: Matching Lines Starting with a Word

Write a regular expression to match lines that start with the word "Hello" in the given text.

Text:

```
Hello, how are you?
Hi there!
Hello, it's a beautiful day.
```

### Exercise 2: Matching Lines Ending with a Word

Write a regular expression to match lines that end with the word "goodbye" or "goodbye" with any punctuation in the given text.

Text:

```
Saying goodbye to friends is hard.
Goodbye, see you later!
Have a great day, not just a goodbye.
Saying goodbye
to your dog is very hard.
```

### Exercise 3: Matching Lines Starting and Ending with a Word

Write a regular expression to match lines that both start and end with the word "start" in the given text.

Text:

```
Start your engines and get ready to start!
The race is about to start.
The end is just as important as the start.
```

### Exercise 4: Matching Lines with Exact Word

Write a regular expression to match lines that contain the exact word "apple" in the given text. "Apple" should not be part of another word.

Text:

```
I have an apple and a pineapple.
The apple is red.
He's very happy.
```

### Exercise 5: Matching Empty Lines

Write a regular expression to match empty lines (lines with no characters) in the given text.

Text:

```

This is a line with content.



Another empty line.
```

### Exercise 6: Matching Lines with Digits at the Start

Write a regular expression to match lines that start with one or more digits in the given text.

Text:

```
123 Main Street
Avenue 456
No digits here.
42 is the answer.
```

### Exercise 7: Matching Lines with Digits at the End

Write a regular expression to match lines that end with one or more digits in the given text.

Text:

```
Apples 123
No numbers in this line.
99 bottles of beer on the wall 42
```

### Exercise 8: Matching Lines with Uppercase Letters

Write a regular expression to match lines that contain at least one uppercase letter in the given text.

Text:

```
hello world
No uppercase letters here.
This Line Has Uppercase Letters
```

### Exercise 9: Matching Lines with Word Boundaries

Write a regular expression to match lines that contain the word "car" as a whole word in the given text.

Text:

```
Cars are cool.
My car is fast.
Carpet is soft.
I'm going to the car shop.
```

### Exercise 10: Matching Lines with Specific Punctuation

Write a regular expression to match lines that contain the exclamation mark at the end of the line in the given text.

Text:

```
This is exciting!
Wow, that's impressive!
No excitement here
Good job!
```

## Matching with quantifiers

### Exercise 1: Matching Variable-Length Numbers

Write a regular expression to match any sequence of one or more digits in the given text.

Text: "There are 42 students in the class, and the answer is 7."

### Exercise 2: Matching Repeated Digits

Write a regular expression to match three consecutive digits in the given text.

Text: "The product key is 4555321."

### Exercise 3: Matching Optional Characters

Write a regular expression to match words that can be spelled with or without a trailing "u" (e.g., "color" or "colour") in the given text.

Text: "The color/colour of the sky is blue."

### Exercise 4: Matching Repetitions of a Specific Character

Write a regular expression to match words with three consecutive "x" characters in the given text.

Text: "The fox jumped over the foxx fence."

### Exercise 5: Matching Repeated Words

Write a regular expression to match repeated words (e.g., "the the") in the given text.

Text: "Yesterday the the cat chased the the mouse."

### Exercise 6: Matching Phone Numbers

Write a regular expression to match phone numbers in the format "(123) 456-7890" that may or may not include parentheses around the area code.

Text: "Call (555) 123-4567 or 555-7890 for assistance."

### Exercise 7: Matching Dates

Write a regular expression to match dates in the format "DD.MM.YYYY" with varying numbers of digits (e.g., "15.1.2023" or "5.12.23") in the given text.

Text: "The important dates are 15.1.2023 and 5.12.23."

### Exercise 8: Matching Words with a Specific Number of Vowels

Write a regular expression to match words with exactly three vowels in the given text.

Text: "The quiet cat slept peacefully."

### Exercise 9: Matching Repeated Patterns

Write a regular expression to match any sequence of "ab" characters repeated one or more times in the given text.

Text: "The pattern abababab is repeated."

### Exercise 10: Matching Email Addresses

Write a regular expression to match email addresses that contain a variable number of letters, digits, dots, and underscores, followed by the "@" symbol, and then a domain with a variable number of letters and dots.

Text: "Contact us at john.doe@example.com or jane_smith@email.co.uk."

## Matching with alternates

### Exercise 1: Matching Programming Languages

Write a regular expression to match the names of either "Python" or "JavaScript" in the given text.

Text: "I enjoy programming in Python and JavaScript."

### Exercise 2: Matching Colors

Write a regular expression to match colors "red," "blue," or "green" in the given text.

Text: "The flag can be red, blue, or green."

### Exercise 3: Matching Days of the Week

Write a regular expression to match any day of the week (Monday, Tuesday, Wednesday, etc.) in the given text.

Text: "The meeting is scheduled for Monday or Friday."

### Exercise 4: Matching File Extensions

Write a regular expression to match files with either a ".jpg", ".jpeg" or ".png" extension in the given text.

Text: "Valid images formats are .jpg, .jpeg and .png files."

### Exercise 5: Matching Phone Numbers

Write a regular expression to match phone numbers that start with either "(123)" or "(456)" in the given text.

Text: "Contact us at (123) 456-7890 or (456) 123-9876 for assistance."

## More exercises

### Exercise 1: Using grep to List Titles

Using the grep command, list all titles (lines that start with #) of the "regex-exercise.md" file.
