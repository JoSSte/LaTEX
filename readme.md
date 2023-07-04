Disclaimer: I'm git savvy not LaTeX savvy. this is my first LaTeX document ever.

That said, This is how I would do it (inspired by https://stackoverflow.com/questions/3655454/conditional-import-in-latex)

I would split my document up into sections. I have chosen header, footer, resume and references in this case:

Then I made two .tex files:

## withReferences.tex
see [withReferences.tex](withReferences.tex)
```latex
\include{header}
\include{resume}
\include{references}
\include{footer}
```

## withoutReferences.tex
see [withoutReferences.tex](withoutReferences.tex)
```latex
\include{header}
\include{resume}
\include{footer}
```

When you compile the `withReferences.tex` file you get the complete document, if you compile the `withoutReferences.tex` you get the document without the references. This gives you one set of files to maintain.

## Example files I used to test:
* [header.tex](header.tex)
* [footer.tex](footer.tex)
* [resume.tex](resume.tex)
* [references.tex](references.tex)
