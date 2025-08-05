# Neovim Cheat Sheet

A quick reference to installed plugins and keybindings, organized by plugin.

---

## Core Keymaps

| Key                 | Mode | Action                                              |
|---------------------|------|-----------------------------------------------------|
| `<C-c>`             | n/i  | Escape in Insert (maps to `<Esc>`)                  |
| `J` (n)             | v    | Move lines down in Visual                            |
| `K` (n)             | v    | Move lines up in Visual                              |
| `<C-d>`             | n    | Scroll down and center cursor                        |
| `<C-u>`             | n    | Scroll up and center cursor                          |
| `<leader>s`         | n    | Replace word under cursor globally                   |
| `<leader>x`         | n    | Toggle file executable (`chmod +x %`)                |
| `<leader>fp`        | n    | Copy current file path to clipboard                  |
| `<leader>lx`        | n    | Toggle LSP diagnostics display                       |
| Tab management      | n    | `to`, `tx`, `tn`, `tp`, `tf` for new/close/next/tab  |
| Split management    | n    | `sv`, `sh`, `se`, `sx` for splits                    |

---

## General Vim Commands

| Command            | Mode | Description                                |
|--------------------|------|--------------------------------------------|
| gcc                | n    | Toggle comment on current line             |
| gc (visual)        | v    | Toggle comment on selected lines           |
| /pattern           | n    | Search forward for pattern                 |
| ?pattern           | n    | Search backward for pattern                |
| n / N              | n    | Next / previous search match               |
| dd                 | n    | Delete current line                        |
| yy                 | n    | Yank (copy) current line                   |
| p / P              | n    | Paste after / before cursor                |
| >> / <<            | n    | Indent / outdent current line              |
| :split             | n    | Open horizontal split                      |
| :vsplit            | n    | Open vertical split                        |
| :tabnew            | n    | Open new tab                               |
| :tabnext / tabprev | n    | Go to next / previous tab                  |
| :e $MYVIMRC        | n    | Edit init.lua (Neovim config)              |
| :so %              | n    | Source current file                        |

---

## windwp/nvim-autopairs

Automatically insert matching pairs.

## rmagatti/auto-sessionf

| Key                 | Mode | Action                                            |
|---------------------|------|---------------------------------------------------|
| `<leader>wr`        | n    | Restore last session for cwd                      |
| `<leader>ws`        | n    | Save session for current directory                |

| Command             | Description                                       |
|---------------------|---------------------------------------------------|
| `:SessionRestore`   | Restore last saved session                       |
| `:SessionSave`      | Save current session                              |

---

## Colorscheme Plugins

### rose-pine, gruvbox, kanagawa, solarized-osaka, tokyonight

Switch via `:colorscheme <name>` in command mode as needed.

| Command             | Description                                       |
|---------------------|---------------------------------------------------|
| `:colorscheme rose-pine`       | Apply Rose Pine theme              |
| `:colorscheme gruvbox`         | Apply Gruvbox theme                |
| `:colorscheme kanagawa`        | Apply Kanagawa theme               |
| `:colorscheme solarized-osaka` | Apply Solarized Osaka theme        |
| `:colorscheme tokyonight`      | Apply Tokyo Night theme            |

---

## stevearc/conform.nvim

| Key                 | Mode | Action                                                |
|---------------------|------|-------------------------------------------------------|
| `<leader>mp`        | n/v  | Format file or selection (via Conform)                |

| Language | Formatter    | Filetype         |
|----------|--------------|------------------|
| Ruby     | rubocop      | `.rb`, `ruby`    |
| Rust     | rustfmt      | `.rs`, `rust`    |

| Command       | Description                                    |
|---------------|------------------------------------------------|
| `:ConformInfo`| Show Conform plugin and formatter settings     |

---

## Git Plugins

### tpope/vim-fugitive

| Key                 | Mode | Action                                               |
|---------------------|------|------------------------------------------------------|
| `<leader>gg`        | n    | `:Git`                                               |
| `<leader>P`         | n    | `:Git push`                                          |
| `<leader>p`         | n    | `:Git pull --rebase`                                 |
| `<leader>t`         | n    | `:Git push -u origin `                               |

### lewis6991/gitsigns.nvim

