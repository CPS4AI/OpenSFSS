# Streaming Function Secret Sharing Implementation

This repository contains our implementation of streaming function secret sharing (SFSS), a new variant of function secret sharing (FSS) that is particularly suitable for secure computation over streaming messages. SFSS facilitates several promising applications in a simple and modular fashion, including conditional transciphering, policy-hiding aggregation, and attribute-hiding aggregation. In this repository, we provide our implementation of SFSS primitives, including streaming distributed point functions and streaming distributed comparison functions with applications, including window-based policy/attribute-hiding aggregation. 

The paper can be found at https://ia.cr/2025/2304. Please refer to the Open Science section in the paper for more details. 

# Requirements

emp-toolkit (https://github.com/emp-toolkit/emp-tool) 

Cmake (version >= 3.12) (https://cmake.org)

GMP (we use version 6.3.0) (https://gmplib.org)


# Build
1. Make the build directory and cd into the directory 
    ```
    mkdir build
    cd build
    ```
2. Build using cmake 
    ```
    cmake ..
    ```
3. Generate the target
    ```
    make 
    ```

# Run 
1. Run basic FSS and SFSS primitive
    ```
    ./bin/sfss_main 
    ```
2. Run related applications with network.

   + Open terminal 1, run `./bin/client_runner_main`
   + Open terminal 2, run `./bin/server_runner_main 0 12345`
   + Open terminal 3, run `./bin/server_runner_main 1 12346`
    
    The result will be shown in the terminals. 







