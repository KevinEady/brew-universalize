# `brew-universalize`

Create universal binaries of Homebrew-installed shared libraries

## Installation

This tool is a simple Bash script and can be installed to any location and made
executable:

```shell
wget https://raw.githubusercontent.com/KevinEady/brew-universalize/HEAD/brew-universalize && \
chmod +x brew-universalize
```

## Usage

```shell
./brew-universalize formula [...]
```

Downloads the bottle for the other system architecture (eg. `arm64` on
`x86_64`), searches for matching `.dylib` library files between installed and
the downloaded bottles, and updates the installed libraries into universal
binaries using `lipo` for the given formulae.

## TODO

- [ ] Error handling
- [ ] Feedback and testing
