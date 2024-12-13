# qute-translate-popup

[userscript](https://github.com/qutebrowser/qutebrowser/blob/master/doc/userscripts.asciidoc) for [qutebrowser](https://github.com/qutebrowser/qutebrowser) for translation of pages or selected text using [Google translate](https://translate.google.com/)/[LibreTranslate](https://github.com/LibreTranslate/LibreTranslate). Makes a qute popup!

## Installation
Copy the file `translate` to the qutebrowser's userscripts directory (`~/.config/qutebrowser/userscripts`) and make it executable.

## Usage
### Translate page
To translate the current page
```
spawn --userscript translate --url
```
You can specify target language. For example to translate to Georgian do
```
spawn --userscript translate --target_lang ka
```

### Translate selected text
This translates the selection and calls a small JS snippet to display a popup in bottom right corner. To dismiss the popup click outside of it.
```
spawn --userscript translate
```

### In hint mode
The userscript can also be used in hint mode by doing
```
hint links userscript translate
```

## Key-bindings
```python
config.bind('tt', 'spawn --userscript translate')
```

## NixOS
You can use nix-shell shebang for python dependency management
```bash
#! /usr/bin/env nix-shell
#! nix-shell -i python3 -p python3Packages.requests
```
 
## Alternatives
Check out [Qute-Translate](https://github.com/AckslD/Qute-Translate/)!
