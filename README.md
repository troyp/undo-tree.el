# undo-tree.el
A fork of http://www.dr-qubit.org/git/undo-tree.git

This fork fixes an issue where long filenames may cause
`undo-tree-make-history-save-file-name` to generate a name in excess of 255
bytes, producing an error when undo-tree tries to save its history. I found
this error particularly annoying, since I have `undo-tree-save-history` run
under `kill-buffer-hook` in a (not-very-effective)
[attempt](https://github.com/syl20bnr/spacemacs/issues/774#issuecomment-194527210)
at preventing undo-tree history corruption.

(I'd love to fix the history corruption, but I have a feeling that wouldn't be
so easy...)
