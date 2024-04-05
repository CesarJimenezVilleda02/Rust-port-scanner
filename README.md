# Port Sniffer README

## Overview

This Rust program is a simple, asynchronous port sniffer that allows users to scan a specified IP address for open ports. It uses the Tokio runtime for asynchronous operations and a command-line interface for input parameters. This tool can be beneficial for network administrators, security professionals, and anyone interested in network programming or security.

## Features

- **Asynchronous Scanning**: Utilizes Tokio for efficient, non-blocking IO operations.
- **Flexible Port Range**: Users can specify a custom range of ports to scan.
- **Command-Line Interface**: Easy to use CLI for specifying target IP address and port range.
- **Concurrency**: Spawns multiple tasks in parallel for faster scanning.

## Requirements

- Rust Programming Language
- Cargo (Rust's package manager and build system)
- Tokio Runtime

## Installation

Ensure Rust, Cargo, and Tokio are installed on your system. You can follow the instructions on the [official Rust website](https://www.rust-lang.org/learn/get-started) for Rust and Cargo, and check Tokio's [getting started guide](https://tokio.rs/tokio/tutorial/setup) for Tokio.

To set up the program:

1. Clone the repository or download the source code.
2. Navigate to the project directory in your terminal.

## Usage

Run the program using Cargo with the following command format:

```
cargo run -- [OPTIONS]
```
Options:
-a or --address <Address>: Specify the target IP address to scan. Defaults to 127.0.0.1 if not provided.
-s or --start <start_port>: Define the starting port number for the scan. Must be greater than 0.
-e or --end <end_port>: Define the ending port number for the scan. Must be less than or equal to 65535. Defaults to 65535 if not provided.

Example:
```
cargo run -- -a 192.168.1.1 -s 1 -e 10000
```
This command will scan the IP address 192.168.1.1 for open ports in the range 1 to 10000.
