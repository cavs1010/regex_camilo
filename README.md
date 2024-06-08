# 📚 Regex in Python: An Overview

Regular expressions (regex) are powerful tools for string manipulation and pattern matching. Here's a quick guide to get you started! 🚀

## 🔹 Basics of Regex

- **Literal Characters**: Most characters match themselves.
  - Example: `a` matches the character 'a'.
- **Special Characters**: Characters like `.` `*` `+` `?` `^` `$` have special meanings.
  - Example: `.` matches any character except a newline.

## 🔹 Special Sequences

- **`\d`**: Matches any digit (0-9) 🧮
- **`\D`**: Matches any non-digit character ❌
- **`\w`**: Matches any word character (a-z, A-Z, 0-9, _) 🔤
- **`\W`**: Matches any non-word character 🆎
- **`\s`**: Matches any whitespace character (spaces, tabs, line breaks) 📏
- **`\S`**: Matches any non-whitespace character 🚫

## 🔹 Quantifiers

- **`*`**: Matches 0 or more repetitions 🌟
  - Example: `a*` matches `'', 'a', 'aa', 'aaa', ...`
- **`+`**: Matches 1 or more repetitions ➕
  - Example: `a+` matches `'a', 'aa', 'aaa', ...`
- **`?`**: Matches 0 or 1 repetition ❓
  - Example: `a?` matches `'', 'a'`
- **`{n}`**: Matches exactly `n` repetitions 🔢
  - Example: `a{3}` matches `'aaa'`
- **`{n,m}`**: Matches between `n` and `m` repetitions 🧮
  - Example: `a{2,4}` matches `'aa', 'aaa', 'aaaa'`

## 🔹 Anchors

- **`^`**: Matches the start of a string 📍
  - Example: `^a` matches 'a' at the beginning of a string.
- **`$`**: Matches the end of a string 🎯
  - Example: `a$` matches 'a' at the end of a string.

## 🔹 Character Classes

- **`[abc]`**: Matches any one of the characters 'a', 'b', or 'c' 🅰️🅱️🆑
  - Example: `[aeiou]` matches any vowel.
- **`[^abc]`**: Matches any character except 'a', 'b', or 'c' 🚫
  - Example: `[^aeiou]` matches any non-vowel.

## 🔹 Grouping and Alternation

- **`(abc)`**: Groups the pattern 'abc' 🔗
  - Example: `(abc)+` matches 'abc', 'abcabc', ...
- **`a|b`**: Matches either 'a' or 'b' 🔀
  - Example: `a|b` matches 'a' or 'b'.

## 🔹 Escaping Special Characters

- Use `\` to escape special characters 🔒
  - Example: `\.` matches a literal period.

## 🔹 Example in Python

```python
import re

# Match a pattern
pattern = r'\d+'
text = "There are 123 apples"
match = re.search(pattern, text)

if match:
    print("Match found:", match.group())
else:
    print("No match found")
