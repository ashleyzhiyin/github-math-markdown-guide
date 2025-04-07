# github-math-markdown-guide
A concise guide to writing math expressions in GitHub-compatible Markdown using LaTeX syntax.
While GitHub's native Markdown lacks full LaTeX support (as found in Jupyter Notebooks), there are still practical techniques to ensure correct rendering of math expressions.
---

### ✅ `README.md` Content (Markdown)

```markdown
# GitHub-Compatible Math in Markdown

This guide documents how to write math expressions using LaTeX-style syntax in Markdown files, with a focus on what is compatible with GitHub rendering.

## Inline Math

Use single dollar signs without spaces:

```markdown
This is an inline formula: $E=mc^2$
```

**Do:** `$E=mc^2$`  
**Don't:** `$ E=mc^2 $`

> GitHub does not render `\(...\)` syntax. Stick with dollar signs.

## Block Math

GitHub-flavored Markdown does **not** natively support block-level math with `$$...$$`.  
However, this can work in environments like:

- Jupyter Notebooks
- GitHub Pages (with MathJax)
- Static site generators (e.g. MkDocs, Docusaurus with plugins)

Example:

```markdown
$$
\sum_{i=1}^n x_i^2
$$
```
If you're working within a regular .md file on GitHub, it's best to stick with inline math ($...$) for reliable rendering.

## Multiline Equations

When using math environments like `aligned`, you can format multi-line equations (in supported renderers):

```latex
\begin{aligned}
y &= mx + b \\
z &= ax^2 + bx + c
\end{aligned}
```

## Tips

- Always keep dollar signs directly next to the math content
- Consider using tools like MathJax or KaTeX for full LaTeX support in rendered pages
- For GitHub README rendering, inline math is safer and more portable

---

Feel free to fork or contribute if you'd like to add more examples or clarify any edge cases.
```
