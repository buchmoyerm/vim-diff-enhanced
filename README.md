#EnhancedDiff plugin
> A Vim plugin for creating better diffs (sometimes)

This plugin allows you to make use of the Patience diff algorithm for generating diffs to use with Vim. This needs the git command line tool available.

You can also customize your setup to use any other tool to generated diffs (e.g. mercurial) Read the help on how to configure the plugin accordingly.

Here are some screenshots that visualize how the patience/histogram algorithm work.

This is the default diff generated by Vim:
![Default diff](default_diff.png)

Now change that to using the "histogram" algorithm by running `:EnhancedDiff histogram`
If Vim is in diff mode, the diff will be updated to this:

![histogram diff](histogram_diff.png)

Note, that the Patience algorithm might not always provide better diffs. But using this plugin you can at least easily switch between different diffs.

###Installation
Use the plugin manager of your choice:

* [Pathogen][pathogen]
  * `git clone https://github.com/chrisbra/vim-diff-enhanced.git ~/.vim/bundle/vim-enhanced-diff`
* [NeoBundle][neobundle]
  * `NeoBundle 'chrisbra/vim-diff-enhanced'`
* [Vundle][vundle]
  * `Plugin 'chrisbra/vim-diff-enhanced'`
* [Vim-Plug][vim-plug]
  * `Plug 'chrisbra/vim-diff-enhanced'`

Alternatively download the [stable][] version of the plugin, edit it with Vim (`vim EnhancedDiff-XXX.vmb`) and simply source it (`:so %`). Restart and take a look at the help (`:h EnhancedDiff.txt`)

[stable]: http://www.vim.org/scripts/script.php?script_id=5121

###Usage
Once installed, take a look at the help at `:h EnhancedDiff`

Here is a short overview of the functionality provided by the plugin:
####Ex commands:
`:PatienceDiff` - Use the Patience Diff algorithm for the next diff mode

`:EnhancedDiff <algorithm>`  - Use &lt;algorithm> to generate the diff.
Use any of
* myers		Default Diff algorithm used
* default	Alias for myers algorithm
* histogram     Fast version of patience algorithm
* minimal	Default diff algorithm, trying harder to minimize the diff
* patience	Patience diff algorithm.

Note: Those 2 commands use the git command line tool internally to generate the
diffs. Make sure you have at least git version 1.8.2 installed.

`:EnhancedDiffDisable`    - Disable plugin (and use default Vim diff capabilities).

###License & Copyright

© 2015 by Christian Brabandt. The Vim License applies. See `:h license`

__NO WARRANTY, EXPRESS OR IMPLIED.  USE AT-YOUR-OWN-RISK__

[pathogen]: https://github.com/tpope/vim-pathogen
[neobundle]: https://github.com/Shougo/neobundle.vim
[vundle]: https://github.com/gmarik/vundle
[vim-plug]: https://github.com/junegunn/vim-plug
