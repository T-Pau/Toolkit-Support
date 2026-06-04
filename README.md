# Toolkit Support

Since Toolkit is meant to be included as a submodule in other projects, everything that is not needed by projects using it is kept out of the main repository. This includes the documentation, and the tests.

## Tests

Tests can be run against the version of Toolkit included in this repository, or against an external version, to allow working on Toolkit as part of another project.

It requires [nihtest](https://nih.at/nihtest) and [Python](https://www.python.org/) to be installed.

To test zip file creation, it needs `zipcmp` from [libzip](https://libzip.org/) to be installed.

To test against the included version:

```sh
mkdir run
cd run
../bin/setup
nihtest --all
```

To test against an external version:
```sh
mkdir run-external
cd run-external
../bin/setup run-external path/to/external/Toolkit
nihtest --all
```
## Documentation

Documentation is built using [zensical](https://zensical.org/).