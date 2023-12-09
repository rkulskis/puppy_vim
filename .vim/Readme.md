# Gruvbox 8 - Vim Color Scheme

![](https://raw.github.com/lifepillar/Resources/master/gruvbox8/gruvbox8-dark-and-light.png)

**Note: if you are using Neovim, checkout the `neovim` branch of this repo.**

This is a simplified and optimized<sup>*</sup> version of
[Gruvbox](https://github.com/morhetz/gruvbox) that I have developed
to address some issues I had with the official color scheme.

 These are the main differences compared to the official Gruvbox:

- by default, no plugin and filetype highlight groups to avoid messing up syntax
  highlighting after switching color schemes (they can be enabled through
  options);
- reduced number of options;
- all options are documented;
- slightly different (and, IMHO, better) 256-color palette;
- gracefully degrades to 16, 8 or even only 2 colors;
- support for transparent backgrounds in terminals;
- no shell scripts;
- up to date highlight group definitions (e.g., includes `ToolbarLine`
  and `ToolbarButton`);
- defines `g:terminal_ansi_colors`;
- generated by [Colortemplate](https://github.com/lifepillar/vim-colortemplate),
  i.e., easily hackable.

<sup>*</sup> Below is the result of a benchmark made using Vim 8.1.1550 and
iTerm 2 v3.2.9 on a MacBook Pro Early 2015 with macOS 10.14.5. Note that Gruvbox
8 is optimized for what are believed to be the most common use cases, i.e., GUI,
true-color terminals and 256-color terminals.

<p align="center">
<img width="500" src="https://raw.github.com/lifepillar/Resources/master/gruvbox8/load_time.png">
</p>


## True-color Variants

![](https://raw.github.com/lifepillar/Resources/master/gruvbox8/gruvbox8-variants.png)

## 256-color Variants

![](https://raw.github.com/lifepillar/Resources/master/gruvbox8/gruvbox8-256-variants.png)

## Less capable terminals

Earlier versions of Gruvbox 8 would complain when the terminal did not have
enough colors. This is no longer the case: Gruvbox 8 will gracefully degrade to
16, 8 or even 2 colors, as illustrated by the screenshot below:

![](https://raw.github.com/lifepillar/Resources/master/gruvbox8/gruvbox8-degrade.png)


## Hacking

Do you want to hack the theme? Install
[Colortemplate](https://github.com/lifepillar/vim-colortemplate), edit the
files in the `templates` folder, then rebuild the color schemes.
