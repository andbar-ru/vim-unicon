unicon
======
Равноконтрастная светлая и тёмная цветовая схема для Vim.

Эта цветовая схема создана под влиянием [solarized][], [gruvbox][] и [lucius][].

Мне понравилась идея, лежащая в основе цветовой схемы solarized: 8 монотонных и 8 акцентных цветов, где акцентные цвета подобраны с целью достичь одинакового контраста, высокой различимости и удобочитаемости. Правда, реализация в solarized мне не показалась удобочитаемой, в основном, из-за слишком низкого контраста. Поэтому я решил создать свою цветовую схему, основанную на той же идее.

Отличия темы unicon от solarized:
* тема unicon более контрастная;
* акцентные цвета имеют действительно одинаковый контраст с фоном;
* разный набор акцентных цветов для светлой и тёмной цветовой схем;
* подсветка синтаксических групп другая;
* пока выкинуты специфические для языков и плагинов синтаксические группы, как и в lucius.

[solarized]: https://github.com/altercation/vim-colors-solarized
[gruvbox]: https://github.com/morhetz/gruvbox
[lucius]: https://github.com/jonathanfilip/vim-lucius

Установка
---------
1. Скопируйте colors/unicon.vim в каталог ~/.vim/colors/ или лучше воспользуйтесь каким-нибудь менеджером плагинов: [vim-plug][], [NeoBundle][], [Vundle][] или [Pathogen][].

2. Добавьте в ~/.vimrc:
   ```
   set background=light  " или dark
   colorscheme unicon
   ```
   Переключаться между светлым и тёмным вариантами можно командами:
   ```
   :set background=light
   :set background-dark
   ```

[vim-plug]: https://github.com/junegunn/vim-plug
[NeoBundle]: https://github.com/Shougo/neobundle.vim
[Vundle]: https://github.com/gmarik/Vundle.vim
[Pathogen]: https://github.com/tpope/vim-pathogen

256 цветов в терминале
----------------------
Unicon поддерживает 256-цветные терминалы, правда палитра для терминалов не обеспечивает ровный контраст, так как набор возможных цветов в терминале ограничен. Я не знаю, как из скрипта можно надёжно определить, поддерживает ли терминал 256 цветов. Команда `tput colors` по идее должна показывать количество возможных цветов в терминале, но её вывод зависит от переменной окружения $TERM и, даже если терминал поддерживает 256-цветную палитру, но значение переменной $TERM не подразумевает этого, `tput colors` вернет число меньше 256. В этом случае можно добавить к значению переменной $TERM '-256color', например, с помощью таких строк в ~/.bashrc:
```
if [[ "$TERM" =~ "term" ]]; then
    export TERM="xterm-256color"
fi
```
или прописав в ~/.vimrc:
```
set t_Co=256
```
Убедиться, что терминал поддерживает 256 цветов можно с помощью специальных тестовых скриптов, коих много в интернете, например [show-all-256-colors.py][] или [terminalcolors.py][].

[show-all-256-colors.py]: https://gist.github.com/mgedmin/2762225
[terminalcolors.py]: https://raw.githubusercontent.com/incitat/eran-dotfiles/master/bin/terminalcolors.py

Скриншоты
---------
**Light**
![unicon_light](https://cloud.githubusercontent.com/assets/21138800/18610934/2a6c690a-7d3b-11e6-9385-78f13b550082.png)

**Dark**
![unicon_dark](https://cloud.githubusercontent.com/assets/21138800/18610936/36dba732-7d3b-11e6-97f8-c1a5d7a67a79.png)
