# Neovim Configuration (MiniMax)

## 🛠️ Basic Information

- **Neovim Version**: `v0.12+` (Required for native `vim.pack` features)
- **Core Framework**: [mini.nvim](https://github.com/echasnovski/mini.nvim)
- **Plugin Manager**: Built-in Neovim `vim.pack` (managed via `nvim-pack-lock.json`)

## 🧩 Active Plugins

This configuration strictly curates its plugins to avoid bloat. Most functionality is provided by the modular `mini.nvim` library, supplemented by a few essential external tools for language intelligence.

### Core Ecosystem (`mini.nvim` modules)

The following modules from `mini.nvim` are enabled and configured in `plugin/30_mini.lua`:

**UI & Navigation**

- `mini.starter`: Minimalist dashboard/start screen.
- `mini.statusline` & `mini.tabline`: Fast, out-of-the-box status and buffer lines.
- `mini.files`: Buffer-like file explorer (replaces traditional sidebar trees).
- `mini.pick`: Extremely fast built-in fuzzy finder (replaces Telescope).
- `mini.clue`: Keybinding discoverability (replaces WhichKey).
- `mini.map`: Text overview minimap.
- `mini.notify`: Notification manager.

**Editing & Text Objects**

- `mini.ai` & `mini.extra`: Enhanced text objects (e.g., inside functions, whole buffers).
- `mini.surround`: Add, delete, or replace surrounding characters (quotes, brackets).
- `mini.operators`: Advanced text edit operators (e.g., swap arguments, evaluate Lua code).
- `mini.pairs`: Autopairs functionality.
- `mini.comment`: Context-aware commenting.
- `mini.align` & `mini.splitjoin`: Text alignment and argument splitting/joining.
- `mini.snippets`: Minimal snippet expansion engine.

**Workflow & Utilities**

- `mini.completion`: Fast, two-stage async LSP autocompletion.
- `mini.diff` & `mini.git`: Git hunk management and integration inside buffers.
- `mini.sessions`: Session management (`:mksession` wrapper).
- `mini.jump` & `mini.jump2d`: Advanced cross-line jumping (replaces tools like Flash/Hop).
- `mini.visits`: Persistent tracking and navigation of visited files.

### External Plugins

Configured in `plugin/40_plugins.lua`, these provide language parsing, LSP support, and formatting:

- **[nvim-treesitter](https://github.com/nvim-treesitter/nvim-treesitter)**: Advanced incremental syntax highlighting and AST parsing.
- **[nvim-treesitter-textobjects](https://github.com/nvim-treesitter/nvim-treesitter-textobjects)**: Tree-sitter powered text objects.
- **[nvim-lspconfig](https://github.com/neovim/nvim-lspconfig)**: Quickstart configurations for the native Neovim LSP client.
- **[conform.nvim](https://github.com/stevearc/conform.nvim)**: Lightweight and robust code formatting engine.
- **[friendly-snippets](https://github.com/rafamadriz/friendly-snippets)**: Collection of pre-configured snippets for multiple languages (used with `mini.snippets`).
