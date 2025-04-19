# PyFetch

A fork of Neofetch written entirely in Python. Displays system information with Neofetch-style ASCII art.

## Features
- **Cross-platform**: works on Windows, Linux, and macOS
- **Comprehensive system information**: displays username, hostname, OS, kernel, uptime, packages, shell, resolution, DE/WM, terminal, CPU, GPU, RAM, disk, temperature
- **ASCII Art**: uses the same ASCII art as Neofetch, with support for custom art
- **ANSI Colors**: full support for color terminals
- **Configurable**: customizable configurations via JSON files
- **Portable**: written entirely in Python, easily extensible

## Installation

### Requirements
- Python 3.6 or higher
- `psutil` module: `pip install psutil`

### Manual Installation
```bash
git clone https://github.com/dddevid/pyfetch.git
cd pyfetch
pip install -r requirements.txt
```
Alternatively, you can install PyFetch via pip:
```bash
pip install git+https://github.com/dddevid/pyfetch.git
```

## Usage
Run PyFetch from the command line:
```bash
python pyfetch.py
```
Or, if installed via pip:
```bash
pyfetch
```

### Options
- `--ascii FILE`: Use a custom ASCII file
- `--ascii_distro DISTRO`: Use ASCII art from a specific distribution
- `--config FILE`: Use a custom configuration file
- `--no_color`: Disable colors
- `--version`: Show PyFetch version

## Configuration
PyFetch can be configured via a JSON configuration file. The default configuration file is located at:
- **Linux/macOS**: `~/.config/pyfetch/config.json` or `~/.pyfetch.json`
- **Windows**: `%APPDATA%\PyFetch\config.json` or `~/pyfetch.json`

### Configuration Example
```json
{
    "show_ascii": true,
    "show_colors": true,
    "show_color_blocks": true,
    "info": {
        "os": true,
        "kernel": true,
        "uptime": true,
        "packages": true,
        "shell": true,
        "resolution": true,
        "de": true,
        "wm": true,
        "terminal": true,
        "cpu": true,
        "gpu": true,
        "memory": true,
        "disk": true,
        "temperatures": true
    },
    "ascii_art": {
        "use_custom": false,
        "custom_path": "",
        "distro_override": ""
    }
}
```

## Extension
PyFetch is designed to be easily extensible. You can add new features by modifying the following files:
- `system_info.py`: Add new methods for collecting system information
- `ascii_art.py`: Add new ASCII art for distributions or operating systems
- `config.py`: Add new configuration options

## Contributing
Contributions are welcome! If you want to contribute to PyFetch, follow these steps:
1. Fork the repository
2. Create a branch for your feature (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Added a new feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License
Distributed under the MIT License. See `LICENSE` for more information.

## Acknowledgments
- [Neofetch](https://github.com/dylanaraps/neofetch) - The original inspiration for this project
