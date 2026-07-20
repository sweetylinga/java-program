# Longest Valid Parentheses

## Problem Statement

Given a string containing only the characters `(` and `)`, return the length of the longest valid (well-formed) parentheses substring.

### Examples

**Example 1**
```
Input: s = "(()"
Output: 2
Explanation: The longest valid parentheses substring is "()".
```

**Example 2**
```
Input: s = ")()())"
Output: 4
Explanation: The longest valid parentheses substring is "()()".
```

**Example 3**
```
Input: s = ""
Output: 0
```

## Approach

This solution uses a **stack** to keep track of the indices of unmatched opening parentheses.

1. Initialize the stack with `-1` as a base index.
2. Traverse the string from left to right.
3. If the current character is `'('`, push its index onto the stack.
4. If the current character is `')'`, pop the top element.
5. If the stack becomes empty after popping, push the current index as the new base.
6. Otherwise, calculate the length of the current valid substring as:

```
currentIndex - stack.peek()
```

7. Update the maximum length whenever a longer valid substring is found.

## Time Complexity

- **Time:** O(n)
- **Space:** O(n)

## Language

Java

## Author

Linga Srilaxmi
