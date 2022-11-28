# README

WPF cheatsheet [web site](https://xdvarpunen.github.io/wpf-cheatsheet/).

## .gitignore

Copied base from here https://raw.githubusercontent.com/github/gitignore/main/Python.gitignore.

## Venv

```powershell
python -m venv venv
.\venv\Scripts\activate
deactivate
```

# Dependencies

```powershell
python -m pip freeze > requirements.txt
python -m pip install -r requirements.txt
```

# MkDocs

For full documentation visit [mkdocs.org](https://www.mkdocs.org).

## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.
