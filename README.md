# sourcenav.lua
A Source Engine navigation mesh parser written in Lua, intended for CS:GO (but will probably work for other source engine games too)

Based on [sourcenav](https://github.com/thiagofelix/sourcenav) by [thiagofelix](https://github.com/thiagofelix) and [bot.nav](https://gitlab.com/Cre3per/bot.nav) by Cre3per

## Dependencies:

- https://github.com/iryont/lua-struct/blob/master/struct.lua (but will probably work with the C module http://www.inf.puc-rio.br/~roberto/struct/ too)

## Usage:

```Lua
local sourcenav = require "sourcenav"

local f = io.open("de_mirage.nav", "rb")
local content = f:read("*all")
f:close()

local nav_mesh = sourcenav.parse(content)

print("Parsed " .. #nav_mesh.places .. " places, " .. #nav_mesh.areas .. " areas, " .. #nav_mesh.ladders .. " ladders.")
```
