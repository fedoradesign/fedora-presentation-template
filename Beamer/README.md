# How to use Fedora Presentation Template

The Beamer template is defined by several **style files** (*.sty*), these are:

1. `beamertheme*.sty`

2. `beamerinnertheme*.sty`

3. `beameroutertheme*.sty`

4. `beamercolortheme*.sty`

In this repository, there are two directories called `fedora43` and `fedora169` that hold settings for different slide ratios, such as 4:3 and 16:9. They include the above files. You can see, that the file names also have an addition where the asterisk is put in the above list. For 4:3 ratio, the files use another `Fedora` addition, while for 16:9 they use `Fedora169`.

## Preparing your TeX installation

You have to install some packages to use the templates without getting errors:

1. Install the font package (`texlive-montserrat`) which will enable using the Fedora Montserrat Font.

2. Install the **ly1** package (`texlive-ly1`) to enable using the above font without error messages.

## Using the 4:3 ratio in your presentation.

### Using the style sheet

1. Copy the content of the `fedora43` directory to the place where you will be building your Beamer files.

Now, you can start working on your presentation in Beamer.

### Beamer preambule settings

There are some requirements, that you have to set in the preambule (Beamer header), so that Beamer would use the templates correctly. Check one possible working preambule:

---

\documentclass[12pt]{beamer} % Setting different fontsize will break the template.
\usepackage[utf8]{inputenc} % Support for UTF-8.
\usepackage[T1]{fontenc} % Support for T1 fonts.
\usepackage{lmodern} % Using modern fonts metrics
\usetheme{Fedora} % Loads the Fedora template for 4:3 slide ratio.
\usepackage{graphicx} % If you want graphics.
\usepackage{montserrat} % Fedora presentation font

---

## Using the 16:9 ratio in your presentation.

### Using the style sheet

1. Copy the content of the `fedora169` directory to the place where you will be building your Beamer files.

Now, you can start working on your presentation in Beamer.

### Beamer preambule settings

There are some requirements, that you have to set in the preambule (Beamer header), so that Beamer would use the templates correctly. The preambule is the same as in the previous section, with only two changes:

1. The `documentclass` command needs another parameter to define the new ratio. Insert the following into the square brackets - `aspectratio=169`.

2. The `usetheme` command will use a new theme, i.e. `Fedora169`. 

If you used the `Fedora` theme as in the previous example, the title page graphics would lose correct proportions. See the working preambule:

---

\documentclass[12pt, aspectratio=169]{beamer} % Setting different fontsize will break the template.
\usepackage[utf8]{inputenc} % Support for UTF-8.
\usepackage[T1]{fontenc} % Support for T1 fonts.
\usepackage{lmodern} % Using modern fonts metrics
\usetheme{Fedora} % Loads the Fedora template for 4:3 slide ratio.
\usepackage{graphicx} % If you want graphics.
\usepackage{montserrat} % Fedora presentation font

---

## Enjoy the template

Write your slides and present on Fedora related topics.
































