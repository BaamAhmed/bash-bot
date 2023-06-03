# BashBot
> Work In Progress

BashBot brings the power of OpenAI's `gpt-3.5-turbo` to your command-line, plus gives you the additional ability to work in the console while talking to ChatGPT, autosaving code that ChatGPT generates, and giving you the ability to quickly save, run, and view that generated code.

> Note: For the time being, to get a license key, contact me at b3ahmed@uwaterloo.ca. I'm working on automating this, but it's under development.

## Installation and Config
```shell
// installing
$: pip install bashbot

// setting up - you will need a valid openAI key and license key
$:  bashbot config
```

## Usage
```shell
// starting BashBot session with autosave = on and language = JS
$: bashbot -S js

```

## Flags
* `-S [lang]`: Autosave generated code in specified language (either `js`, `py`, `c`, or `jsx`)
* `-N [name]`: Name of autosaved code (default: bashbot_code)
* `-P [relative path]`: Path where code will be autosaved (default: directory from which bashbot was called)
* `-L`: Enable logging

## Special Keywords:
These words, if entered by themselves during a BashBot session, will trigger different things locally but will not be sent as a prompt to ChatGPT:
* `console`: opens the system console, use `exit_console` to return to the BashBot session
* `run`: run the last saved code
* `open`: open the last saved code in vim in the terminal
* `exit`: terminate the BashBot session


## Languages:
Through the `-S` flag, code generated in these languages will be saved, and can be executed without leaving the BashBot session.
* Python
* JavaScript
* JSX (React)
* C
