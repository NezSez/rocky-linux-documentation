---
title: GNU Info Cheatsheet
author: David Hensley (NezSez)
contributors:
date: Sat 2023-05-06 00:42:04 UTC
tested with: Rocky Linux 8.7
tags:
  - info
  - pinfo
  - cheatsheet
---

# GNU Info Cheatsheet
Quick reference sheet for using GNU's `info`[^1] program. These key bindings also work in `pinfo`.

The default keybindings for navigation used are the same as the well known emacs bindings, which are also used for the bash shell by default.
You can start it with [`info --vi-keys <topic>`](https://www.gnu.org/software/texinfo/manual/info-stnd/html_node/Invoking-Info.html#g_t_002d_002dvi_002dkeys)
option if you prefer the VI key bindings.

[//]: TODO: Add the vi keybindings


!!! note "Accessibility Option"

    It also supports screen reading for the visualy impaired by starting it as [`info --speech-friendly <topic>`](https://www.gnu.org/software/texinfo/manual/info-stnd/html_node/Invoking-Info.html#index-_002d_002dspeech_002dfriendly-_0028_002db_0029-command-line-option)but this only the in MS-DOS/MS-Windows install according to the GNU docs; that seems ironic :)


- Launch by entering `info <topic>` at the command line.
- You can also use `pinfo <topic>` to view info and man pages; it supports colors and hyperlinks
- You can read info on `info` by entering `info info` at the command prompt.
- Entering `h` within `info` itself will open an `info` "window" with help.
- Remember that `info` ***IS*** case-sensitive: `h` and `H` are ***NOT*** the same command.
- If you get confused you can always enter `q` to quit and start over.

=== "Default Bindings (Emacs)"

The <kbd>Meta</kbd> usually = <kbd>ALT</kbd> key; <kbd>ESC</kbd> key, which is the same as <kbd>ctrl</kbd>+<kbd>[</kbd> works. So <kbd>ctrl</kbd>+<kbd>[</kbd>  <kbd>v</kbd> is an equivalent.

|    Key binding                           |    Action                                              |
|:-----------------------------------------|:-------------------------------------------------------|
|<kbd>q</kbd>                              | Quit, exit back to shell prompt                        |
|<kbd>Ctrl</kbd>+<kbd>h</kbd>              | Help (`l` ("el" *not* "one") exits help and returns to the previous location |
|<kbd>H</kbd>                              | Split screen and show basic key bindings               |
|<kbd>h</kbd>                              | Start the builtin tutorial                             |
|                                          |                                                        |
|<kbd>Ctrl</kbd>+<kbd>n</kbd>, <kbd>Down-arrow</kbd>  | Move cursor down to next line               |
|<kbd>Ctrl</kbd>+<kbd>p</kbd>, <kbd>Up-arrow</kbd>    | Move cursor up to previous line             |
|<kbd>Ctrl</kbd>+<kbd>b</kbd>, <kbd>Left-arrow</kbd>  | Move cursor one character to left           |
|<kbd>Ctrl</kbd>+<kbd>f</kbd>, <kbd>Right-arrow</kbd> | Move cursor one character to right          |
|<kbd>Ctrl</kbd>+<kbd>a</kbd>                         | Move cursor to beginning of current line    |
|<kbd>Ctrl</kbd>+<kbd>e</kbd>                         | Move cursor to end of current line          |
|                                                     |                                             |
|<kbd>Spacebar</kbd>                                  | Scroll forward (down) one screen; advance to next screen if at the bottom of current one |
|<kbd>Ctrl</kbd>+<kbd>v</kbd>, <kbd>Page-Down</kbd>   | Scroll forward (down) one screen            |
|<kbd>Meta-V</kbd>, <kbd>Page-Up</kbd>		          | Scroll backward (up) one screen.            |           |
|                                          |                                                        |
|<kbd>b</kbd>, <kbd>HOME</kbd>             | Move cursor to beginning of current node               |
|<kbd>e</kbd>, <kbd>END</kbd>			   | Move cursor to end of current node                     |
|<kbd>l</kbd>                              | Move to last/previous node in the current window       |
|<kbd>n</kbd>                              | Move to next node on this level                        |
|<kbd>]</kbd>                              | Move to next node in the document                      |
|<kbd>p</kbd>                              | Move to previous node on this level                    |
|<kbd>[</kbd>                              | Move to previous node in the document                  |
|<kbd>u</kbd>                              | Move up a node one level                               |
|<kbd>t</kbd>                              | Move to top node of document                           |
|<kbd>d</kbd>                              | Move to main  `directory` node                         |
|                                          |                                                        |
|<kbd>1...9</kbd>                          | Pick corresponding item in current node's menu         |
|<kbd>0</kbd>                              | Pick the last item in menu                             |
|                                          |                                                        |
|<kbd>f</kbd>                              | Follow a cross-reference by name                       |
|<kbd>g</kbd>                              | Move to a node specified by name                       |
|                                          |                                                        |
|<kbd>s</kbd>                              | Case-insensitive search for string                     |
|<kbd>S</kbd>                              | Case-sensitive search for string                       |
|<kbd>Ctrl</kbd>+<kbd>x</kbd> <kbd>n</kbd> | Repeat last search                                     |
|<kbd>Ctrl</kbd>+<kbd>x</kbd> <kbd>N</kbd> | Repeat last search in opposite direction               |
|<kbd>Ctrl</kbd>+<kbd>g</kbd>              | Cancel iterative operations (i.e. incremental search)  |
|                                          |                                                        |
|<kbd>TAB</kbd>                            | Skip to next hyperlink                                 |
|<kbd>RET</kbd>, <kbd>ENTER</kbd>          | Follow hypertext link under cursor                     |

=== "VI Bindings"

|    Key binding                           |    Action                                              |
|:-----------------------------------------|:-------------------------------------------------------|
|<kbd>q</kbd>                              | Quit, exit back to shell prompt                        |


[^1]: [Info: An Introduction](https://www.gnu.org/software/emacs/manual/html_mono/info.html)
