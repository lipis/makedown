# XFile

`xfile` is a versatile CLI tool that lets you execute shell scripts,
JavaScript code, and Python code from one or more markdown files.
It's a streamlined alternative to `Makefile` or `package.json` scripts,
and it features built-in syntax highlighting through markdown code blocks.

## Key Features

- Multilingual Execution: Supports Zsh, JavaScript, and Python.
- Simplified Scripting: Use markdown files (.md) to organize and run commands.
- Syntax Highlighting: Leverages markdown code blocks for readability.
- Autocomplete Support: ZSH completions for a smoother workflow.

## Installation

```zsh
npm install -g x.md
```

## Usage

Create a file named `x.md` in your project root, with the following example content:

    <!-- /path/to/my/project/x.md -->

    # hello

    Prints "Hello" to `stdout` using Zsh.

    ```zsh
    echo "Hello"
    ```

    # world

    Just prints "World" to `stdout` using JavaScript.

    ```js
    console.log("World");
    ```

    # generate-password

    Prints a random password to `stdout` using Python.

    ```python
    import random
    import string

    length = 16

    characters = string.ascii_letters + string.digits + string.punctuation
    password = ''.join(random.choice(characters) for _ in range(length))
    print(password)
    ```

Run `x generate-password` to generate a random password.

## Command line completions for ZSH

Run the following once to add `x` command completions to your `.zshrc`:

```zsh
x --zsh-completion >> ~/.zshrc
```

Then restart your terminal.

It will suggest available commands when you type `x` and press tab.
