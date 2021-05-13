<!-- 
cd '' ;
pandoc -o _SmallSample.tex SmallSample.md ; 
latexmk -pdf SmallSample.tex 
\input{_SmallSample.tex}
-->

<!-- This is a comment. It will not appear in the final content -->


# Markdown

##  Simple Structure

Text in Markdown uses `#` at the beginning of a line to indicate headings. 
`#` = heading.
`##` = sub-heading.
`###` = sub-sub-heading, and so on.

##  On Sentences
Text does not have to be formated in traditional paragraph form.
LaTeX will properly format blocks of text that are separated by more than 2 lines. 

Having each sentence start at the beginning of a line, is a useful in many ways.
It shows paragraph structure more clearly.
It shows how long your sentences are.
It makes it easy to find the right sentence when editing,
It is easy to shift a sentence into a new position in the paragraph.

Putting different elements of a sentence on separate lines is also possible.
This can
	highlight sentence structure,
	build confidence that the commas are in the right place, and
	still compile into a normal looking sentence.

# Using \LaTeX

\textcite{lamport1994latex} is one of the first, and still most widely cited books on LaTeX.
With some LaTeX knowledge, sprinkle it throughout the document provides great effect.
Math like $e=mc^2$, for example, looks terrific when formatted in LaTeX.
