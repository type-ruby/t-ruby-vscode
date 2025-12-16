# T-Ruby for VS Code & Cursor

[![T-Ruby](https://img.shields.io/gem/v/t-ruby?label=T-Ruby)](https://rubygems.org/gems/t-ruby)
[![License](https://img.shields.io/github/license/type-ruby/t-ruby-vscode)](LICENSE)

**VS Code**  
[![Extension](https://img.shields.io/visual-studio-marketplace/v/t-ruby.t-ruby?label=Extension)](https://marketplace.visualstudio.com/items?itemName=t-ruby.t-ruby) [![Downloads](https://img.shields.io/visual-studio-marketplace/i/t-ruby.t-ruby?label=Downloads)](https://marketplace.visualstudio.com/items?itemName=t-ruby.t-ruby)

**Cursor (Open VSX)**  
[![Extension](https://img.shields.io/open-vsx/v/t-ruby/t-ruby?label=Extension)](https://open-vsx.org/extension/t-ruby/t-ruby) [![Downloads](https://img.shields.io/open-vsx/dt/t-ruby/t-ruby?label=Downloads)](https://open-vsx.org/extension/t-ruby/t-ruby)

T-Ruby language support for VS Code and Cursor. Provides syntax highlighting, LSP-based code intelligence, and development tools for [T-Ruby](https://github.com/type-ruby/t-ruby) - a TypeScript-style static type system for Ruby.

## Features

- Syntax highlighting for `.trb` and `.d.trb` files
- LSP-based code intelligence:
  - Real-time diagnostics (type errors)
  - Autocomplete suggestions
  - Go to definition
  - Hover information
- Commands:
  - `T-Ruby: Compile Current File` - Compile the current `.trb` file
  - `T-Ruby: Generate Declaration File` - Generate `.d.trb` declaration file
  - `T-Ruby: Restart Language Server` - Restart the LSP server

## Requirements

- [T-Ruby Compiler](https://github.com/type-ruby/t-ruby) (`trc`) must be installed and available in your PATH

```bash
gem install t-ruby
```

## Installation

### VS Code

Install from the [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=t-ruby.t-ruby):

1. Open VS Code
2. Go to Extensions (Ctrl+Shift+X)
3. Search for "T-Ruby"
4. Click Install

Or install via command line:

```bash
code --install-extension t-ruby.t-ruby
```

### Cursor

Install from the [Open VSX Registry](https://open-vsx.org/extension/t-ruby/t-ruby):

1. Open Cursor
2. Go to Extensions (Ctrl+Shift+X)
3. Search for "T-Ruby"
4. Click Install

## Configuration

| Setting | Default | Description |
|---------|---------|-------------|
| `t-ruby.lspPath` | `trc` | Path to the T-Ruby compiler executable |
| `t-ruby.enableLSP` | `true` | Enable Language Server Protocol support |
| `t-ruby.diagnostics.enable` | `true` | Enable real-time diagnostics |
| `t-ruby.completion.enable` | `true` | Enable autocomplete suggestions |

## Related

- [T-Ruby Compiler](https://github.com/type-ruby/t-ruby) - The main T-Ruby compiler
- [T-Ruby JetBrains](https://github.com/type-ruby/t-ruby-jetbrains) - JetBrains IDE plugin
- [T-Ruby Vim](https://github.com/type-ruby/t-ruby-vim) - Vim/Neovim plugin

## License

BSD 2-Clause
