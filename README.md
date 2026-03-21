# aspias-zsh-theme

A clean and customizable Zsh theme based on Oh My Zsh's 'clean' theme, with Git integration and OS-aware styling.

## Features

- **Customizable Colors**: Override default colors for namespace, path, user/host, and root via environment variables.
- **OS-Aware Host Coloring**: Automatically sets host color based on OS (yellow for OpenBSD, red for FreeBSD, white otherwise).
- **Hostname Length-Based Coloring**: Optionally use consistent colors based on hostname length for per-machine theming.
- **Root Detection**: Switches user color to red when running as root.
- **Namespace Support**: Display an optional namespace prefix (e.g., project name) in brackets.
- **Git Integration**: Shows Git branch and status with clean/dirty indicators (✓/✗).
- **LS Colors**: Configures file type colors for `ls` output on both BSD/macOS and Linux.
- **Minimal Prompt**: Clean format: `[namespace] user@host:path/ git_info #/$`

## Installation

1. Ensure you have [Oh My Zsh](https://ohmyz.sh/) installed.
2. Clone or download this repository.
3. Copy `aspias.zsh-theme` to your Oh My Zsh themes directory:
   ```
   cp aspias.zsh-theme ~/.oh-my-zsh/themes/
   ```
4. Set the theme in your `~/.zshrc`:
   ```
   ZSH_THEME=aspias
   ```
5. Reload your Zsh configuration:
   ```
   source ~/.zshrc
   ```

## Customization

Customize colors by setting environment variables in your `~/.zshrc` before sourcing the theme:

```zsh
export ASPIAS_NAMESPACE_COLOR=yellow
export ASPIAS_PATH_COLOR=blue
export ASPIAS_USER_COLOR=white
export ASPIAS_ROOT_COLOR=red
export ASPIAS_HOST_COLOR=white
```

Available colors: black, red, green, yellow, blue, magenta, cyan, white.

For hostname-based coloring, set:
```zsh
export ASPIAS_HOST_COLOR_MODE=hostname_length
```

This assigns a consistent color based on your hostname's length (cycles through red, green, yellow, blue, magenta, cyan, white).

To display a namespace (e.g., current project):
```zsh
export ASPIAS_NAMESPACE=myproject
```

## Example Prompt

```
[myproject] user@host:~ (master ✓) $
```

- `[myproject]`: Namespace (if set)
- `user@host`: User and host (host color varies by OS or hostname length)
- `~`: Current directory
- `(master ✓)`: Git branch and clean status
- `$`: Prompt symbol (changes to `#` for root)

## Requirements

- Zsh
- Oh My Zsh
- Git (for Git integration)</content>
<parameter name="filePath">/home/lotherk/Sync/code/aspias-zsh-theme/README.md