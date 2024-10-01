# AVAX-PROOF-Avalanche-Custom-Subnet

## Overview

This repository provides the setup and tools for working with the HyperChain environment. It includes functionality for creating and minting assets, as well as running a local Avalanche network to test your applications.

## Getting Started

### Prerequisites

- Go (1.15 or later)
- Git
- An IDE or text editor for code editing (e.g., VSCode, Sublime Text)

### Setup Instructions

1. **Clone the Initial Repository**:
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. **Normalize Dependencies**:
   Inside your project folder, run:
   ```bash
   go mod tidy
   ```

3. **Configure Project Constants**:
   - Open `consts/consts.go` and add any missing parts necessary for your project configuration.

4. **Register Actions**:
   - Go to `registry/registry.go` and register the `Create_Asset` and `Mint_Asset` actions.

### Running Your VM Locally

1. **Set Up Go Path**:
   Ensure Go is in your terminal's PATH. You can do this by running:
   ```bash
   export PATH=$PATH:$(go env GOPATH)/bin
   ```
   If that doesn't work, try:
   ```bash
   export PATH=$PATH:/usr/local/go/bin
   ```

2. **Run the Local Environment**:
   Start the VM by executing:
   ```bash
   MODE="run-single" ./scripts/run.sh
   ```

3. **Build the Project**:
   Compile the project by running:
   ```bash
   ./scripts/build.sh
   ```
   If you encounter a permissions denied error, use:
   ```bash
   bash ./scripts/run.sh
   ```

4. **Import Demo Keys**:
   Load the demo private key included in the project:
   ```bash
   ./build/token-cli key import demo.pk
   ```
   Import the chain using:
   ```bash
   ./build/token-cli chain import-anr
   ```

### Interacting with Your HyperChain

- Follow the demos included in the README file or those located in the repository to test your assets and transactions.

### Closing Your Local Avalanche Network

- To stop your local Avalanche network, run:
  ```bash
  killall avalanche-network-runner
  ```

## Authors

- monolienex

## License

This project is licensed under the MIT License. See the LICENSE file for more details.

---

Feel free to reach out if you have any questions or need further assistance!
