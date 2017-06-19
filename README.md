# Syntastic Swift

Syntastic Swift works with the [syntastic](https://github.com/vim-syntastic/syntastic) Vim plugin to compile a single Swift file and display any warnings or errors inside Vim.

## Installation

Install syntastic using [Pathogen](https://github.com/tpope/vim-pathogen):
```
cd ~/.vim/bundle && \
git clone --depth=1 https://github.com/vim-syntastic/syntastic.git
```

Then install this syntax checker:
```
cd ~/.vim/bundle && \
git clone --depth=1 https://github.com/TheCodedSelf/syntastic-swift
```

## Usage
Open a Swift file in Vim and save it. The swift syntax checker will run and provide you with any errors or warnings.

## Troubleshooting
Run `:SyntasticInfo`. You should see the following included in the output:
```
Available checkers: swift
Currently enabled checkers: swift
```

If you don't, then add the following to your .vimrc:
```
let g:syntastic_aggregate_errors = 1
let g:syntastic_swift_checkers = ['swift'] 
" If you have other Swift checkers, add them to the above array
```

Reopen a Swift file and take a look at `:SyntasticInfo`. If you're still experiencing problems, feel free to make an issue on this repository.
