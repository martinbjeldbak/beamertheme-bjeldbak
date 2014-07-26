# beamertheme-bjeldbak
A simple beamer theme. I'm aiming for a minimalistic look.

See my blog post accompanying this theme [here](http://martinbmadsen.dk/a-minimalistic-customizable-beamer-theme/) for more information.

This theme started off as me modifying Cameron Bracken's theme published in his blog post [here](http://cameron.bracken.bz/beamer-template).

## Installing

Add this repository to your presentation like so

```bash
$ git clone git@github.com:fapper/beamertheme-bjeldbak.git
```
then, in your root or preamble set ``beamerthemebjeldbak.sty`` as the presentation style with ``\usetheme{bjeldbak}``.


## Screenshots

![Screenshot 1](/beamerthemebjeldbak1.png)

![Screenshot 2](/beamerthemebjeldbak2.png)

![Screenshot 3](/beamerthemebjeldbak3.png)

![Screenshot 4](/beamerthemebjeldbak4.png)

## Minimum working example
Having cloned as above, this will compile a mini presentation.

```tex
\documentclass{beamer}

\usetheme{beamertheme-bjeldbak/beamerthemebjeldbak}

\title{Testing}
\author{Martin Madsen}

\begin{document}
  {%
    \setbeamertemplate{headline}{}
    \frame{\titlepage}
  }

  \begin{frame}
    It's working!
  \end{frame}
\end{document}
```

## Customizing
Here are a couple of things you can change up. I'm sure there are more!

### Changing theme font
This is done on line 9 with ``\RequirePackage{tgpagella}``, and can be set to any packaged font in the TUG [font catalogue](http://www.tug.dk/FontCatalogue/).

### Changing current slide typography
Line 20 accomplishes this. You can replace ``/`` with ``-``, ``of``, or any other separation character(s) you may have in mind.

### Changing top/bottom bar colors
If you want to change the color of the teal bars above and below  each slide, simply change the ``\definecolor{barcolor}{HTML}{77C4D3}`` command on line 43 with any other hex value.

### Showing clickable bottom bar
By default, the clickable navbar at the bottom (enabled by in all standard themes) is hidden, as I have never needed to use it. If you want re-enable it again paste the following after the ``\usetheme{bjeldbak}`` in your preamble:

```tex
\setbeamertemplate{navigation symbols}[horizontal]
```

Alternatively, remove/comment out line 40 in the theme file.