| Key                 | Mode | Action                                               |
|---------------------|------|------------------------------------------------------|
| `]h` / `[h`         | n    | Next / Prev hunk                                     |
| `<leader>gs` / `gr` | n/v  | Stage / Reset hunk                                   |
| `<leader>gS`        | n    | Stage buffer                                         |
| `<leader>gR`        | n    | Reset buffer                                         |
| `<leader>gp`        | n    | Preview hunk                                         |
| `<leader>gbl`       | n    | Blame line (full)                                    |
| `<leader>gd` / `gD` | n    | Diff this / Diff ~                                    |
| `ih` (o/x)          | o/x  | Select hunk textobject                                |

### folke/todo-comments.nvim (global & via Snacks)

| Key           | Mode | Action                             |
|---------------|------|------------------------------------|
| `]t` / `[t`   | n    | Next / Previous TODO remark        |
| `<leader>pt`  | n    | List all TODOs (Snacks picker)     |
| `<leader>pT`  | n    | List TODO/FIX/FIXME (Snacks picker)|

---

## kdheepak/lazygit.nvim (disabled)

| Key           | Mode | Action             |
|---------------|------|--------------------|
| `<leader>lg`  | n    | `:LazyGit`         |

| Commands                     | Description                          |
|------------------------------|--------------------------------------|
| `:LazyGitConfig`            | Open LazyGit config                  |
| `:LazyGitCurrentFile`       | Open LazyGit for current file        |
| `:LazyGitFilter`            | Open filter view in LazyGit          |
| `:LazyGitFilterCurrentFile` | Filter view for current file         |

---

## ThePrimeagen/git-worktree.nvim

| Key           | Mode | Action                       |
|---------------|------|------------------------------|
| `<leader>wl`  | n    | List worktrees (Telescope)   |
| `<leader>wc`  | n    | Create new git worktree      |

| Commands                     | Description                          |
|------------------------------|--------------------------------------|
| `:Telescope git_worktree`    | List and switch Git worktrees        |
| `:Telescope git_worktree create_git_worktree` | Create a new worktree  |

---

## thePrimeagen/harpoon

| Key           | Mode | Action                         |
|---------------|------|--------------------------------|
| `<leader>a`   | n    | Add file to Harpoon list       |
| `<C-e>`       | n    | Toggle Harpoon quick menu      |
| `<C-y>`,`<C-i>`,`<C-n>`,`<C-s>` | n | Jump to Harpoon mark 1-4 |
| `<C-S-P>`/`<C-S-N>` | n    | Prev / Next Harpoon buffer   |

---

## HakonHarnes/img-clip.nvim

| Key           | Mode | Action                            |
|---------------|------|-----------------------------------|
| `<leader>pi`  | n    | Paste image from system clipboard |

---

## b0o/incline.nvim

File name + icon in window bar.

---

## hrsh7th/nvim-cmp (& dependencies)

Completion with snippets, LSP, Tailwind colorizer.

Essential mappings in Insert mode:

| Key           | Action                                 |
|---------------|----------------------------------------|
| `<C-e>`       | Abort completion                       |
| `<C-f>`/`<C-b>`| Scroll docs                           |
| `<Tab>`/`<S-Tab>` | Next/Prev item or snippet expansion|
| `<CR>`        | Confirm selection                      |
| `<C-y>`       | Confirm or fallback                    |

---

## nvim-lualine/lualine.nvim

Statusline with mode, branch, diff, filename, LSP update count.

---

## echasnovski/mini.*

- `mini.comment`: `gc` toggles comments using TS context.
- `mini.files`: `<leader>ee` or `<leader>ef` for file explorer.
- `mini.surround`: `sa`/`sr`/`ds` etc. for surroundings.
- `mini.trailspace`: `<leader>cw` to trim trailing whitespace.
- `mini.splitjoin`: `sj`/`sk` to join/split.

| Command                     | Description                          |
|-----------------------------|--------------------------------------|
| `:lua MiniFiles.open()`     | Open file explorer                   |
| `:lua MiniFiles.open(vim.api.nvim_buf_get_name(0))` | Open explorer on current file |

---

## folke/trouble.nvim

| Key               | Mode | Action                           |
|-------------------|------|----------------------------------|
| `<leader>xw`      | n    | Toggle workspace diagnostics     |
| `<leader>xd`      | n    | Toggle buffer diagnostics        |
| `<leader>xq`      | n    | Toggle quickfix                  |
| `<leader>xl`      | n    | Toggle loclist                   |
| `<leader>xt`      | n    | Toggle TODO view                 |

