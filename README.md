old GIF using zoxide:
[![xplr-zoxide.gif](https://s6.gifyu.com/images/xplr-zoxide.gif)](https://gifyu.com/image/AclQ)

## Requirements

- ~~[zoxide] (https://github.com/ajeetdsouza/zoxide)~~
- [z.lua](https://github.com/skywind3000/z.lua)

## Installation

### Install manually

- Add the following line in `~/.config/xplr/init.lua`

  ```lua
  local home = os.getenv("HOME")
  package.path = home
  .. "/.config/xplr/plugins/?/init.lua;"
  .. home
  .. "/.config/xplr/plugins/?.lua;"
  .. package.path
  ```

- Clone the plugin

  ```bash
  mkdir -p ~/.config/xplr/plugins

  git clone https://github.com/sayanarijit/zoxide.xplr ~/.config/xplr/plugins/zoxide
  ```

- Require the module in `~/.config/xplr/init.lua`

  ```lua
  require("zoxide").setup()

  -- Or

  require("zlua").setup{
    bin = "zoxide",
    mode = "default",
    key = "Z",
  }

  -- Type `Z` to spawn z.lua prompt.
  ```
