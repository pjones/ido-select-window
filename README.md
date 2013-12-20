# ido-select-window

A tiny package to change the window focus in Emacs using `ido` and the
name of each window's buffer.

Yes, there are plenty of packages for switching the window focus.  As
far as I can tell they're all based on the position of a window
(e.g. focus left, focus right, etc.)  The [switch-window] [] package
makes this a bit more visual but covers up the contents of the window
and doesn't play nicely with my IRC buffers.

I thought it would be an interesting experiment to use `ido` and the
mini-buffer for switching windows based on buffer names.  That's what
this package does.

[switch-window]: https://github.com/dimitri/switch-window

# Usage

If you're using the Emacs packaging system then this package should
automatically load.  If not, require it.

Then set a key binding.  I like the idea of replacing `C-x o`:

    (global-set-key (kbd "C-x o") 'ido-select-window)
