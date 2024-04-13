## Introduction

Basic pre-commit usage.

## Installation

Root permissions are not required:

```bash
pip install -r requirements-dev.txt
```

Verify the installation:

```bash
pre-commit --version
```

### Configuration

Copy the following files to the root path of your project:

- `.flake8`. A configuration file for the Flake8 library.
- `.pre-commit-config.yaml`. File with the hooks to apply to the project's files. Hook example: the Black library.
- `pyproject.toml`. A configuration file for the Black library.

#### Max line length

Files to modify:

- `.flake8`
- `pyproject.toml`


### Install the git hook scripts

The first time we work with pre-commit in our project, run:

```bash
pre-commit install
```

## Run

Each time we run the `git commit` command, pre-commit will apply the hook scripts to all files we have added to the commit. If pre-commit modifies any file, the commit won't be applied and we have to add the files again and run the `git commit` command.

### Commit without pre-commit

To create a commit without the pre-commit checks you can run:

```bash
git commit -nm "Commit text"
```

### Run specific hook

For example, to run the hook with id `unittests`:

```bash
pre-commit run unittests --all-files
```

## Strange situations

- I can't test with pre-commit a file called main.py.

## Resources

https://pre-commit.com/

https://pre-commit.com/hooks.html
