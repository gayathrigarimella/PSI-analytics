# Private Set Operations from Oblivious Switching [![Build Status](https://travis-ci.org/encryptogroup/OPPRF-PSI.svg?branch=master)](https://travis-ci.org/encryptogroup/OPPRF-PSI)

An implementation of the protocols presented in the paper "Private Set Operations from Oblivious Switching" accepted at PKC'21 (https://eprint.iacr.org/2021/243.pdf). We present a circuit-PSI protocols to compute on the intersection to learn functionalities like cardinality, cardinality-sum, any function 'g' while leaking the intersection. This framework also allows us to learn the plain intersection and union of the sets. Lastly, we show how to compute the Private-ID functionality using our union protocol, making it the first Private-ID instantiated using symmetric-key operations. 


## Required packages:
 - g++ (vection >=8) 
 - libboost-all-dev (version >=1.69) 
 - libgmp-dev 
 - libssl-dev 
 - libntl-dev

## Compilation

To compile as library.

```
mkdir build
cd build
cmake [OPTIONS] -DCMAKE_BUILD_TYPE=[Release|Debug] ..
make
// or make -j 10 for faster compilation
```

Available options are as follows:

- `-DPSI_ANALYTICS_BUILD_TESTS=ON` to compile tests
- `-DPSI_ANALYTICS_BUILD_EXAMPLE=ON` to compile an example with circuit-based threshold checking.

The options can be combined to build both the tests and the example.

## Tests

To run the tests and make sure that everything works as intended, 
you will need to run `cmake` with enabled `PSI_ANALYTICS_BUILD_TESTS`.
Then, run the test binary in `${build_directory}/bin/` without arguments.

## Applications

To run the available example, you will need to enable the `PSI_ANALYTICS_BUILD_EXAMPLE` flag.
Then, run the example binary in`${build_directory}/bin/` either from two terminals locally or 
between two machines.
To find information about the command line arguments, run `${example_name} --help`. 
Suitable parameters and formulas for calculating those can be found in the paper.
