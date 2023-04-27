# nvim-cadence

Syntax highlighting for the Cadence programming language. A high level programming lanaguage intended for smart contract development.

Modified from upstream with renaming to cdc since nvim recognize that

### Installation

Add it using your favorite plugin maanger. 

In LazyNvim you can do

```lua
return {
  --load in syntax/indent file
  "bjartek/nvim-cadence",
  config = function()
    -- startup the cadence shared lspconfig
    require("lspconfig").cadence.setup({
      init_options = {
        -- i normally set this to none as it will not warn me on access(all) errors
        accessCheckMode = "none",
      },
    })
  end,
}
```
