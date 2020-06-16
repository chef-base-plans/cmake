[![Build Status](https://dev.azure.com/chefcorp-partnerengineering/Chef%20Base%20Plans/_apis/build/status/chef-base-plans.cmake?branchName=master)](https://dev.azure.com/chefcorp-partnerengineering/Chef%20Base%20Plans/_build/latest?definitionId=69&branchName=master)

# cmake

CMake is an open-source, cross-platform family of tools designed to build, test and package software.  See [documentation](https://cmake.org)

## Maintainers

* The Core Planners: <chef-core-planners@chef.io>

## Type of Package

Binary package

### Use as Dependency

Binary packages can be set as runtime or build time dependencies. See [Defining your dependencies](https://www.habitat.sh/docs/developing-packages/developing-packages/#sts=Define%20Your%20Dependencies) for more information.

To add core/cmake as a dependency, you can add one of the following to your plan file.

##### Buildtime Dependency

> pkg_build_deps=(core/cmake)

##### Runtime dependency

> pkg_deps=(core/cmake)

### Use as Tool

#### Installation

To install this plan, you should run the following commands to first install, and then link the binaries this plan creates.

``hab pkg install core/cmake --binlink``

will add the following binaries to the PATH:

* /bin/cmake
* /bin/ctest
* /bin/cpack

#### Using an example binary

You can now use the binary as normal.  For example:

``/bin/cmake --help`` or ``cmake --help``

```bash
$ cmake --help
Usage

  cmake [options] <path-to-source>
  cmake [options] <path-to-existing-build>
  cmake [options] -S <path-to-source> -B <path-to-build>
...
...
```
