### Loding configuration
```
#reload without restart vim 
:source $MYVIMRC
```

### The \<leader\>?
``
:echo mapleader
``

### Folding
All folder command start with 'z'. To set the default to unfold, add `set foldlevelstart=99` to the .vimrc file.

[References](http://vimdoc.sourceforge.net/htmldoc/fold.html)

```
zR - Open all folds
zM - Close all folds
[z - Move to the start of the current open fold
]z - Move to the end of the current open fold
```
The PIV plugin made better folding for php file, to disable it, try:

```
let g:DisableAutoPHPFolding = 1 # in the .vimrc file
or
:EnableFastPHPFolds
:EnablePHPFolds
:DisablePHPFolds
```


### Mapping
[References](http://vim.wikia.com/wiki/Mapping_keys_in_Vim_-_Tutorial_(Part_1))

```
:map - Display all maps
:nmap - Display normal mode maps
:imap - Display insert mode maps
:vmap - Display visual and select mode maps
:smap - Display select mode maps
:xmap - Display visual mode maps
:cmap - Display command-line mode maps
:omap - Display operator pending mode maps

:map g - To display all the key maps that start with a key sequence

:nnoremap <F2> :ls<CR> - Create a new map
```



### Plugins
```
#Add new plugins
echo Bundle \'spf13/vim-colors\' >> ~/.vimrc.bundles.local
vim +BundleInstall! +BundleClean +q

echo UnBundle \'chriskempson/base16-vim\' >> ~/.vimrc.bundles.local
```


### Theming
```
# To check current color scheme
:color

# To list all installed color scheme
:colorscheme <space> <tab>

# To change a color scheme in .vimrc
:colorcheme base16-default

```
