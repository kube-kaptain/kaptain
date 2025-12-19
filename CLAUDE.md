# Kaptain

Kaptain is designed to be an opinionated Kubernetes deployment toolkit on which to base your
in-house deployment system. Kaptain provides scripts and documentation and packages to make
this easy to do right and put together quickly.


## Project Structure

This repository is a [Branchout/branchout](https://github.com/Branchout/branchout) project.
The repos available are listed in `Branchoutprojects` and can be found on disk in a folder of
the same name as their prefix (before first hyphen). Its two purposes are to organise and
document and make working with all the repos easy and clean AND to put centralised docs in.


## Tech Stack

A simple shell and OCI image based stack - see the [Dependencies](#dependencies) section for more info.


## Development Setup

A unix environment (Linux, MacOS, WSL2, etc) with Git and Docker installed. All other tools (BATS, Shellcheck, yq, coreutils, etc) run inside containers.

### macOS (Homebrew)

Git is included with Xcode Command Line Tools (required for Homebrew). For Docker, install the CLI and one of the following runtimes:

```bash
brew install docker

# Pick ONE runtime:
brew install colima           # Lightweight, recommended
brew install rancher-desktop  # Includes Kubernetes
brew install --cask docker    # Docker Desktop (commercial license may apply)
```

### Linux

#### Debian/Ubuntu (apt)

```bash
sudo apt update
sudo apt install git docker.io
```

#### RHEL/Fedora (yum/dnf)

```bash
sudo dnf install git docker
```

#### Arch

```bash
sudo pacman -S git docker
```


## Build & Run

Build and run behaviour will be per sub project - this project is for humans and LLMs to consume/contribute to.


## Testing

<!-- TODO -->


## Code Style

- Always ensure text files have a trailing newline
- Repos are always named in the style group-name group-name-morename group-name-morename-evenmore etc
- With the exception of README.md and CLAUDE.md, all markdown docs should be NamedLikeThis.md


## Architecture

<!-- TODO -->


## Common Tasks

<!-- TODO -->


## Dependencies

Only common tools such as:

* Bash 3.2 up - shell runtime for branchout
* Branchout - bulk repo management and documentation
* Git - source control operations
* Docker - packaging OCI images, running containers for testing and builds

And inside containers others like:

* Bash 4.X - shell runtime for scripts
* kubectl - all kube API operations
* BATS - testing scripts
* Shellcheck - linting scripts
* yq 4 - manipulating YAML documents
* sed, awk, tail, head, etc etc - GNU versions of common unix utilities

Later, various projects project specialisation repos will exist that support things like:

* Different build tools
* Different cloud providers
* Different manifest storage/handling options
* Different repackaged common projects ready to deploy under this model


## Notes

Be careful in shell scripts to not lose data from executing sub shells and trying to write to vars outside that context.
