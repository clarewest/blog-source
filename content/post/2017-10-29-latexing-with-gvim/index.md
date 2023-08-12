---
title: Latexing with gvim
author: CE West
date: '2017-10-29'
slug: latexing-with-gvim
categories:
  - personal
tags:
  - latex
  - coding
meta_img: images/image.png
description: How to use latex without a GUI
---

Here I’ll share my set-up for writing Latex with gvim instead of a separate Latex editor. If you are text-editor averse, this blog post is not for you. But if, like me, you love vim and hate useless GUIs, this might be helpful.

<!--more-->

Until now, I’ve been happily using TexMaker for writing, but during a recent period of intense Latexing I started to find the useable screen space oppressively small. The unnecessary GUI had to go.   

<div class="figure">

![Number of structures in the PDB](https://www.blopig.com/blog/wp-content/uploads/2017/10/Screen-Shot-2017-10-29-at-20.53.42.png?w=1250&ssl=1)

<p class="caption">No offence TexMaker but I don’t like you</p>

</div>

One of our good friends in [Statistical Genetics](http://www.stats.ox.ac.uk/~myers/) recommended some things to help me with the transition to just using good old (g)vim, which I will now recommend to you.

The key thing is the [LaTex-Box plug-in](https://github.com/LaTeX-Box-Team/LaTeX-Box) for vim, which gives you the compilation commands, as well as the essentials such as smart indentation, highlight matching, command completion, etc. I used pathogen to install it (see the GitHub for instructions).

Of course, you can then customise your `.vimrc` file to add more helpful things. This can be the simple preferences, such as using a light background when using gvim:

```bash
if has(“gui_running”)
        set background=light
endif
```

You can also do more complicated magic like tabbing through available commands, and the ability to minimise sections, etc. Sidenote: to make working with paragraphs easier, I recommend setting the up/down arrows to move the cursor to the next line in the GUI rather than the next actual line. I prefer overriding this behaviour only in gvim, while leaving the normal behaviour in vim (for actual coding). But each to their own.

To get started, open a `.tex` file, then compile and view the document with the command `Latexmk`.

<div class="figure">

![Basic forms diagram](https://www.blopig.com/blog/wp-content/uploads/2017/10/Screen-Shot-2017-10-29-at-20.51.47.png?w=524&ssl=1)

<p class="caption">Command suggestions are an example of a magical feature added in .vimrc</p>

</div>

The configurations for this command are set in the file `.latexmkrc`. Mine looks like this:

```bash
$recorder = 1;
$pdf_mode = 1;
$bibtex_use = 2;
$pdflatex = "pdflatex --shell-escape %O %S";
$pdf_previewer = "start open -a skim %O %S";
```

My pdf viewer of choice on Mac is Skim, which autoupdates. I view the source and preview at the same time using split view. Please admire the beauty below:

<div class="figure">

![Basic forms diagram](https://i0.wp.com/www.blopig.com/blog/wp-content/uploads/2017/10/Screen-Shot-2017-10-21-at-18.53.34.png?w=1250&ssl=1)

<p class="caption">Wow what a beautiful screen

</p>

</div>

My favourite part is that whenever you save (w), it recompiles and updates the preview. As someone who accidentally types :w everywhere that isn’t vim, it’s nice that this is now productive. It also recompiles automatically if the .bib file is updated. Note that if you have errors at compilation (I’m sure you don’t), you can view them with the command LatexErrors.

Now you too can be a (nearly) GUI-free lightweight Latexer. Enjoy!

*This blog post was originally posted on the [OPIG blog](https://www.blopig.com/blog/author/clare/).*



