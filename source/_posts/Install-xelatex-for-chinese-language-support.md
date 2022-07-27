---
title: Install xelatex for chinese language support
date: 2022-07-26 20:39:50
tags:
---
# Why Xelatex?

We all know that latex(pdfTex) is a wonderful tool for anyone who is interested in academic writing. However, its support for languages apart from English is not as great as those for other part. Anyway, xelatex(xeTex) is an alternative choice. Below are the instructions for downloading xelatex.(For Ubuntu Only)

# Install

Of course, all you need is included in texlive. However, Ubuntu's support for tex is quite broke, so I suggest you follow the instructions given by https://tug.org/texlive/acquire.html. 

If you encounter some problems about latexmk, try the following command.
```shell
sudo apt install latexmk
```

# Something else for Vscode Users

If you want to change the configurations for vscode so that you can use the favourite ide for tex writing, do the following things.

1. Install extensions, including "Latex", "Latex language support" and "Latex Workshop". 

2. Edit settings.json. Add this into settings:
```json
  "latex-workshop.latex.tools": [{
    "name": "latexmk",
    "command": "latexmk",
    "args": [
        "-xelatex",
        "-synctex=1",
        "-interaction=nonstopmode",
        "-file-line-error",
        "%DOC%"
    ]
  }],
```

3. Now you may be happy to find that your vscode has turned to one smart tex-writer!