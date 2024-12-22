# rstylesf

My (SF) own coding style for R, helps me collaborate with past-me and future-me.

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

```r
a <- 1
b <- c(1, 2, 3)
```

## Underscore

Use underscore only to separate words. Do not use dot (`.`) and do not use hyphen (`-`) even if allowed,
unless it is really, really natural to do so.

```r
this_is_a_long_name <- c("a", "b", "c")
```

NOTE: Actually, the reason is for quick double-click selection. With dots, the editors I use do not treat
the whole name as one word. It is quite inconvenient to me.

## Length

Long names are OK with me. My memory is not good. It is more important to know quickly what
a variable is than to type less.

# Strings

Use double quotes, unless there are double quotes in the string.

```r
a <- "Hello"
b <- '"Hello"'
```

# Indentation

Use two spaces (usually).

```r
fct <- function(x) {
    x^2
  }
```

or

```r
fct <- function(x) {
  x^2
}
```

NOTE: The reason is the shorter line length I prefer.

# Align in a readable way

That is, align in any way I want.

```r
fct <- function(x,
                y1, y2,
                z) {
    x + y1 + y2 + z
  }
```

or

```r
fct <- function(x,
                y1, y2,
                z) {
  x + y1 + y2 + z
}
```

NOTE: Again, the reason is the shorter line length I prefer.

# Line Length

70 for code. I sometimes work on a small screen. For comments, 70 if possible but it is not a must.

40(!) for documentation and similar content. I sometimes edit files on my mobile phone using GitHub.
The screen is small and has no auto-word-wrap. Therefore, I started trying to use 40.

# Whitespace

Always add at least one whitespace before an operator and one whitespace after an operator, except for `^` and similar operators

```r
3 + 2
5 * 4
2^2
```

For me, it is OK to add more white spaces to align elements. It is easier for me to detect typo errors that lead to inconsistent alignment.

```r
a     <- 1
b     <- 2
candd <- 3
```

# Indendation within brackets and parentheses

Indent the lines within a pair of brackets or parentheses:

```r
fct <- function(
    x,
    y1, y2,
    z
  ) {
    x + y1 + y2 + z
  }
```

or

```r
fct <- function(
  x,
  y1, y2,
  z
) {
  x + y1 + y2 + z
}
```

NOTE: This example aligns the same code from above in a different way, to illustrate that I allow inconsistency in the style myself.

NOTE: I now resort to the more popular C-style indentation for new code,
though I may keep the Python-style indentation for old code for consistency.
I now have more and more work in collaboration with others and it may be better
to follow the norm in this regard.

# Word Wrap

For documentation, I am totally OK with something like this:

```r
# This is an example of
# a document or
# comment, some lines are very long, and
# some lines are short.
# and the line width is very very
# irregular.
```

GitHub monitors changes line-by-line. Reformatting (rewrapping) a paragraph
will result in changes in many lines, even when the actual change is in
one word in one sentence. Reformatting makes it difficult to know what changed.
Paragraphs like the one above are not that difficult to read, especially
when I use a line width of about 40 words.
