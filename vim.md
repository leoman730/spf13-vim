### Loding configuration
```
#reload without restart vim 
:source $MYVIMRC

#reload current file content
:e! 
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
zo - Open one fold under the cursor, zO (for recursive)
zc - Close one fold under the cursor, zC (for recursive)
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

### Match braces

Use `%` key to match ({{}])  
To select context inside the match braces: `v%`

### Commenting
[Reference](http://spf13.com/post/vim-plugins-nerd-commenter)

```
# Toggle comment
<leader>c<space>

# Sexier comment
<leader>cs<space>
```

### Search
Use `*` to search the term under cursor  
To remove current search highlight: `:noh`

### Undo / Redo
u: Undo last change (can be repeated to undo preceding commands)
Ctrl-R: Redo changes which were undone (undo the undos)


### Formating
To autoformat (indentation) on a file, use:

```
:set shiftwidth=2|4
gg=G
```


### Trigger on write

[Reference](http://vim.wikia.com/wiki/Remove_unwanted_spaces#Automatically_removing_all_trailing_whitespace)

```
#Automatically remove trailin whitespace on file write
autocmd FileType c,cpp,java,php,html,js,css,scss
autocmd BufWritePre * :%s/\s\+$//e
```


### Copy & Paste
To copy to clicpboard, select the desire lines in visual mode, then `!pbcopy` 
Copy line by range  
```
:12,15y -- copy line from 12 to 15
```



### Variables
```
:set            - shows vars different from defaults
:set all        - shows all values
:set foo?       - shows the value of foo
:set foo+=opt   - add opt to the value w/o changing others
:set foo-=opt   - remove opt from value
:set foo&       - reset foo to default value
:setlocal foo   - only the current buffer
```


### Tab vs. Space
[Reference](http://stackoverflow.com/questions/1562336/tab-vs-space-preferences-in-vim)

```
tabstop - the width of tab character
shiftwidth - specifies how many columns to increment/decrement when using the << and >> commands
softtabstop - the amount of whitespace to be inserted when you press the Tab key in insert mode
expandtab (on) -  the tab key inserts softtabstop number of space characters
expandtab (off) - the Tab key inserts a the smallest possible number of tab+space characters that matches softtabstop
```


### ZenCoding - The Emmet plugin
[Tutorial](https://raw.githubusercontent.com/mattn/emmet-vim/master/TUTORIAL)

```
Activate expandsion: '<c-y>,'
Wrap with an abbreviation: '<c-y>,' in visual mode
Merge line: '<c-y>m'
Toggle comment: '<c-y>/'
Make an anchor from a URL: Select url, then '<c-y>a'
```

### Status
Find out the current opened file name: `:f`



## References:

[Vim Tips & Tricks](https://www.cs.swarthmore.edu/help/vim/home.html)  
[Vim Cast] (http://vimcasts.org/)
