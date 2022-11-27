<h1 align="center">colStats</h1>

*<p align="center">A CLI tool that executes statistical operations on CSV files.</p>*

## About

Use the `colStats` CLI tool to perform operations like sum or average in specified columns of CSV files.

### Status:

[![Actions Status](https://github.com/rossijonas/colStats/workflows/Test/badge.svg)](https://github.com/rossijonas/colStats/actions)
[![Actions Status](https://github.com/rossijonas/colStats/workflows/Build/badge.svg)](https://github.com/rossijonas/colStats/actions)

### Features:

- Cross-platform:  Linux / macOS / Windows.

- Allow passing multiple CSV files.

- Executes sum and average operations.

## Installation

### Requirements:

- [Go](https://go.dev/) version 1.18.6 (or above)

### How to install:

- Run: 

  ```
  $ go install github.com/rossijonas/colStats@latest
  ```

## Usage

### Options:

```
$ colStats -h
Usage of ./colStats:
  -col int
        CSV column on which to execute operation (default 1)
  -op string
        Operation to be executed (default "sum")
```

### Examples:

#### Calculate the average of the numbers in the 3rd column of the provided CSV file:

```
$ colStats -op avg -col 3 testdata/example.csv
227.6
```

#### Calculate the average of all the numbers in the 3rd column both of the CSV files provided:

```
$ colStats -op avg -col 3 testdata/example.csv testdata/examples2.csv
233.84
```

## Backlog

- Add example Gif to README file.

## Credits

_This is an exercise from the book "Powerful Command-Line Applications in Go", but it may differ from the original exercise._
