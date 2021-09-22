# 🚪better-escape.nvim

This is a lua version of
[better_escape.vim](https://github.com/jdhao/better-escape.vim)

✨Features
--------
* Escape without getting delay when typing in insert mode
* Customizable mapping and timeout
* Use multiple mappings

📦Installation
------------
Use your favourite package manager and call setup function.
```vim
" Vimscript with vim-plug
Plug 'max397574/better-escape.nvim'
lua require("better_escape").setup()
```

```lua
-- lua with packer.nvim
use {
  "max397574/better-escape.nvim",
  config = function()
    require("better_escape").setup()
  end,
}
```

✅Usage
-----
Just use your mappings.

⚙️Customization
-------------
Call the setup function before calling the init function.

```lua
-- lua, default settings
require("better_escape").setup {
    mapping = {"jk", "jj"}, -- a table with mappings to use
    timeout = 200, -- the time in which the keys must be hit in ms
}
```

```vim
-- Vimscript, default settings
lua << EOF
require("better_escape").setup {
    mapping = {"jk","jj"}, -- a table with mappings to use
    timeout = 200, -- the time in which the keys must be hit in ms
}
EOF
```

🚫Limitations/Issues
--------------------
* Doesn't work if one of the keys of the mapping is mapped to something else.

💡Future Plans/Ideas
------------------
* Fix the limitations.

👀Demo
------

When using `inoremap jk <ESC>`:

https://user-images.githubusercontent.com/81827001/134317521-0c446238-c24c-4303-9539-e5eb6236d221.mp4

When using this plugin:

https://user-images.githubusercontent.com/81827001/134317540-95a66237-dd77-49a9-8f11-8b037458354c.mp4

