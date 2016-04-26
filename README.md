# vim

```bash
git clone git@github.com:okwrtdsh/vim.git ~/.vim
ln -s ~/.vim/vimrc ~/.vimrc
ln -s ~/.vim/vimrc.local ~/.vimrc.local
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

## vim-bootstrap-updaterの修正
以下のエラーが出る場合はvim-bootstrap-updaterを修正して下さい．
```shell
$ vim
Error detected while processing /home/okwrtdsh/.vim/bundle/vim-bootstrap-updater/plugin/vim_bootstrap_updater.vim:
line    4:
E319: Sorry, the command is not available in this version: python import sys
line    5:
E319: Sorry, the command is not available in this version: python import vim
line    6:
E319: Sorry, the command is not available in this version: python sys.path.append(vim.eval('expand("<sfile>:h")'))
```

```diff
$ git diff
diff --git a/plugin/vim_bootstrap_updater.vim b/plugin/vim_bootstrap_updater.vim
index 19f2870..ba8c189 100644
--- a/plugin/vim_bootstrap_updater.vim
+++ b/plugin/vim_bootstrap_updater.vim
@@ -1,10 +1,10 @@
 " --------------------------------
 " Add our plugin to the path
 " --------------------------------
-python import sys
-python import os
-python import vim
-python sys.path.append(vim.eval('expand("<sfile>:h")'))
+python3 import sys
+python3 import os
+python3 import vim
+python3 sys.path.append(vim.eval('expand("<sfile>:h")'))
 
 " --------------------------------
 "  Function(s)
 ```
