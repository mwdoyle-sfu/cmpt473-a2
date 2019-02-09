# Assignment 2 - SFU CMPT473, SPR 2019

## Overview

Testing the open source [csv2json](https://github.com/mattn/csv2json) program using *input space partitioning*, and *combinatiorial test generation* using ACTS.

## How to run the test harness
	
	./a2

> Or if you have [go](https://golang.org/) installed, you can build from source using `go run main.go`.

## How to run the software under test (SUT)
	
	./csv2json < data.csv 1> data.json 2> data.log

Runs the csv2json executable redirecting stdout to a json file and stderr to a log file

## File Structure

	.
	├── README.md
	├── TestData
	│   ├── ExpectedMessages
	│   │   └── data1.log
	│   ├── ExpectedOutput
	│   │   └── data1.json
	│   └── TestFiles
	│       └── data1.csv
	├── TestOutput
	│   ├── Files
	│   │   └── data1.json              autogenerated
	│   └── Messages
	│       └── data1.log               autogeenrated
	├── a2                              test harness
	├── csv2json                        SUT
	└── main.go                         test harness src

## Personal Notes

- `cmd 1> file.txt` redirect stdout to a file in overwrite mode. The file is created if it doesn't already exist.
- `cmd 2> file.txt` redirect stderr to a file in overwrite mode.
- `cmd 2>&1` redirect stderr to stdout.
- `cmd >> file` append stdout of cmd to file.
- `cmd 2>> file` append stderr of cmd to file.

### what is t-way test?

Given any t parameters (out of all the parameters) of a system, every combination of values of these t parameters is covered in at least one test in the test set.

i.e for a 2-way test (pairwise test), 2 parameters out of all the parameters of a

### Running ACTS3.0

	TSLgenerator spec 
	java -jar acts_3.0.jar specfile

## TODO
