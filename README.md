# Pyparse

## About

A static Python code parser that generates static analysis information for the
Kieker [SAR (Static Architecture
Recovery)](https://github.com/kieker-monitoring/kieker/tree/main/tools/sar)
tool. The combination of Kieker fxca (FXTran Code Analysis) tool and the
[fxtran](https://github.com/pmarguinaud/fxtran) tool are a complementary
counterpart of Pyparse for the Fortran language. The tool is actively
maintained by developers from the Kieker developers group and communities.

## Author
Daphné Larrivain <daphne.larrivain@ecole.ensicaen.fr>

## Outputs

It uses Python's built-in `ast` module to get the abstract syntax tree (AST) of
the target program, and produces static information required by SAR.  Pyparse
generates the following files on function calls and data flow. See
[CsvExporter.py](https://github.com/kieker-monitoring/pyparse/blob/main/src/pyparse/CsvExporter.py)
for more details.

```
operation_definitions.csv
calltable.csv
common-blocks.csv
dataflow-cc.csv
dataflow-cb.csv
notfound_calls.csv
notfound_dataflow.csv
```

## Misc.

Use `--help` to get more information.
