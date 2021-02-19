# Mac Tips

Miscellaneous tips and tricks for macOS to ease the migration from Linux / Windows.

## Terminal

### Package manager

**Homebrew** is this *the* package manager for macOS. With it you can install pretty much every application you are ever going to need.

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

**Note:** Installing Python with Homebrew is not advised. Recommended way for installing Python is installing `pyenv` with Homebrew and using it to install Python.

TODO: Section about `pyenv`
