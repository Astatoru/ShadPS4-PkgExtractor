# ShadPS4Plus-PkgExtractor Linux Wrapper Script

Wrapper script for the [shadPS4Plus extractor tool](https://github.com/AzaharPlus/shadPS4Plus) that extracts packages (.pkg) and puts them into correct directories.

## Requirements

- Linux
- Executable `extractor.AppImage` placed in the same directory (you can use executable from original repository if you don't trust mine)

## Usage

```bash
./extract [OPTIONS] PACKAGE.pkg [PACKAGE2.pkg ...]
```

### Options

| Option | Description | Default Value |
| :--- | :--- | :--- |
| `-g, --games-directory` | Path to games directory* | None |
| `-a, --addons-directory` | Path to DLC directory** | `~/.local/share/shadPS4/addcont` |
| `-h, --help` | Display help message | - |

\* **Settings > Configure > Paths > Game Folders**

\** **Settings > Configure > Paths > DLC Path**

## Examples

- Extract base game and update:
```bash
./extract --game-directory /path/to/games/directory package_game.pkg package_update.pkg
```
- Extract game and update in place (next to .pkg file):
```bash
./extract package_game.pkg package_update.pkg
```
