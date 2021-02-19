# Mac Tips

Miscellaneous tips and tricks for macOS to ease the migration from Linux / Windows.

## Terminal

Mac comes with a basic terminal application called `Terminal`. But there are other terminal apps with more functionality.
[Iterm2](https://iterm2.com/) is a widely used alternative. 

### Package manager

**Homebrew** is *the* package manager for macOS. With it you can install pretty much every application you are ever going to need.

Install it from [here](https://brew.sh/) and fire a terminal.

Search packages with `brew search packagename`

> `brew search slack`

>```
>==> Formulae
 >slackcat      slacknimate
> ==> Casks
>slack      slack-beta

Install package with `brew install packagename` if the package is a formula (an open source package) or with `brew install --cask packagename` if it's cask (a non-open source package).

>```brew install --cask packagename```

## Languages

### Python

**Note:** Installing Python directly with Homebrew is not advised. Recommended way for installing Python is installing `pyenv` with Homebrew and using it to install Python.

#### pyenv - A python version manager
Pyenv is widely used version manager for Python on Mac - [website](https://github.com/pyenv/pyenv)

###### Install
```
brew update
brew install pyenv
```

###### Usage
Help
```
pyenv --help
pyenv install --help
```

Install a python version
```
pyenv install [python-version]
```

Use newly installed python version
```
cd <your-project-directory>
pyenv local <python-version>
```
Note: These commands will actually set the `python-version` to enable automatically whenever you `cd` into 
`<your-project-directory>`. So from now on you can forget about having to manually enable the Python version 
in this project directory going forward!

##### pyenv-virtualenv - A python virtual environment manager
```
brew update
brew install pyenv-virtualenv
```

Create a virtualenv called `<virtualenv-name>` which is based on `python-version`
```
pyenv virtualenv [python-version] <virtualenv-name>
```
Use newly installed virtualenv
```
cd <your-project-directory>
pyenv local <virtualenv-name>
```
Note: These commands will actually set the virtualenv called `<virtualenv-name>` to automatically be sourced whenever 
you `cd` into `<your-project-directory>`. So from now on you can forget about having to manually enable the Python 
virtualenv in this project directory going forward!
