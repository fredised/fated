# Fated - Text Effects Library for Python

![Version](https://img.shields.io/pypi/v/fated)
![Python Version](https://img.shields.io/pypi/pyversions/fated)
![License](https://img.shields.io/github/license/fredised/fated)

Fated is a Python library that adds visual effects to text output including typewriter animation and other text styling options. It provides a simple API for creating rich, animated terminal text with no external dependencies.

Make your terminal applications more engaging with smooth animations, colorful text, and eye-catching effects!

## Features

- **Text Animation Effects**: Typewriter, blink, fade-in, wave, glitch, shake, matrix, and more
- **Text Styling**: Colors, background colors, bold, italic, underline, and other text styles
- **Chainable Effects**: Combine multiple effects together seamlessly
- **Simple API**: Intuitive interface that works with standard print function
- **Alternative Syntax**: Use the + operator with shortcut objects for even cleaner code
- **No Dependencies**: Uses only Python standard library modules
- **Cross-Platform**: Works on Windows, macOS, and Linux terminals that support ANSI escape codes

## Installation

Install directly from PyPI using pip:

```bash
pip install fated
```
## Compatibility

Fated works best in terminals that support ANSI escape codes:
- Modern versions of Windows Terminal, PowerShell, and cmd.exe
- macOS Terminal, iTerm2
- Linux terminals (GNOME Terminal, Konsole, xterm, etc.)
- VS Code integrated terminal
- Jupyter notebooks (results may vary)

## Usage

### Traditional Syntax

```python
from fate import typewriter, color, style

# Simple typewriter effect
print(typewriter("Hello, World!"))

# Colored text
print(color.red("This text is red"))
print(color.blue("This text is blue"))

# Text styling
print(style.bold("Bold text"))
print(style.italic("Italic text"))

# Chain multiple effects
print(style.bold(color.green(typewriter("Bold green typewriter text"))))

# Predefined combinations
from fate import error, warning, success, info
print(error("Error message"))
print(success("Success message"))
```

### Shortcut Syntax (New!)

```python
from fate.shortcuts import fateTypeWriter, fateRed, fateBold

# Use the + operator
print(fateTypeWriter + "Hello, World!")

# Colored text
print(fateRed + "This text is red")

# Text styling
print(fateBold + "Bold text")

# Custom parameters
print(fateTypeWriter(speed=20) + "Fast typing!")

# Predefined combinations
from fate.shortcuts import fateError, fateSuccess
print(fateError + "Error message")
print(fateSuccess + "Success message")
```

## Examples

The repository includes example files:

- `examples.py` - Demonstrates the traditional syntax
- `shortcut_example.py` - Demonstrates the new shortcut syntax

Run the examples to see the library in action:

```bash
python examples.py
python shortcut_example.py
```

## Available Effects

- `typewriter` - Types text character by character
- `blink` - Makes text blink
- `fade_in` - Gradually reveals text
- `wave` - Creates a wave-like animation
- `glitch` - Creates a glitchy, distorted effect
- `shake` - Shakes the text
- `rainbow` - Cycles through rainbow colors
- `typing_with_errors` - Realistic typing with random errors
- `matrix_effect` - Matrix-like falling character effect
- `slide_in` - Slides text in from left or right
- `reveal_masked` - Reveals masked text character by character

  ## This Was generated fully with replit agent
