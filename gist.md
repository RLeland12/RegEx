# RegEx

RegEx, what is it?


A regular expression (Regex) are a sequence of characters used to find matching character combinations in text. Per MDN web docs its described as, "Regular expressions are patterns used to match character combinations in strings. In JavaScript, regular expressions are also objects. These patterns are used with the exec() and test() methods of RegExp, and with the match(), matchAll(), replace(), replaceAll(), search(), and split() methods of String."("Regular expressions," 2021).


Summary:
data validation,data scraping,data wrangling,string parsing,string replacement,syntax highlightning
This tutorial will regex and how it works, meant to help the user write and create a regex ;Fields of application range from validation to parsing/replacing strings, passing through translating data to other formats and web scraping..


Anchors-^and$:

^The        matches any string that starts with "The"
end$        matches a string that ends with end
^The end$   exact string match (starts and ends with The end)
roar        matches any string that has the text roar in it



Quantifiers — * + ? and {}

abc*        matches a string that has ab followed by zero or more c
abc+        matches a string that has ab followed by one or more c
abc?        matches a string that has ab followed by zero or one c
abc{2}      matches a string that has ab followed by 2 c
abc{2,}     matches a string that has ab followed by 2 or more c
abc{2,5}    matches a string that has ab followed by 2 up to 5 c
a(bc)*      matches a string that has a followed by zero or more copies of the sequence bc
a(bc){2,5}  matches a string that has a followed by 2 up to 5 copies of the sequence bc



Grouping and capturing — ()

a(bc)           parentheses create a capturing group with value bc
a(?:bc)*        using ?: we disable the capturing group
a(?<foo>bc)     using ?<foo> we put a name to the group




Bracket expressions — []


[abc]            matches a string that has either an a or a b or a c -> is the same as a|b|c
[a-c]            same as previous
[a-fA-F0-9]      a string that represents a single hexadecimal digit, case insensitively
[0-9]%           a string that has a character from 0 to 9 before a % sign
[^a-zA-Z]        a string that has not a letter from a to z or from A to Z. In this case the ^ is used as negation of the expression



OR operator — | or []

a(b|c)     matches a string that has a followed by b or c (and captures b or c)
a[bc]      same as previous, but without capturing b or c



Character classes — \d \w \s and .


\d         matches a single character that is a digit
\w         matches a word character (alphanumeric character plus underscore)
\s         matches a whitespace character (includes tabs and line breaks)
.          matches any character


Flags:


A regex usually comes within this form /abc/, where the search pattern is delimited by two slash characters /. At the end we can specify a flag with these values (we can also combine them each other):

g (global) does not return after the first match, restarting the subsequent searches from the end of the previous match
m (multi-line) when enabled ^ and $ will match the start and end of a line, instead of the whole string
i (insensitive) makes the whole expression case-insensitive (for instance /aBc/i would match AbC)


Character Escapes
, allows us to search for character that is used in regex. Example(/^a, will search for instance of ^a in string)

Author :Robert Leland https://github.com/rleland12
