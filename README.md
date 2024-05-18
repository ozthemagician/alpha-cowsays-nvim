# alpha-cowsays-nvim

This plugin is a simple addon for [alpha-nvim](https://github.com/goolord/alpha-nvim) Startify theme. It adds a random cowsay quote to the startify header.

## Quick Start

Lazy Config:

```lua
return {
  "goolord/alpha-nvim",
  event = "VimEnter",
  dependencies = {
    "ozthemagician/alpha-cowsays-nvim",
  },
  config = function()
    local alpha = require("alpha")
    local startify = require("alpha.themes.startify")
    local cow = require("alpha-cowsays-nvim")

    startify.section.header.val = cow.cowsays()

    alpha.setup(startify.config)
  end,
}
```
