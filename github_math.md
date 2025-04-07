# GitHub-Compatible Math in Markdown

- This guide documents how to write math expressions using LaTeX-style syntax in Markdown files
- with a focus on what is compatible with GitHub **rendering**.
- While GitHub's native Markdown lacks full LaTeX support (as found in Jupyter Notebooks), there are still practical techniques to ensure correct rendering of math expressions.

## Inline Math

Use single dollar signs without spaces:

```markdown
This is an inline formula: $E=mc^2$
```

**Do:** `$E=mc^2$`  
**Don't:** `$ E=mc^2 $`

> GitHub does not render `\(...\)` syntax. Stick with dollar signs.

## Block Math

### Dollar Signs on Separate Lines (Block Math)
When writing block-level math expressions, the dollar signs ($$) should each be placed on their own line, with the equation between them. 
This format is required for proper rendering in environments like Jupyter Notebook or MathJax-based renderers.

### There is also a line break after the line break character \\, don't write it right next to each other

Example:

```markdown
$$
A = \begin{bmatrix}
a_{11} & a_{12} & \dots & a_{1n} \\
a_{21} & a_{22} & \dots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m1} & a_{m2} & \dots & a_{mn}
\end{bmatrix}
$$
```

### Spaces Between Dollar Signs and Text (Inline Math)
leave spaces between the formula and surrounding text to avoid rendering issues.

Correct usage:
```markdown

Given a matrix $A$ of dimensions $m \times n$, the SVD is given by:

$$
A = U \Sigma V^T
$$

```
In this example:
- $A$ is inline math, with no space inside the dollar signs.
- The block-level formula for SVD is wrapped properly with $$ on separate lines.

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
