# Dotfiles

This repository contains my personal dotfiles. They are managed by [chezmoi](https://www.chezmoi.io/).

## Installation

1. Install `chezmoi` on your machine. You can find the installation instructions on the [official website](https://www.chezmoi.io/docs/install/).
2. Set the environment variable `GITHUB_USERNAME` to your GitHub username. This is used to fetch the dotfiles from the correct repository. You can do this by adding the following line to your shell configuration file (e.g. `~/.bashrc` or `~/.zshrc`):

```bash
export GITHUB_USERNAME="your-username"
```

3. Run the following command to apply the dotfiles to your system:

```bash
sh -c "$(curl -fsLS get.chezmoi.io)" -- init --apply $GITHUB_USERNAME
```

## Useful commands

- `chezmoi diff`: Show the differences between the dotfiles in the repository and the ones on your system.
- `chezmoi update`: Update the dotfiles on your system to the latest version from the repository.
- `chezmoi add <file>`: Add a file to the repository.
- `chezmoi cd`: Change the working directory to the root of the dotfiles repository.
