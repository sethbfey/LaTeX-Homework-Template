# LaTeX Homework Template

A minimalistic, modular LaTeX class and style collection designed for university homework.

See [`template.pdf`](template.pdf) for a compiled example.

## Repository Structure

* **`myhw.cls`**: Document class built on `article`. Handles page geometry, the title page, and the `exercise`/`solution` environments.
* **`mymath.sty`**: Loads math packages and defines custom commands and theorem environments.
* **`mycs.sty`**: Loads `minted` for syntax-highlighted code and `algpseudocode` for pseudocode.
* **`mytikz.sty`**: The graphics toolkit. Pre-loads `tikz`, `pgfplots`, `graphicx`, and layout packages like `float` and `caption`.
* **`template.tex`**: A blank boilerplate file to quickly spin up a new assignment.

## Installation

To make these files globally available to all your LaTeX projects without cluttering your working directories, clone or copy them into your local `texmf` tree.

**macOS / Linux (TeX Live)**
```bash
~/Library/texmf/tex/latex/local/latex-homework-template/
```

**Windows (TeX Live)**
```
C:\Users\<username>\texmf\tex\latex\local\latex-homework-template\
```

**Windows (MiKTeX)**
```
C:\Users\<username>\AppData\Local\MiKTeX\tex\latex\local\latex-homework-template\
```

*Note: Depending on your TeX distribution, you may need to run `mktexlsr` (or `texhash`) to update the file database.*

## Usage

Create a new `.tex` file, use `myhw` as your document class, and pull in only the style packages you need for that assignment:

```latex
\documentclass{myhw}

\usepackage{mymath} % optional
\usepackage{mycs}   % optional
\usepackage{mytikz} % optional
```

See `template.tex` for a full working example.

### Title Page Fields

| Command | Description |
|---|---|
| `\school{...}` | University or institution name |
| `\semester{...}` | Semester and year |
| `\course{...}` | Course number and name |
| `\instructor{...}` | Instructor name |
| `\student{...}` | Student name |
| `\duedate{...}` | Due date |
| `\title{...}` | Assignment title |

### Environments

| Environment | Description |
|---|---|
| `\begin{exercise}{n}` | Numbered exercise block with horizontal rule dividers |
| `\begin{solution}` | Solution block; clears to a new page on close |
