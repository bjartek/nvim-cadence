# nvim-cadence

Syntax highlighting for the Cadence programming language. A high level programming lanaguage intended for smart contract development.

Modified from upstream with renaming to cdc since nvim recognize that

### Installation

Add it using your favorite plugin manager. 

In LazyNvim you can do

```lua
return {
  "bjartek/nvim-cadence",
  config = function()
    -- i really like format on save and this does the trick
    vim.api.nvim_create_autocmd("BufWritePre", {
      pattern = { "*.cdc" },
      command = ":normal gg=G''",
    })
    -- startup the cadence shared lspconfig
    require("lspconfig").cadence.setup({
      init_options = {
        -- i like to set this since we use access(account) quite a lot and this does not throw an error when that happends
        accessCheckMode = "none",
      },
    })
  end,
}
```
