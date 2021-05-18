# JFR Test Runner

## Usage

`generate-jfr-files <java-runtime> <class> <output-dir>`

`java-runtime` - the path to a Java interpreter to be used.

`class` - the name of the class to run. It is assumed that `CLASSPATH` has been properly set so that this class is reachable.

`output-dir` the path to the directory where the output will be stored. The script will attempt to create the directory if it does not exist.

## Description

This script is intended to generate recordings for all the different possible parameters for `-XX:StartFlightRecorder`.
Some, such as `disk=false`, do not make sense to run.
The recordings will be saved in the output directory specified, with names that correspond to the `‑XX:StartFlightRecorder` parameter they were started with.
