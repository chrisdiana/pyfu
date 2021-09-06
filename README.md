# pyfu

> Run and debug Python functions from CLI

Pyfu is a small utility for running Python functions from command line.
With pyfu you can run functions from CLI on standard Python packages and modules without any additional packages or dependencies.

### How to use

Call pyfu followed by your Python package or module along with any
function arguments to run the function without leaving the terminal.

```
$ pyfu mypackage.module_a.foo bar
```

### Installation:

```
$ git clone git@github.com:chrisdiana/pyfu.git
$ sudo sh install.sh
```

### Example

For example, if your Python package is:

```
mypackage_directory
  └─mypackage
     ├── __init__.py
     └── module_a.py

```

And module_a.py contains:

```python
def foo(bar):
    print(bar)
```

Then from `mypackage_directory` you can execute the `foo` function using:

```
$ pyfu mypackage.module_a.foo bar
```

### Why?

Python has a great interface for running modules and scripts from command line but there isn’t any built in way to run individual functions. There are some great packages out there that can help solve this problem ([click](https://github.com/pallets/click), [invoke](https://github.com/pyinvoke/invoke)) but at the expense of adding complexity and additional dependencies.

Pyfu allows for functional access to Python files without polluting the code with extra decorators or options and without additional packages or libraries.


