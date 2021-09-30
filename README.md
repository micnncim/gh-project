# `gh project` GitHub CLI extension

[GitHub CLI](https://github.com/cli/cli) extension for listing projects, editing projects interactively.

## Installation

```console
$ gh extension install micnncim/gh-project
```

This extension depends on [fzf](https://github.com/junegunn/fzf) as a fuzzy finder. To install using Homebrew:

```console
$ brew install fzf
```

## Usage

```console
$ # Lists all projects in a current repository.
$ gh project list
$ # Lists all projects in a given organization.
$ gh project list --org=acme-org
# # Links a project in a current repository to issue or PR #123 interactively.
$ gh project add 123
# # Links a project in a given organization to issue or PR #123 interactively.
$ gh project add 123 --org=acme-org
# # Unlinks a project  a current repository to issue or PR #123 interactively.
$ gh project remove 123
# # Unlinks a project in a given organization to issue or PR #123 interactively.
$ gh project remove 123 --org=acme-org

```

## Environment Variables

- `GH_PROJECT_ORGANIZATION` (optional): If this environment variable is set, projects in the organization are listed rather than a current repository even without the flag `--org`.
