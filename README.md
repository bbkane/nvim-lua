# TODO:

Get gx working with links... How do you source a vim file in Lua?

lsp-go

lsp-bash?

https://github.com/mjlbach/defaults.nvim

https://github.com/mattn/efm-langserver - pausing till I have lua working :)

https://github.com/rockerBOO/awesome-neovim

treesitter

# DONE

efm-pyright
lsp-lua
plugins!
packer - working :)
nvim-compe - working :)
lsp-pyright - got it - will probably want to check for venvs, but whatever
https://github.com/lewis6991/gitsigns.nvim - done enough - could change colors to look better, but colorscheme might do that anyway

# Bugs found

:PackerStatus Broken

```
Error executing vim.schedule lua callback: vim/shared.lua:396: t: expected
table, got nil
stack traceback:
        vim/shared.lua:396: in function 'tbl_count'
        ...ite/pack/packer/start/packer.nvim/lua/packer/display.lua:273: in
 function 'cb'
        vim.lua:253: in function <vim.lua:253>
```

---

```lua
    use {
      'lewis6991/gitsigns.nvim', requires = { 'nvim-lua/plenary.nvim' },
    }
```

a `config =` block in here doesn't appear to work...

# Needed to install :)

## Building NeoVim

I followed https://github.com/neovim/neovim/wiki/Installing-Neovim#homebrew-on-macos-or-linux

Think I had to do:

```
brew install --HEAD luajit
brew install --HEAD neovim
```

But I also have the following, so who knows...

```
$ brew list | grep lua
lua
luajit
luajit-openresty
luarocks
```

## Others

volta install pyright
volta install bash-language-server
brew install efm-langserver

## sunneko lua

https://www.chrisatmachine.com/Neovim/28-neovim-lua-development/
https://github.com/sumneko/lua-language-server/wiki/Build-and-Run-(Standalone)

that worked relatively well