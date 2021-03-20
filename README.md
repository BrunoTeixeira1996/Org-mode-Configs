# My Emacs Org-mode configs

`This is just a repo to old some org-mode configs to create reports faster`

## Steps to make this work

**First put this lisp code in your** `init.el`

```lisp
(with-eval-after-load 'ox-latex
  (add-to-list 'org-latex-classes
               '("org-plain-latex"
                 "\\documentclass{article}
                   [NO-DEFAULT-PACKAGES]
                   [PACKAGES]
                   [EXTRA]"
                ("\\section{%s}" . "\\section*{%s}")
                 ("\\subsection{%s}" . "\\subsection*{%s}")
                 ("\\subsubsection{%s}" . "\\subsubsection*{%s}")
                 ("\\paragraph{%s}" . "\\paragraph*{%s}")
                 ("\\subparagraph{%s}" . "\\subparagraph*{%s}")))
  )
```



**If you need to change the output format, language, styling , just change the** `setup.org` **file in** `setup` **folder**

**In the** `tests` **folder there are some example of pdf outputs**

**In the** `skeleton` **folder is where we focus to build a report**

## Note

Dont forget to change the `setup` file location
