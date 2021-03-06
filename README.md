# Main
1. Скрипт клонирует репозиторий в **/tmp/dotfiles**
2. Сперва запускаем скрипт из под **root** для установки обновлений/пакетов из репозитория/установки бинарников/completions 
3. После чего можем проверить/удалить/заново установить dotfiles для **root**-а
4. Для обычного пользователя меню урезано - дотсупны только пункты меню, относящиеся к dotfiles
5. Сами dotfiles качаются из репозитория : https://github.com/rubtsove/dotfiles

#  Возможности 
1. Обновление через **apt**/**yum** ( apt делает ещё и autoremove && autoclean )
2. Устанавливает пакеты из repo : **vim,wget,curl,htop,grc,lnav,tree,ccze,needrestart,git,unzip**
3. Установка **bat** - аналог cat
4. Установка **cht.sh** и его bash completions - анлог tldr
5. Установка **grc/grccat** для расцветки терминала
6. Установка **exa** и его bash completions- аналог ls
7. Установка **duf** - аналог df -Th
8. Установка **ds** - аналог du -sh, написанный на rust
9. Установка **gdu** - аналог ncdu, написанный на go
10. Установка **duskuss** - аналог du -sh
11. Установка **dir-stats** - аналог du -ahc|sort -hr |head, написанный на rust
12. Установка **sss** - аналог netstat -ntulp
13. Установка **procs** и его bash completions- аналог ps -aux
14. Установка **btm** и его bash completions- аналог htop
15. Установка **fddind** - и его bash completions- аналог find
16. Установка **ripgrep** - и его bash completions- аналог grep
17. Проверка наличия папок : .config/, **.vim**/, dotfiles/
18. Удаление страрых dotfiles 
19. Копирование новых dotfiles с этого repo
20. Установка **FZF** (работют сочетания клавиш Ctrl+r, CTRL+t, Alt+c)
# .bashrc
1. Кастомный **PS1**
2. Default Editor: **VIM**
3. FZF настроен и для поиска скрытых файлов тоже
4. FZF keybindings: устанавливается для каждого пользователя
5. Функция **fuzzy-sys** - применяем FZF для проверки сервисов systemd
# .bash_aliases
1. Расцветка базируется на бинарнике **grc** - для него подготовлены основные alias-ы
2. **fzf-pkg** - позволяет через fzf находить и устанавливать пакеты
# .vimrc
1. Автоматом загружается менеджер плагинов **vim-plug** - при первом запуске надо нажать Enter - что бы плагины автоматом скачались
2. В конфиге прописаны следующие плагины : fzf, fzf.vim, NERDTree, syntastic(проверка синтаксиса), vim-airline(тема base16)
3. Сочетание клавиш **Ctlr + p** : вызывает FZF
4. Сочетание клавиш **Ctlr + n** : вызывает/скрывает **NERDTree**
5. **NERDTree** настроен для показа скрытых файлов
6. Для Centos7 при установке плагинов используем конфиг : Plug 'junegunn/fzf', { 'dir': '~/.fzf', 'do': './install --all' }