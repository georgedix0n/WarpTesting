# CUDA Warp Details Program

This CUDA program demonstrates how thread and block details can be printed for a basic GPU computation, focusing on warp-level information in a grid of threads.

## Overview

The program launches a simple CUDA kernel, `print_details_of_warps`, which calculates and prints various thread and block attributes, including:
- **Thread ID (`tid`)**
- **Block ID (in x and y dimensions)**
- **Global ID (`gid`)**
- **Warp ID (`warp_id`)** (threads grouped in units of 32)
- **Global Block ID (`gbid`)**

These values help visualize the organization of threads within blocks and warps in a 2D grid.

## Execution Details

- **Grid Size**: 2x2 (4 blocks in total)
- **Block Size**: 42 threads per block

After launching the kernel, the program synchronizes and resets the CUDA device.
