# Ocelescope Plugin Template

- This is a plugin template for the Ocelescope framework.

- The plugin template is a good starting point for your own ocelescope plugin.

- A empty plugin is located at `./src/plugin-template/plugin.py`

- I highly recommend also using uv as a package manager.

## First Steps

  1. Install dependencies with

  ```sh
  uv sync
  ```

  or using the requirment.txt

  ```sh
  pip install -r requirements.txt
  ```

  1. Rename the Template plugin

  Rename the name of the class and also the label and description

  ```python "src/plugin-template/plugin.py"
  
  class PluginTemplate(Plugin):  # Rename me
    label = "Minimal Plugin" # Change Me
    description = "A ocelescope plugin" #Change Me
    version = "0.1.0"

    ...

  ```

  Don't forget to also change the import in the `__init__.py`

  ```python "src/plugin-template/plugin.py"
  
  from .plugin import PluginTemplate #Change Me

  __all__ = ["PluginTemplate"] #Change Me
  ```
  
## Building

You can either zip the src folder yourself

```sh
plugin.zip/
└──plugin-template/
    ├── __init__.py  # Entry point
    ├── plugin.py
```

or using the ocelescope command

```sh
ocelescope build
```

or if you are using uv

```sh
uv run ocelescope build
```

## Using the github workflow

by pushing tags you can also use the github workflow

... how to trigger workflow
