I'm using [Maximum Awesome](https://github.com/square/maximum-awesome) but I've changed some of the default settings.
Search for "DIFF" in this README to find out what I've changed
Also, see the CheatSheet at the bottom for things I've learned about this setup (I don't work with the guys at Square, after all :)

# Maximum Awesome

Config files for vim and tmux, lovingly tended by a small subculture of
peace-loving hippies. Built for Mac OS X.

## What's in it?

* [MacVim](https://code.google.com/p/macvim/) (independent or for use in a terminal)
* [iTerm 2](http://www.iterm2.com/)
* [tmux](http://tmux.sourceforge.net/)
* Awesome syntax highlighting with the [Solarized color scheme](http://ethanschoonover.com/solarized)
* Want to know more? [Fly Vim, First Class](http://corner.squareup.com/2013/08/fly-vim-first-class.html)

### vim

* `,d` brings up [NERDTree](https://github.com/scrooloose/nerdtree), a sidebar buffer for navigating and manipulating files
* `,t` brings up [ctrlp.vim](https://github.com/kien/ctrlp.vim), a project file filter for easily opening specific files
* `,b` restricts ctrlp.vim to open buffers
* `,a` starts project search with [ack.vim](https://github.com/mileszs/ack.vim) using [ag](https://github.com/ggreer/the_silver_searcher) (like ack)
* `ds`/`cs` delete/change surrounding characters (e.g. `"Hey!"` + `ds"` = `Hey!`, `"Hey!"` + `cs"'` = `'Hey!'`) with [vim-surround](https://github.com/tpope/vim-surround)
* `\\\` toggles current line comment
* `\\` toggles visual selection comment lines
* `vii`/`vai` visually select *in* or *around* the cursor's indent
* `,[space]` strips trailing whitespace
* `<C-]>` jump to definition using ctags
* `,l` begins aligning lines on a string, usually used as `,l=` to align assignments
* `<C-hjkl>` move between windows, shorthand for `<C-w> hjkl`

### tmux

* `<C-j>` is the prefix  (DIFF C-a is square's default, but I use C-a to get to the beginning of the line in bash and to add numbers in vim)
* mouse scroll initiates tmux scroll
* `prefix v` makes a vertical split
* `prefix s` makes a horizontal split

## Install

    rake

## Customize
In your home directory, Maximum Awesome creates a `.vimrc.local` file where you can customize
Vim to your heart’s content. However, we’d love to incorporate your changes and improve Vim
for everyone, so feel free to fork Maximum Awesome and open some pull requests!

## Uninstall

    rake uninstall

Note that this won't remove everything, but your vim configuration should be reset to whatever it was before installing. Some uninstallation steps will be manual.

## Contribute

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

Any contributors to the master maximum-awesome repository must sign the
[Individual Contributor License Agreement (CLA)][cla].  It's a short form that
covers our bases and makes sure you're eligible to contribute.

[cla]: https://spreadsheets.google.com/spreadsheet/viewform?formkey=dDViT2xzUHAwRkI3X3k5Z0lQM091OGc6MQ&ndplr=1

When you have a change you'd like to see in the master repository, [send a pull
request](https://github.com/square/maximum-awesome/pulls). Before we merge your
request, we'll make sure you're in the list of people who have signed a CLA.

## Acknowledgements

Thanks to the vimsters at Square who put this together. Thanks to Tim Pope for
his awesome vim plugins.

## Austin's CheatSheet (DIFF)

* My `<tmux-leader>` is `<C-j>`
* get to tmux copy mode with <tmux-leader> [
  * tmux has a pipe-copy command that maximum-awesome uses to bind bind copied text into the Mac OSX clipboard (awesome!)
  * use vim commands in tmux copy mode to move and copy text
