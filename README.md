unicon
======
Uniform contrast light and dark colorscheme for Vim (GUI, true-color and 256-color terminals).

This colorscheme is heavily inspired by [solarized][], [gruvbox][] and [lucius][].

I like the idea, solarized based on: 8 monotonous and 8 accent colours, where accent colours are
chosen to present even contrast, high identifiability and readability. But it wasn't implemented
very well in solarized, in my opinion, mainly due to  very low contrast. So I have decided to
reimplement those ideas.

Differences from solarized:
* unicon has higher contrast;
* accent colours have actually the same contrast to background;
* different set of accent colours for light and dark variants of colorscheme;
* highlighting of syntax groups is different;
* There are not language- and plugin-specific syntax for now.

[solarized]: https://github.com/altercation/vim-colors-solarized
[gruvbox]: https://github.com/morhetz/gruvbox
[lucius]: https://github.com/jonathanfilip/vim-lucius

Installation
------------
1. Copy colors/unicon.vim to directory ~/.vim/colors/ or better use any of plugin manager:
   [vim-plug][], [NeoBundle][], [Vundle][] или [Pathogen][].

2. Append to ~/.vimrc:
   ```
   set background=light  " or dark
   colorscheme unicon
   ```
   You can toggle between light and dark variants using commands:
   ```
   :set background=light
   :set background-dark
   ```

[vim-plug]: https://github.com/junegunn/vim-plug
[NeoBundle]: https://github.com/Shougo/neobundle.vim
[Vundle]: https://github.com/gmarik/Vundle.vim
[Pathogen]: https://github.com/tpope/vim-pathogen

True colors in terminal
----------------------
If your terminal supports true colors add this line to ~/.vimrc before the line setting colorscheme.
```
set termguicolors
```

Screenshots
-----------
**Light**
![unicon_light](https://cloud.githubusercontent.com/assets/21138800/18610934/2a6c690a-7d3b-11e6-9385-78f13b550082.png)

**Dark**
![unicon_dark](https://cloud.githubusercontent.com/assets/21138800/18610936/36dba732-7d3b-11e6-97f8-c1a5d7a67a79.png)
