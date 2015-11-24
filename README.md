# vim

```bash
git clone git@github.com:okwrtdsh/vim.git ~/.vim
cp ~/.vim/vimrc ~/.vimrc
cp ~/.vim/vimrc.local ~/.vimrc.local
```

## ncurses-termのインストール
以下のエラーが出る場合はncurses-termをインストールして下さい．
```
E558: Terminal entry not found in terminfo
'gnome-256color' not known. Available builtin terminals are:
builtin_riscos
builtin_amiga
builtin_beos-ansi
builtin_ansi
builtin_pcansi
builtin_win32
builtin_vt320
builtin_vt52
builtin_xterm
builtin_iris-ansi
builtin_debug
builtin_dumb
defaulting to 'ansi'
```
ncurses-termのインストール

```bash
sudo apt-get install ncurses-term
```
