---
##  simple.md  adapted from
##  simple.tex - A simple article to illustrate document structure.
##
##  Andrew Roberts - June 2003

title: How to Structure a LaTeX Document
author:
  name: Andrew Roberts
  address: School of Computing,\
           University of Leeds,\
           Leeds,\
           United Kingdom,\
           LS2 1HE
  email: andyr@comp.leeds.ac.uk  
date:   June 2003

abstract: >
  In this article, I shall discuss some of the fundamental topics in
  producing a structured document.  This document itself does not go into
  much depth, but is instead the output of an example of how to implement
  structure. Its LaTeX source, when in used with my tutorial
  (http://www.comp.leeds.ac.uk/andyr/misc/latex/\-latextutorial2.html)
  provides all the relevant information.

---



## Introduction

This small document is designed to illustrate how easy it is to create a
well structured document within LaTeX [@lamport94].  You should quickly be able to
see how the article looks very professional, despite the content being
far from academic.  Titles, section headings, justified text, text
formatting etc., is all there, and you would be surprised when you see
just how little markup was required to get this output.

## Structure

One of the great advantages of LaTeX is that all it needs to know is
the structure of a document, and then it will take care of the layout
and presentation itself.  So, here we shall begin looking at how exactly
you tell LaTeX what it needs to know about your document.

### Top Matter

The first thing you normally have is a title of the document, as well as
information about the author and date of publication.  In LaTeX terms,
this is all generally referred to as *top matter*.

#### Article Information

* `\title{title}` - The title of the article.
* `\date`         - The date. Use:
  * `\date{\today}` - to get the date that the document is typeset.
  * `\date{date}`   - for a specific date.
  * `\date{}`       - for no date.

#### Author Information

The basic article class only provides the one command:

* `\author` - The author of the document.

It is common to not only include the author name, but to insert new
lines (`\\`) after and add things such
as address and email details.  For a slightly more logical approach, use
the AMS article class (`amsart`) and you have the following extra
commands:

* `\address` - The author's address.  Use the new line command (`\\`) for line breaks.
* `\thanks`  - Where you put any acknowledgments.
* `\email`   - The author's email address.
* `\urladdr` - The URL for the author's web page.


### Sectioning Commands

The commands for inserting sections are fairly intuitive.  Of course,
certain commands are appropriate to different document classes.
For example, a book has chapters but a article doesn't.

| Command                         | Level |
| ------------------------------- | ----- |
| `\part{part}`                   |  -1   |
| `\chapter{chapter}`             |   0   |
| `\section{section}`             |   1   |
| `\subsection{subsection}`       |   2   |
| `\subsubsection{subsubsection}` |   3   |
| `\paragraph{paragraph}`         |   4   |
| `\subparagraph{subparagraph}`   |   5   |


Numbering of the sections is performed automatically by LaTeX, so don't
bother adding them explicitly, just insert the heading you want between
the curly braces.  If you don't want sections number, then add an asterisk (\*) after the
section command, but before the first curly brace, e.g.,
`\section*{A Title Without Numbers}`.


<!-- 
%Create the environment for the bibliography.  Since there is only one
%reference, set the label width to be one character (I shall follow
%convention as use the number '9'.  This is because it helps to remind
%that it is the maximum number of refs that is now permitted by that
%width).
\begin{thebibliography}{9}
%The \bibitem is to start a new reference.  Ensure that the cite_key is
%unique.  You don't need to put each element on a new line, but I did
%simply for readability.
	\bibitem{lamport94}
	  Leslie Lamport,
	  \emph{\LaTeX: A Document Preparation System}.
	  Addison Wesley, Massachusetts,
	  2nd Edition,
	  1994.

\end{thebibliography} %Must end the environment
-->
