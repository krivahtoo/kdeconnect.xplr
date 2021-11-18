> Warning: Work in progress

Share files via kdeconnect in xplr


Requirements
------------

- [kdeconnect](https://kdeconnect.kde.org/)


Installation
------------

### Install manually

- Add the following line in `~/.config/xplr/init.lua`

  ```lua
  package.path = os.getenv("HOME") .. '/.config/xplr/plugins/?/src/init.lua'
  ```

- Clone the plugin

  ```bash
  mkdir -p ~/.config/xplr/plugins

  git clone https://github.com/krivahtoo/kdeconnect.xplr ~/.config/xplr/plugins/kdeconnect
  ```

- Require the module in `~/.config/xplr/init.lua`

  ```lua
  require("kdeconnect").setup()
  
  -- Or
  
  require("kdeconnect").setup{
    mode = "selection_ops",
    key = "K",
  }

  -- Select files and type `:sK` to share
  ```

