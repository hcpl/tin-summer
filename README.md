# file-sniffer

[![Build Status](https://travis-ci.org/vmchale/file-sniffer.svg?branch=master)](https://travis-ci.org/vmchale/file-sniffer)

If you do a significant amount of programming, you'll probably end up with
build artifacts scattered about. `sniff` is a tool to help you find those
artifacts. It's especially useful when you're writing build systems 
(because you can make sure your `clean` command actually cleans everything).

## Features

  - [x] find "likely build artifact" directories
    - [x] use .gitignore/path to make decision
  - [ ] match speed of gnu utils on traversals
    - [x] faster when finding artifacts
    - [x] faster with excludes
  - [x] colorized output
  - [x] sort results by size

### Languages Tested With

  - [x] Haskell (incl. GHCJS)
  - [x] Rust
  - [x] Julia
  - [x] Python
  - [x] Elm
  - [x] Nim
  - [x] Vimscript

## Installation

### Binary install

The easiest way to install for Linux or Windows is to download a binary from the [releases
page](https://github.com/vmchale/file-sniffer/releases).

### Cargo

If your platform doesn't have binaries, get [cargo](https://rustup.rs/). Then:

```bash
 $ cargo install file-sniffer
```

## Use

Search current directory for directories with build artifacts:

```bash
 $ sniff artifacts
```

Look in `$DIR` for build artifacts and sort by size:

```bash
 $ sniff artifacts $DIR --sort
```

Look for artifacts or directories containing artifacts that occupy more than 1GB of disk space:


```bash
 $ sniff artifacts -t1G
```

### Accessibility

To turn off colorized output:

```bash
export CLICOLOR=0
```
