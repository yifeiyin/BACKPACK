Use Package Control

### Install: 
* Sublime REPL 
* SublimeCodeIntel (for code completion)
* MagicPython (for better python highlighting)

### Under Sublime Key Bindings, add:
```
// ////// command r and command b both work, they are only active in python context
{
        "keys": ["super+r"],
        "caption": "SublimeREPL: Python - RUN current file",
        "command": "run_existing_window_command",
        "args": {
            "id": "repl_python_run",
            "file": "config/Python/Main.sublime-menu"
        },
                "context": [
        { "key": "selector", "operator": "equal", "operand": "source.python" }]
    },
    {
        "keys": ["super+b"],
        "caption": "SublimeREPL: Python - RUN current file",
        "command": "run_existing_window_command",
        "args": {
            "id": "repl_python_run",
            "file": "config/Python/Main.sublime-menu"
        },
        "context": [
        { "key": "selector", "operator": "equal", "operand": "source.python" }]
    },
```

### Under SublimeREPL Settings, add:
```
// standard sublime view settings that will be overwritten on each repl view
// this has to be customized as a whole dictionary

// ///////// For syntax highlighting
{
    "repl_view_settings": {
        "syntax": "Packages/Text/Plain text.tmLanguage"
    },
}
```
