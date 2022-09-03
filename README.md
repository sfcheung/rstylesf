# rstylesf

My (SF) own coding style for R, to help me collaborate with past-me and future-me.

# Preamble

Adapted for my own situation, such as the devices I usually use, the screen size, the packages I usually use,
and my not-so-good memory. If possible, I try not to have a style that relies on packages not in the
standard library, that is, packages not installed along with R. When I decide whether to adopt a
style, my only concern is whether it is good for me.

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

NOTE: Actually, the reason is for quick double-click selection. With dots, editors I use do not treat
the whole name as one word. It is quite inconvenient to me.

## Length

Long names are OK with me. My memory is not goot. It is more important to know quickly what
a variable is than to type less.

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

NOTE: The reason is the shorter line length I prefer.

# Align in a readable way

That is ... align in anyway I want.

```
fct <- function(x,
                y1, y2,
                z) {
    x + y1 + y2 + z
  }
```

NOTE: Again, the reaons is the shorter line length I prefer.

# Line Length

70 for code. I sometimes work on a small screen. For comments, 70 if possible but it is not a must.

40(!) for documentation and similar content. I sometimes edit files on my mobile phone using GitHub.
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

Indent the lines within a pair of brackets or parenthese. This is not the common style in R but I prefer this one as it makes
the block easier to read, as in Python.

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

# Word Wrap

For documentation, I am totally OK with something like this:

```
This is an example of
a document or
comment, some lines are very long, and
some lines are short.
and the line width is very very
irregular.
```

GitHub monitors changes line-by-line. Reformatting (rewrapping) a paragraph
will result in changes in many lines, even when the actual change is on
one word in one sentence. Reformatting makes me difficult know what changed.
Paragrpah like the one aboe is not that difficult to read, especaily
when I use a line width of about 40 words.
