# Ansible Mac Provisioning

![ansible-lint](https://github.com/sergief/ansible-mac-provisioning/actions/workflows/ansible-lint.yml/badge.svg)

This repository contains ansible roles to automatically install Software in a mac

## Roles

* `oh-my-zsh`: Configures [oh my zsh](https://ohmyz.sh) for the mac terminal with the plugins and fonts I use. It also installs [iTerm2](https://iterm2.com)
* `java`: Installs [SDK Man](https://sdkman.io) and the Java and Maven versions specified in the playbook file.
* `node`: Installs [NVM](https://github.com/nvm-sh/nvm) and the specified Node version in the playbook file.
* `python`: Installs [PyEnv](https://github.com/pyenv/pyenv) and the selected Python version in the playbook file.
* `vscode`: Installs [Visual Studio Code](https://code.visualstudio.com) and the chosen plugins, specified in the playbook file.
* `hombrew`: Installs the [homebrew](https://brew.sh) packages, the [homebrew cask](https://github.com/Homebrew/homebrew-cask) packages and the [Mac App Store](https://github.com/mas-cli/mas) packages specified in the playbook file.

## Requirements
Before using this tools you must install [homebrew](https://brew.sh) and [ansible](https://www.ansible.com)

Once you have installed `homebrew`, the easiest way to install ansible is via `homebrew`:
```zsh
brew install ansible
```

## How to use it
Review the [Playbook](./playbook.yml) file and make sure it's what you need. You can tweak it adding or removing packages, deactivating roles or changing versions.

Run it:
```zsh
ansible-playbook playbook.yml
```