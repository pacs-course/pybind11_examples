# Examples of pybind11 #

Modified version of the code in [this github repo](git@github.com:tdegeus/pybind11_examples.git) to be consistent with the
conventions used in the Examples.

You need either to have pybind11 set through the module environment

```
 module add pybind11
```

Or, have installed the pybind11 clone in the `Extra` section:

``` bash
 cd Extra
 git submodule update pybind11 # if not already got the submodule
 cd pybind11
 ./install_PACS.sh
 cd ../..
 export mkPybind11Prefix=${PWD}/Examples/share/cmake/
 
```
The last line is needed for the examples that uses cmake.
