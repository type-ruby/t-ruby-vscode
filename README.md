<p align="center">
  <img src="https://avatars.githubusercontent.com/u/248530250" alt="T-Ruby" height="120">
</p>

<h1 align="center">T-Ruby for VS Code & Cursor</h1>

<p align="center">
  <a href="https://type-ruby.github.io">Official Website</a>
  &nbsp;&nbsp;•&nbsp;&nbsp;
  <a href="https://github.com/type-ruby/t-ruby">GitHub</a>
  &nbsp;&nbsp;•&nbsp;&nbsp;
  <a href="https://marketplace.visualstudio.com/items?itemName=t-ruby.t-ruby">VS Code Marketplace</a>
  &nbsp;&nbsp;•&nbsp;&nbsp;
  <a href="https://open-vsx.org/extension/t-ruby/t-ruby">Cursor Marketplace</a>
</p>

<p align="center">
  <a href="https://rubygems.org/gems/t-ruby"><img src="https://img.shields.io/gem/v/t-ruby?label=T-Ruby" alt="T-Ruby"></a>
  <a href="LICENSE"><img src="https://img.shields.io/github/license/type-ruby/t-ruby-vscode" alt="License"></a>
</p>

<p align="center">
  <strong>VS Code</strong><br>
  <a href="https://marketplace.visualstudio.com/items?itemName=t-ruby.t-ruby"><img src="https://img.shields.io/visual-studio-marketplace/v/t-ruby.t-ruby?label=Extension" alt="Extension"></a>
  <a href="https://marketplace.visualstudio.com/items?itemName=t-ruby.t-ruby"><img src="https://img.shields.io/visual-studio-marketplace/i/t-ruby.t-ruby?label=Downloads" alt="Downloads"></a>
</p>

<p align="center">
  <strong>Cursor (Open VSX)</strong><br>
  <a href="https://open-vsx.org/extension/t-ruby/t-ruby"><img src="https://img.shields.io/open-vsx/v/t-ruby/t-ruby?label=Extension" alt="Extension"></a>
  <a href="https://open-vsx.org/extension/t-ruby/t-ruby"><img src="https://img.shields.io/open-vsx/dt/t-ruby/t-ruby?label=Downloads" alt="Downloads"></a>
</p>

---

T-Ruby language support for VS Code and Cursor. Provides syntax highlighting, LSP-based code intelligence, and development tools for [T-Ruby](https://github.com/type-ruby/t-ruby) - a TypeScript-style static type system for Ruby.

> **Note**: This extension shares the same source code for both VS Code and Cursor, providing identical functionality in both editors.

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

After installation, configure the extension in VS Code settings (`Ctrl+,`):

```json
{
  "t-ruby.lspPath": "trc",
  "t-ruby.enableLSP": true,
  "t-ruby.diagnostics.enable": true,
  "t-ruby.completion.enable": true
}
```

### Configuration Options

| Option | Type | Default | Description |
|--------|------|---------|-------------|
| `t-ruby.lspPath` | string | `"trc"` | Path to T-Ruby compiler |
| `t-ruby.enableLSP` | boolean | `true` | Enable Language Server |
| `t-ruby.diagnostics.enable` | boolean | `true` | Enable real-time diagnostics |
| `t-ruby.completion.enable` | boolean | `true` | Enable autocomplete |

## Features

### Syntax Highlighting

The extension provides full syntax highlighting for:
- `.trb` files (T-Ruby source files)
- `.d.trb` files (T-Ruby declaration files)

Type annotations, interfaces, and type aliases are highlighted distinctly.

### IntelliSense

- **Autocomplete**: Type suggestions for parameters and return types
- **Hover**: View type information by hovering over symbols
- **Go to Definition**: Navigate to type/function definitions

### Diagnostics

Real-time error checking for:
- Unknown types
- Duplicate definitions
- Syntax errors

### Commands

Access via Command Palette (`Ctrl+Shift+P`):

| Command | Description |
|---------|-------------|
| `T-Ruby: Compile Current File` | Compile the active `.trb` file |
| `T-Ruby: Generate Declaration File` | Generate `.d.trb` from source |
| `T-Ruby: Restart Language Server` | Restart the LSP server |

## Quick Start Example

1. Create a new file `hello.trb`:

```trb
type UserId = String

interface User
  id: UserId
  name: String
  age: Integer
end

def greet(user: User): String
  "Hello, #{user.name}!"
end
```

2. Save the file - you'll see syntax highlighting and real-time diagnostics

3. Hover over types to see their definitions

4. Use `Ctrl+Space` for autocomplete suggestions

## Troubleshooting

### LSP not starting

1. Check if `trc` is installed: `which trc`
2. Verify the path in settings: `t-ruby.lspPath`
3. Check Output panel: View > Output > T-Ruby Language Server

### No syntax highlighting

1. Ensure file has `.trb` or `.d.trb` extension
2. Check file association: View > Command Palette > "Change Language Mode"

### Performance issues

- Disable diagnostics for large files: `"t-ruby.diagnostics.enable": false`
- Restart the language server: Command Palette > "T-Ruby: Restart Language Server"

## Contributing

Issues and pull requests are welcome!
https://github.com/type-ruby/t-ruby-vscode/issues

## Related

- [T-Ruby Compiler](https://github.com/type-ruby/t-ruby) - The main T-Ruby compiler
- [T-Ruby JetBrains](https://github.com/type-ruby/t-ruby-jetbrains) - JetBrains IDE plugin
- [T-Ruby Vim](https://github.com/type-ruby/t-ruby-vim) - Vim/Neovim plugin

## License

BSD 2-Clause