| Commands           | Description                    |
|--------------------|--------------------------------|
| `:Trouble`         | Open Trouble with default view |
| `:TroubleClose`    | Close Trouble window           |
| `:TroubleToggle`   | Toggle Trouble window          |

---

## mbbill/undotree

| Key           | Mode | Action           |
|---------------|------|------------------|
| `<leader>u`   | n    | Toggle UndoTree  |

| Command       | Description           |
|---------------|-----------------------|
| `:UndotreeToggle` | Toggle UndoTree view |

---

## nvim-tree/nvim-tree.lua (disabled)

| Key           | Mode | Action                   |
|---------------|------|--------------------------|
| `<leader>ee`  | n    | Toggle file explorer     |
| `<leader>ef`  | n    | Focus current file in tree|
| `<leader>ec`  | n    | Collapse file explorer   |
| `<leader>er`  | n    | Refresh file explorer    |

| Commands           | Description                  |
|--------------------|------------------------------|
| `:NvimTreeToggle`  | Toggle file explorer widget  |
| `:NvimTreeFindFile`| Reveal current file in tree  |
| `:NvimTreeOpen`    | Open file explorer           |
| `:NvimTreeClose`   | Close file explorer          |

---

## kevinhwang91/nvim-ufo

| Key           | Mode | Action                    |
|---------------|------|---------------------------|
| `zR`          | n    | Open all folds            |
| `zM`          | n    | Close all folds           |

---

## stevearc/oil.nvim

| Key           | Mode | Action                    |
|---------------|------|---------------------------|
| `-`           | n    | Open parent directory      |
| `<leader>-`   | n    | Toggle oil float            |

---

## MeanderingProgrammer/render-markdown.nvim

Enhances markdown headings, code blocks, bullets, checkboxes.

---

## folke/snacks.nvim

| Key           | Mode | Action                                  |
|---------------|------|-----------------------------------------|
| `<leader>lg`  | n    | `snacks.lazygit()`                      |
| `<leader>gl`  | n    | `snacks.lazygit.log()`                  |
| `<leader>rN`  | n    | Rename file                             |
| `<leader>dB`  | n    | Buffer delete                           |
| `<leader>pf`  | n    | Snacks finder: files                    |
| `<leader>pc`  | n    | Finder: config files                    |
| `<leader>ps`  | n    | Finder: grep word                       |
| `<leader>pws` | n/x  | Finder: grep selection                  |
| `<leader>pk`  | n    | Finder: search keymaps                  |
| `<leader>gbr` | n    | Finder: git branches (picker)           |
| `<leader>th`  | n    | Finder: colorschemes                    |
| `<leader>vh`  | n    | Finder: help pages                      |

---

## telescope.nvim

| Key           | Mode | Action                           |
|---------------|------|----------------------------------|
| `<leader>pr`  | n    | Recent files (`oldfiles`)        |
| `<leader>pWs` | n    | Grep WORD under cursor           |
| `<leader>ths` | n    | Theme switcher                   |

| Command                 | Description                                     |
|-------------------------|-------------------------------------------------|
| `:Telescope find_files` | Find files in current working directory         |
| `:Telescope live_grep`  | Live grep search across files                   |
| `:Telescope buffers`    | List open buffers                               |
| `:Telescope help_tags`  | Browse Neovim help pages                        |
| `:Telescope oldfiles`   | Fuzzy find recently opened files                |
| `:Telescope themes`     | Open theme switcher (telescope-themes extension) |

---

## nvim-treesitter

Automatic syntax, indentation, incremental selection:
- `<C-space>`: expand node

| Command                    | Description                                     |
|----------------------------|-------------------------------------------------|
| `:TSInstall <lang>`        | Install tree-sitter parser for `<lang>`         |
| `:TSUpdate`                | Update installed parsers                        |
| `:TSBufEnable highlight`   | Enable syntax highlighting for current buffer   |
| `:TSBufEnable indent`      | Enable indentation for current buffer           |
| `:TSBufDisable highlight`  | Disable syntax highlighting for current buffer  |
| `:TSBufDisable indent`     | Disable indentation for current buffer          |
