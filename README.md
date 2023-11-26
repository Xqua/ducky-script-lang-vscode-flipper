# Ducky Script Language for VSCode

This extension enables syntax highlighting for the **Ducky Script** scripting language with the **Flipper Zero** mods added, allowing for easier and more efficient scripting.
<br>

## Features

This extension works with **.txt files**.

Syntax detection features :
*   Detection and highlighting for **comment lines** (`REM` lines),
*   Detection and highlighting for **control keys** (`ENTER`, `ESC`, `GUI`, `ALT`, `CTRL` and so on  -- detailed list below),
*   Detection and highlighting for **flipper added control keys** (`CTRL-ALT`, `CTRL-SHIFT`, `ALT-SHIFT`, `ALT-GUI`, `GUI-SHIFT` and so on  -- detailed list below),
*   Detection and highlighting for **timer commands** (`DELAY`, `DEFAULTDELAY`, `REPEAT` and so on -- detailed list below),
*   Detection and highlighting for **strings** (`STRING` lines).

Detailed list of supported commands :

| Keyword                           | Category | Behaviour                               |
| --------------------------------- | :------: | --------------------------------------- |
| `REM`                             | Comment  | Turns the line into a comment           |
| `STRING`                          | Variable | Detects the following value as a string |
| `DELAY`                           | Variable | Detects the following value as a number |
| `DEFAULTDELAY` or `DEFAULT_DELAY` | Variable | Detects the following value as a number |
| `REPEAT`                          | Variable | Detects the following value as a number |
| `GUI`                             | Key      | Detects a keyboard key                  |
| `WINDOWS`                         | Key      | Detects a keyboard key                  |
| `APP`                             | Key      | Detects a keyboard key                  |
| `MENU`                            | Key      | Detects a keyboard key                  |
| `SHIFT`                           | Key      | Detects a keyboard key                  |
| `ALT`                             | Key      | Detects a keyboard key                  |
| `CTRL` or `CONTROL`               | Key      | Detects a keyboard key                  |
| `DOWNARROW` or `DOWN`             | Key      | Detects a keyboard key                  |
| `UPARROW` or `UP`                 | Key      | Detects a keyboard key                  |
| `LEFTARROW` or `LEFT`             | Key      | Detects a keyboard key                  |
| `RIGHTARROW` or `RIGHT`           | Key      | Detects a keyboard key                  |
| `BREAK`                           | Key      | Detects a keyboard key                  |
| `PAUSE`                           | Key      | Detects a keyboard key                  |
| `CAPSLOCK`                        | Key      | Detects a keyboard key                  |
| `DELETE`                          | Key      | Detects a keyboard key                  |
| `END`                             | Key      | Detects a keyboard key                  |
| `ENTER`                           | Key      | Detects a keyboard key                  |
| `ESCAPE` or `ESC`                 | Key      | Detects a keyboard key                  |
| `HOME`                            | Key      | Detects a keyboard key                  |
| `INSERT`                          | Key      | Detects a keyboard key                  |
| `NUMLOCK`                         | Key      | Detects a keyboard key                  |
| `PAGEUP`                          | Key      | Detects a keyboard key                  |
| `PAGEDOWN`                        | Key      | Detects a keyboard key                  |
| `PRINTSCREEN`                     | Key      | Detects a keyboard key                  |
| `SCROLLLOCK`                      | Key      | Detects a keyboard key                  |
| `SPACE`                           | Key      | Detects a keyboard key                  |
| `TAB`                             | Key      | Detects a keyboard key                  |
| `CTRL-ALT`                        | Key      | Detects a keyboard key                  |
| `CTRL-SHIFT`                      | Key      | Detects a keyboard key                  |
| `ALT-SHIFT`                       | Key      | Detects a keyboard key                  |
| `ALT-GUI`                         | Key      | Detects a keyboard key                  |
| `GUI-SHIFT`                       | Key      | Detects a keyboard key                  |
| `ALTCHAR`                         | Key      | ALT+Numpad input                        |
| `ALTSTRING`                       | Key      | ALT+Numpad input                        |
| `ALTCODE`                         | Key      | ALT+Numpad input                        |
| `SYSRQ`                           | Key      | Detects a keyboard key                  |

## Flipper mods

Below you can find the commands Flipper Zero can execute in addition to the Rubber Ducky Scripting Language 1.0 syntax.

### Modifier keys

|   Command       |   Notes      |
|   `CTRL-ALT`    |   CTRL+ALT   |
|   `CTRL-SHIFT`  |   CTRL+SHIFT |
|   `ALT-SHIFT`   |   ALT+SHIFT  |
|   `ALT-GUI`     |   ALT+WIN    |
|   `GUI-SHIFT`   |   WIN+SHIFT  |

### ALT+Numpad input

On Windows, you can input characters by pressing the ALT key and entering its code on the Numpad.

|   Command       |   Parameters      |   Notes                                                              |
|   `ALTCHAR`     |   Character code  |   Print single character                                             |
|   `ALTSTRING`   |   Text string     |   Print text string using ALT+Numpad method                          |
|   `ALTCODE`     |   Text string     |   Same as ALTSTRING, presented in some Ducky Script implementations  |


### Magic SysRq key

On Linux, you can execute commands using the Magic SysRq Key.

|   Command     |   Parameters        |
|   `SYSRQ`     |   Single character  |

<br>

## Known Issues

This extension does not yet provide syntax error detection, the problematic phrases are just **not highlighted**.

<br>

## Related projects

### Ducky Script OS-specific payloads

Here is another repo of mine containing a compilation of Ducky Script payloads sorted by OS and by distribution, which you can adapt to your needs : <br>
https://github.com/cvbenur/ducky-scripts-and-payloads

<br>

## Releases

### 1.0.6 - Nov, 2023

Added the Flipper Zero mods

### 1.0.5 - March 7th, 2020

Added an icon to the extension. It can be found under `./img/icon.png`.

Here it is :
<p align="center">
    <img width=128 height=128 src="./img/icon.png">
</p>

<br>

### 1.0.2 - March 6th, 2020

Improved detection of single-line command/letter key combinations.

Certain combinations would not get detected in cases with more than 2 successive commands/letter keys.
In those cases, only the 2 first instructions of each line woud get detected.
> **E.g.** `CTRL ALT DELETE` would only detect `CTRL ALT`.

Detection now works for potentially infinite single-line command/letter key combinations.

<br>

### 1.0.1 - March 4th, 2020

Improved detection of error-prone keyword use cases.

Certain inline keyword combinations resulted in false positives, and thus errors in highlighting.
> **E.g.** Certain `REM` lines would highlight other keywords and variables instead of treating them as comments.

<br>

### 1.0.0 - March 4th, 2020

Initial release of the **Ducky Script Language for VSCode** extension.

. . .
<br>

### About this extension

Written by **benur**. The source code to this extension is free to download and tweak or customize for your personnal use only.

This is my very first extension, so feedback is much appreciated ! :)

**Enjoy!**
