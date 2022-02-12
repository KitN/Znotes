# Pep - 8 Style notes
[https://www.python.org/dev/peps/pep-0008/](https://www.python.org/dev/peps/pep-0008/)

## General Thoughts
Learned a lot from this. Some of it still goes over my head because of a lack of familiarity with the higher level organization of modules, classes, libraries etc. etc.
Bit by bit, a cup is filled

## Table of Contents
* [Introduction](https://www.python.org/dev/peps/pep-0008/#introduction)
* [A Foolish Consistency is the Hobgoblin of Little Minds](https://www.python.org/dev/peps/pep-0008/#a-foolish-consistency-is-the-hobgoblin-of-little-minds)
    * There are good reasons to ignore style Conventions!
        * e.g. backwards compatibility
* [Code Lay-out](https://www.python.org/dev/peps/pep-0008/#code-lay-out)
    * [Indentation](https://www.python.org/dev/peps/pep-0008/#indentation)
        * Python's implicit line joining inside parentheses, brackets and braces,
        * alight vertically when u do this
        * **OR** use a _hanging indent_
    * [Tabs or Spaces?](https://www.python.org/dev/peps/pep-0008/#tabs-or-spaces)
        * JUST TABS (unless backwards compatiblity is imptnt)
    * [Maximum Line Length](https://www.python.org/dev/peps/pep-0008/#maximum-line-length)
        * 79 in general
        * **72 for docstrings etc.** since you have options
        * Long lines can be broken over multiple lines by wrapping expressions in parentheses. These should be used in preference to using a backslash for line continuation.
    * [Should a Line Break Before or After a Binary Operator?](https://www.python.org/dev/peps/pep-0008/#should-a-line-break-before-or-after-a-binary-operator)
        * Donald Knuth explains the traditional rule in his _Computers and Typesetting_ series: "Although formulas within a paragraph always break after binary operations and relations, displayed formulas always break before binary operations" [\[3\]](https://www.python.org/dev/peps/pep-0008/#id7).
        * Following the tradition from mathematics usually results in more readable code:
    * [Blank Lines](https://www.python.org/dev/peps/pep-0008/#blank-lines)
        * Python accepts the control-L (i.e. ^L) form feed character as whitespace;
        * **What is this character?**
    * [Source File Encoding](https://www.python.org/dev/peps/pep-0008/#source-file-encoding)
    * [Imports](https://www.python.org/dev/peps/pep-0008/#imports)
        * Imports should be grouped in the following order:
            1.  Standard library imports.
            2.  Related third party imports.
            3.  Local application/library specific imports
      * You should put a blank line between each group of imports.
    * [Module Level Dunder Names](https://www.python.org/dev/peps/pep-0008/#module-level-dunder-names)
        * (i.e. names with two leading and two trailing underscores) such as \_\_all\_\_, \_\_author\_\_, \_\_version\_\_, etc. **DUNDERS**
* [String Quotes](https://www.python.org/dev/peps/pep-0008/#string-quotes)
    * pick a kind and stick with it
* [Whitespace in Expressions and Statements](https://www.python.org/dev/peps/pep-0008/#whitespace-in-expressions-and-statements)
    * [Pet Peeves](https://www.python.org/dev/peps/pep-0008/#pet-peeves)
    * [Other Recommendations](https://www.python.org/dev/peps/pep-0008/#other-recommendations)
        * onsider adding whitespace around the operators with the lowest priority(ies). Use your own judgment; however, never use more than one space, and always have the same amount of whitespace on both sides of a binary operator:
       * ```py    
        i = i + 1
        submitted += 1
        x = x*2 - 1
        hypot2 = x*x + y*y
        c = (a+b) * (a-b)
     ```
     
* [When to Use Trailing Commas](https://www.python.org/dev/peps/pep-0008/#when-to-use-trailing-commas)
    * mandatory when making a tuple of one element.
* [Comments](https://www.python.org/dev/peps/pep-0008/#comments)
    * Comments should be complete sentences. The first word should be capitalized, unless it is an identifier that begins with a lower case letter (never alter the case of identifiers!).
    * [Block Comments](https://www.python.org/dev/peps/pep-0008/#block-comments)
    * [Inline Comments](https://www.python.org/dev/peps/pep-0008/#inline-comments)
        * Inline comments are unnecessary and in fact distracting if they state the obvious. Don't do this:
    * [Documentation Strings](https://www.python.org/dev/peps/pep-0008/#documentation-strings)
* [Naming Conventions](https://www.python.org/dev/peps/pep-0008/#naming-conventions)
    * [Overriding Principle](https://www.python.org/dev/peps/pep-0008/#overriding-principle)
    * [Descriptive: Naming Styles](https://www.python.org/dev/peps/pep-0008/#descriptive-naming-styles)
    * [Prescriptive: Naming Conventions](https://www.python.org/dev/peps/pep-0008/#prescriptive-naming-conventions)
        * [Names to Avoid](https://www.python.org/dev/peps/pep-0008/#names-to-avoid)
        * [ASCII Compatibility](https://www.python.org/dev/peps/pep-0008/#ascii-compatibility)
        * [Package and Module Names](https://www.python.org/dev/peps/pep-0008/#package-and-module-names)
        * [Class Names](https://www.python.org/dev/peps/pep-0008/#class-names)
        * [Type Variable Names](https://www.python.org/dev/peps/pep-0008/#type-variable-names)
        * [Exception Names](https://www.python.org/dev/peps/pep-0008/#exception-names)
        * [Global Variable Names](https://www.python.org/dev/peps/pep-0008/#global-variable-names)
        * [Function and Variable Names](https://www.python.org/dev/peps/pep-0008/#function-and-variable-names)
        * [Function and Method Arguments](https://www.python.org/dev/peps/pep-0008/#function-and-method-arguments)
        * [Method Names and Instance Variables](https://www.python.org/dev/peps/pep-0008/#method-names-and-instance-variables)
        * [Constants](https://www.python.org/dev/peps/pep-0008/#constants)
        * [Designing for Inheritance](https://www.python.org/dev/peps/pep-0008/#designing-for-inheritance)
    * [Public and Internal Interfaces](https://www.python.org/dev/peps/pep-0008/#public-and-internal-interfaces)
* [Programming Recommendations](https://www.python.org/dev/peps/pep-0008/#programming-recommendations)
    * Comparisons to singletons like None should always be done with is or is not, never the equality operators.
    * [Function Annotations](https://www.python.org/dev/peps/pep-0008/#function-annotations)
    * [Variable Annotations](https://www.python.org/dev/peps/pep-0008/#variable-annotations)
* [References](https://www.python.org/dev/peps/pep-0008/#references)
* [Copyright](https://www.python.org/dev/peps/pep-0008/#copyright)

