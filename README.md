# Markdown vs LaTeX / TeX Markup

_Markdown vs Markup_



## Article

```latex
\documentclass{article}

\begin{document}
Hello world!
\end{document}
```

vs

```
Hello world!
```

</>

```latex
\documentclass{article}
\title{How to Structure a LaTeX Document}
\author{Andrew Roberts}
\date{December 2016}
\begin{document}
   \maketitle
   Hello world!
\end{document}
```

vs

```
---
title:  How to Structure a LaTeX Document
author: Andrew Roberts
date:   December 2016
---

Hello world!
```

</>


## Book

```latex
\documentclass{book}
\begin{document}

\chapter{Introduction}
This chapter's content...

\section{Structure}
This section's content...

\subsection{Top Matter}
This subsection's content...

\subsubsection{Article Information}
This subsubsection's content...
\end{document}
```

vs

```
# Introduction

This chapter's content...

## Structure

This section's content...

### Top Matter

This subsection's content...

#### Article Information

This subsubsection's content...
```

</>


## Inline Text Formatting

```latex
A \textbf{bold \textit{Hello LaTeX}} to start!
```

vs

```
A **bold _Hello LaTeX_** to start!
```

</>


## Verbatim Text

```latex
\begin{verbatim}
The verbatim environment
  simply reproduces every
 character you input,
including all  s p a c e s!
\end{verbatim}
```

vs

```
····The verbatim environment
····  simply reproduces every
···· character you input,
····including all  s p a c e s!
```

</>


## Bullet List

```latex
\begin{itemize}  
\item The first item
\item The second item
\item The third etc.
\end{list_type}
```

vs

```
* The first item
* The second item
* The third etc.
```

</>


## Numbered List

```latex
\begin{enumerate}  
\item The first item
\item The second item
\item The third etc.
\end{list_type}
```

vs

```
1. The first item
2. The second item
3. The third etc.
```

</>

```latex
\begin{enumerate}  
\item The first item
\begin{enumerate}
\item Nested item 1
\item Nested item 2
\end{enumerate}
\item The second item
\item The third etc.
\end{list_type}
```

vs

```
1. The first item
   a. Nested item 1
   b. Nested item 2
2. The second item
3. The third etc.
```

</>



## Simple Table

```latex
\begin{tabular}{ l l l }
  Day & Min Temp & Max Temp \\
  Monday & 11° C & 22° C \\
  Tuesday & 9° C & 19° C \\
  Wednesday & 10° C & 21° C \\
\end{tabular}
```

vs

```
Day       | Min Temp | Max Temp
--------- | -------- | --------
Monday    |  11° C   |  22° C
Tuesday   |   9° C   |  19° C
Wednesday |  10° C   |  21° C
```

</>


