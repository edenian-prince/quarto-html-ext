# quarto template

I've been reusing the same css styles for almost every project, so I figured it was time to make a quarto template out of it. Feel free to use this for your htmls.

Please see this github page for install instructions and the style guide https://edenian-prince.github.io/quarto-html-ext/

# Install

in a terminal, navigate to the root of your quarto project and execute this:

`quarto add edenian-prince/quarto-html-ext/nwpage`

if you're making a site or project, adjust the front matter `_quarto.yml` to have `format: nwpage-html` like this:

```
project:
  type: website

website:
  title: "codebook"
  navbar:
    left:
      - href: index.qmd
        text: Home
      - about.qmd

format:
  nwpage-html:
    toc: true
```

if you just have a single document, put this in the front matter of the .qmd file like this:

```
---
title: single qmd doc
format:
  nwpage-html: default
---
```

or to create a project with the template as a base, do this (i don't really recommend this..):

`quarto use template edenian-prince/quarto-html-ext/nwpage`
