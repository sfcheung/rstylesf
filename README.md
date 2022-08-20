# rstylesf

My (SF) own coding style for R, to help me collaborate with past-me and future-me.

# Preamble

Adapted for my own situation, such as the devices I usually use, the screen size, the package I usually use,
and my not-so-good memory. If possible, I try not to have a style that relies on packages not in the
standard library, that is, packages not installed along with R. If it is good for me, it is good.

# General Principles

Simple and (generally) consistent.

# Naming

## Case

Use **lowercase letters**. Use uppercase letters when it is really, really natural (to me) to use the uppercase letters.
Should (nearly) never use CamelCase.

```
a <- 1
b <- c(1, 2, 3)
```

## Underscore

Use underscore only to separate words. Do not use dot (`.`) and do not use hyphen (`-`) even if allowed,
unless it is really, really natural to do so.

```
this_is_a_long_name <- c("a", "b", "c")
```

## Length

Long names are OK with me. It is more important to know quickly what a variable is than to type less.

# Strings

Use double quotes, unless there are double quotes in the string.

```
a <- "Hello"
b <- '"Hello"'
```

# Identation

Use two spaces (usually).

```
fct <- function(x) {
    x^2
  }
```

# Align in a readable way

That is ... align in anyway I want.

```
fct <- function(x,
                y1, y2,
                z) {
    x + y1 + y2 + z
  }
```

# Line Length

70 for code. I sometimes work on a small screen. For comments, 70 if possible but it is not a must.

40(!) for documentation and similar text. I sometimes edit files on my mobile phone using GitHub.
The screen is small and no auto-wordwrap. Therefore, I started trying to use 40.

# Whitespace

Always add at least one whitespace before an operator and one whitespace after an operator, except for `^` and similar operators

```
3 + 2
5 * 4
2^2
```

For me, it is OK to add more whitespaces to align elements. It is easier for me to detect typo errors that lead to inconsistent alignment.

```
a     <- 1
b     <- 2
candd <- 3
```

# Indendation within brackets and parentheses

Indent the lines within a pair of brackets or parenthese.

```
fct <- function(
    x,
    y1, y2,
    z
  ) {
    x + y1 + y2 + z
  }

```

NOTE: This example aligns the same code from above in a different way, to illustrate that I do allow inconsistency in the style myself.
