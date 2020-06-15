# Date Group

Group a directory of files.

![CI](https://github.com/RealOrangeOne/date-group-rs/workflows/CI/badge.svg)

Dates are determined through multiple sources:

- EXIF metadata
- Date in filename

## Installation

Downloads can be found under [releases](https://github.com/RealOrangeOne/date-group/releases). Alternatively, use the provided [Docker container](https://hub.docker.com/r/theorangeone/date-group).

### Build yourself

Clone the project, and use `cargo build --release` to create the binary at `target/release/date-group`.

## Usage

The only required argument is the source. The source is 1 or more directory of images you want to group. Grouping will be done relative to this source.

`--verbose` can be used to see the list of files moved, and the ones which were unable to be parsed.

`--dry-run` can be used to perform all the parsing operations, but without moving files.

`--format` will let you specify how files will be grouped. This defaults to `%Y/%B` (eg `2020/May`).

If the destination a file is meant to be moved to already exists, `--delete-redundant-source` can be used to delete the source to ensure things remain clean.
