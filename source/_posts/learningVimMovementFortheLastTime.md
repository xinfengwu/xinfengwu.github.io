---
title: Learning Vim Movement For the Last Time
date: 2023-08-24 23:45:03
tags:
---

In this page, I summarized the Vim movement commands which are important.
# Basic motions

- `j`: move down one line
- `k`: move up one line
- `h`: move left one character
- `l`: move right one character

# Moving by Word 

- `w` : Moves the cursor to the beginning of the next word
- `W` : Moves the cursor to the beginning of the next word (using spaces)
- `e` : Moves the cursor to the end of the next word
- `E` : Moves the cursor to the end of the next word (using spaces)
- `b` : Moves the cursor to the beginning of the previous word
- `B` : Moves the cursor to the beginning of the previous word (using spaces)
- `ge` : Moves the cursor to the end of the previous word
- `gE` : Moves the cursor to the end of the previous word (using spaces)

# Moving within the Line(s)

Vim also provides quick ways to move the cursor based on a search character.

- `f`  :  Moves the forward cursor to the first occurrence of a character in the current line
- `t`  :  Moves the forward cursor to right before the first occurrence of a character in the current line
- `F`  :  Moves the backward cursor to the first occurrence of a character in the current line
- `T`  :  Moves the backward cursor to right before the first occurrence of a character in the current line
- `;`  : Repeats a f/t/F/T command in the same direction
- `,`  :  Repeats a f/t/F/T command in the reverse direction

**Moving to a Specific Line**

`:set number`

`:set nonumber`

`[count]G` == `[count]gg` Goto line [count], default first line, on the first non-blank character linewise.

## **Moving to the Beginning of a Line**

- `0` : Moves the cursor to the line's first column
- `^` :  Moves the cursor to the line's first non-whitespace character
- `I` : Like ^, but also enters into edit mode (mnemonic: "Insert at the beginning of a line")
- `S` : Like "I", but it erases the entire line (mnemonic: "Substitute a line")
- `o` :  Like "I", but moves the cursor the beginning of the line below, inserting a new line
- `O` :  Like "I", but moves the cursor the beginning of the line above, inserting a new line

## **Moving to the End of a Line**

- `$` : Moves the cursor to the end of a line
- `A` : Like "$", but also enters into edit mode (mnemonic: "Append to a line")

# Moving by Sentence, Paragraph or Section

**Troff-Related Movement**

`)` : move forward one sentence

`(` : move backward one sentence

`}` : move forward one paragraph

`{` : move backward one paragraph

**Section Movement**

`[[` : [count] section backward or to the previous ‘{’ in the first column

`[]` : [count] section backward or to the previous ‘}’ in the first column

`]]` : [count] section forward or to the next ‘{’ in the first column

`][` : [count] section forward or to the next ‘}’ in the first column

**Method Location**

`[m` : Go to [count] previous start of a method(for Java or similar structured language)

`[M` : Go to [count] previous end of a method(for Java or similar structured language)

`]m` : Go to [count] next start of a method(for Java or similar structured language)

`]M` : Go to [count] next end of a method(for Java or similar structured language)

# **Moving within the Screen**

- `H`: move to the top of the screen(mnemonic: "High")
- `M`: move to the middle of the screen(mnemonic: "Middle")
- `L`: move to the bottom of the screen(mnemonic: "Low")
- `^U`: move up half a screen
- `^D`: move down half a screen

# ****Moving to the Beginning and End of a Document****

- `gg`: Moves the cursor to beginning of the document
- `G`: Moves the cursor to the start of the document's last line. You must use "G$" to get to the true end of the document
- `^F`: page down
- `^B`: page up

# Moving Between Tab Pages

`:help tabpage`

**Moving between Tab Pages**

`gt` : Go to the next tab page. Wraps around from the last to the first one.

`gT` : Go to the previous tab page. Wraps around from the first to the last one.

**Moving Tab Pages left and right**

`:tabm [N]` : Move the current tab page to after tab page N.

`:tabm +[N]`

`:tabm -[N]` : Move the current tab page N places to the right (with +) or to the left (with -)

`:tabs` : List the tab pages and the windows they contain.

# Moving Between Windows

`:help ctrl-w`

**Moving Between Windows**

`ctrl-w j` : Go to Nth window below current one.

`ctrl-w k` : Go to Nth window above current one.

`ctrl-w h` : Go to Nth window left current one.

`ctrl-w l` : Go to Nth window right current one.

# Go Back to a File

`Ctrl + ^` : Edit [count]th file in the buffer list
