# apa7-md2latex

[![hackmd-github-sync-badge](https://hackmd.io/y_0QmFQ2TO6rm7swFpaf_g/badge)](https://hackmd.io/y_0QmFQ2TO6rm7swFpaf_g)


While working on my MBA for the University of Fredericton, I came up with a way of writing that fits my tech temperament.
The writing process itself is very simple:
 
![](https://github.com/wrashi/apa7-md2latex/blob/main/md.png?raw=true)

Several tools and processes are required to make it all work.
Once mastered, though, the results are a stunning paper, properly formatted with no effort, every time.

##  Why Use Markdown?

90% of the difficulty of writing is the content.
Yet too many people get caught up in the formatting and make that 90% of their work.
They fuss over font size, whether to use bold or italics, one space or two, and on and on.
When confronted with APA 7 versus APA 6 in academic writing, an almost infinite amount of time can get sucked up fast!

As humanity becomes an internet species, Markdown is taking its place in many people's writing.
Its simple formatting and ease of reading and writing for both humans and machines makes it increasingly popular.
Using style sheets (e.g. CSS) allow the same content to appear dramatically different without changing the underlying structure.

Since 90-95% of academic writing is simple text and headings, Markdown is a great tool.

When writing with groups, Markdown allows everyone to focus on structure and content.
Because Markdown is simple text, there are a lot of great tools, like GitHub, for collaborative work.


##  Why Use $\LaTeX$?

LaTeX is a technology that turns properly structured text into gorgeous output. 
It makes all the formatting decisions according to the latest versions of the rules.
Need a cover page? Covered.
Add an abstract? Simple.
Worried about formatting references? Handled for you.

But let's be real.
LaTeX is complicated, hard to type and easy to mess up.
Which is why writing in a simple format like Markdown and then translating it into LaTeX is so beneficial.

Once you learn some LaTeX, though, you can sprinkle it throughout your document to great effect.
Math like $e=mc^2$, for example, looks terrific when formatted in LaTeX.

**NB**
Text editors like TextMate have great built-in LaTeX functionality (e.g. create PDF with `command-r`).



##  Why Use BibLaTeX?

BibLaTeX formats your citations and references according to the latest version of APA 7.
Using `\parencite{}` for citations with the author name within parentheses and `\textcite{}` with the author name and year in parentheses is a straightforward way to make sure to get it right.

In many cases, things you want to cite already have BibLaTeX citation information that you can just copy.
For example, Google Scholar's cite window has BibTeX (the same as BibLaTeX for our purposes) at the bottom.


# Getting Started

- [ ] Make sure you have the requirements installed
- [ ] Download & modify the template folder & files.


##  Installing Requirements

If you're on a Mac and have [Homebrew](https://brew.sh/ "The Missing Package Manager for macOS (or Linux) — Homebrew") installed, it is far and away the easiest way to install these packages.

- $\LaTeX$ (with APA7 package)
- Pandoc
- LaTeXmk (optional, but recommended)

##  How to Use The Template

This section refers to two `.tex` documents.
The "secondary" one has a `_` underscore at the beginning of the name and receives the translation from Markdown.
The "main" one doesn't have the underscore. 
The "main" file is the one that gets compiled.

1. Change the filenames, as desired
	- all filenames should be the same, except the secondary `.tex` file which should start with an underscore.
	- Not having spaces in your filename will avoid a lot headache.
1. Change the content in the main `.tex` file to include 
	your name,
	the name of the course,
	the instructor's name,
	the due date.
1. If you changed the file name, change the line `\input{_Template.tex}` to match the new filename
1. Write your content in the `.md` file
1. Translate the Markdown file with `Pandoc` in the Terminal (e.g. `pandoc -o _Template.tex Template.md`) where "Template" is your filename.
	`-o` in the name of the output file. 
	Pandoc can create many types of files and uses the extension you use with `-o` to determine what kind of document to create (e.g. `-o _Template.doc` for a Word document).
1. Compile the main `.tex` document
	- If your text editor supports it, the command will be something like "Typeset" or "Build". The shortcut key is often `command-r`.
	- If building in the Terminal, `latexmk -pdf Template.tex` where "Template" is the new filename.

##  How it Works

Inside the folder, the documents are named (almost) the same.
You can change the name to anything as long as you keep 2 things: the extensions (i.e. `.md` and `.tex`) and the underscore (`_`) at the beginning of the 1 `.tex` file.
The `.md` file is where the body of your writing goes.
The main `.tex` file is where the header information for LaTeX goes, and this is the file that you compile

After writing Markdown in the `.md` file, use `pandoc` to translate it into LaTeX.
The translated content will be placed in the file starting with `_`.

# Advanced Use Cases

##  Stitching Together Multiple Documents
LaTeX is very flexible and powerful.
If everyone writes their piece in a separate document, the LaTeX header document can stitch them all together seamlessly.
Just use `\input{FILENAME.tex}` for each file to be included.

##  Output to Word

$\LaTeX$ expects to output PDF or similar formats. 
Pandoc can be create Word documents formatted according to a template, like the one provided during the UFred orientation.
After producing the PDF, try the following.

	pandoc --citeproc SmallSample.tex --bibliography=bibliography.bib --reference-doc=~/UFred/Orientation/2019-10-20\ APA\ format\ template.docx -o SmallSample.docx

# Small Sample

A small example is included in the sample folder.

