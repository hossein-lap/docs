# Lua <!--{{{-->

Lua is a powerful, fast, lightweight and embeddable programming language. It is
used by many frameworks, games and other applications. While it can be used
by itself, it has been designed to be easy to embed in another application.
It is implemented in ANSI C, a subset of C programming language that is very
portable, which means it can run on many systems and many devices where the most
other scripting languages would not be able to run.

"Lua" (pronounced LOO-ah) means "Moon" in Portuguese. As such, it is neither an
acronym nor an abbreviation, but a noun.
Lua comes from two languages: DEL and Sol. DEL means "Data Entry Language",
While Sol means "Simple object language" and also means Sun in Portuguese.

One of main advantages of Lua is its simplicity. Programming which is also called
scripting in the case of programs that run inside an embedded applications, is
the process of writing computer program. A programming language is a language
used to give instructions to a computer through computer code that is contained
in a computer program. A programming language consists of two things: a syntax,
which is like grammar in English, and libraries, basic functions provided with
the language. These libraries could be compared with vocabulary in English.

## Hello World! <!--{{{-->

Lua can either be used embedded in an application or by itself.
The first example of Lua code in this book will be the basic and traditional
hello world program.

> A "Hello world" program is a computer program that outputs "Hello, world" on a
> display device. Because it is typically one of the simplest programs possible
> in most programming languages, it is by tradition often used to illustrate
> to beginners the most basic syntax of a programming language, or to verify that
> a language or system is operating correctly.

```lua
print("Hello World!")
```
The code above prints the text Hello, world! to the output, printing referring to
displaying text in the output, not to printing something on paper.
It does so by calling the print function with the string ”Hello, world!”
as an argument.

Note that Lua is most of the time embedded in a lower level application,
which means that the print function will not always display text in an area that
is visible to the user.

<!--}}}-->
## Comments <!--{{{-->

A comment is a code annotation that is ignored by the programming language.
Comments can be used to describe one or many lines of code, to document a program,
to temporarily disable code, or for any other reason. They need to be prefixed by
two hyphens to be recognized by Lua and they can be put either on their own line
or at the end of another line:

```lua
print("This is normal code.")
-- This is a comment
print("This is still normal code.") -- This is a comment at the end of a line of code.
```

These comments are called short comments. It is also possible to create long comments,
which start with a long bracket and can continue on many lines:

```lua
print("This is normal code")
--[[Line 1
Line 2
]]
```

Long brackets consist of two brackets in the middle of which any number of
equality signs may be put. That number is called the level of the long bracket.
Long brackets will continue until the next bracket of the same level, if there is one.

A long bracket with no equal sign is called a long bracket of level 0.
This approach makes it possible to use closing double brackets inside of
long comments by adding equal signs in the middle of the two brackets.
It is often useful to do this when using comments to disable blocks of code.

```lua
--[==[
This is a comment that contains a closing long bracket of level 0 which is here:
 ]]
However, the closing double bracket doesn't make the comment end, because the
  comment was opened with an opening long bracket of level 2, and only a closing
  long bracket of level 2 can close it.
]==]
```

In the example above, the closing long bracket of level 0 (`]]`) does not close the comment,
but the closing long bracket of level 2 (`]==]`) does.

<!--}}}-->
## Syntax <!--{{{-->

The syntax of a programming language defines how statements and expressions must be
written in that programming language, just like grammar defines how sentences and words
must be written. Statements and expressions can be respectively compared to sentences and
words. Expressions are pieces of code that have a value and that can be evaluated, while
statements are pieces of code that can be executed and that contain an instruction and one
or many expressions to use that instruction with. For example, `3 + 5` is an expression and
`variable = 3 + 5` is a statement that sets the value of variable to that expression.

<!--}}}-->
## Obtaining Lua <!--{{{-->

Lua can be obtained on the official Lua website, on the download 
[page](http://www.lua.org/download.html).
Instructions are
also available there: the download button is for the source code, which is probably not what
you want. You are probably looking for binaries, so you should look around the page to find
information about those (what exactly you are looking for depends on the platform you are
using). The purpose of this book is only to teach the Lua language, not to teach usage of
the Lua tools. It is generally assumed that the reader will be using Lua in an embedded
environment, but this does not need to be the case for the book to be useful, only does it
mean that the book will not describe the usage of Lua as a standalone language.

<!--}}}-->
<!--}}}-->
