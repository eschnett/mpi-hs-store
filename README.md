# [mpi-hs-store](https://github.com/eschnett/mpi-hs-store)

[MPI](https://www.mpi-forum.org) bindings for Haskell

* [GitHub](https://github.com/eschnett/mpi-hs-store): Source code repository
* [Hackage](http://hackage.haskell.org/package/mpi-hs-store): Haskell
  package and documentation
* [Stackage](https://www.stackage.org/package/mpi-hs-store): Stackage
  snapshots
* [Azure
  Pipelines](https://dev.azure.com/schnetter/mpi-hs-store/_build):
  Build Status [![Build
  Status](https://dev.azure.com/schnetter/mpi-hs-store/_apis/build/status/eschnett.mpi-hs-store?branchName=master)](https://dev.azure.com/schnetter/mpi-hs-store/_build/latest?definitionId=8&branchName=master)



## Overview

This is a companion package to
[`mpi-hs`](https://github.com/eschnett/mpi-hs). Read the documentation
there.

This package `mpi-hs-store` provides a high-level interface based on
`Data.Store` in the
[`store`](https://hackage.haskell.org/package/store) package. This
is a separate package to reduce dependencies for `mpi-hs`. Note that
`mpi-hs` has a similar high-level interface based on `Data.Storable`
already built in.

### Running the tests

There is one test case provided in `tests`:

```
stack build --test --no-run-tests
mpiexec -n 3 stack exec -- $(stack path --dist-dir)/build/mpi-test-store/mpi-test-store
```
