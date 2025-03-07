# Toy Programmer

An AI-powered Go programming tool that helps you generate Go programs based on text assignments.

## Overview

Toy Programmer is an advanced tool built with Dagger that leverages AI to automatically generate Go programs from text descriptions. It consists of two main modules:

1. **ToyProgrammer**: The main application that takes programming assignments as input and generates Go code.
2. **ToyWorkspace**: A supporting module that provides a containerized environment for code generation and testing.

## Features

- **AI-Powered Code Generation**: Generate Go programs from simple text descriptions
- **Containerized Environments**: Uses Docker containers for isolated development
- **QA Automation**: Optional AI-driven QA testing for generated code
- **Build Verification**: Ensures generated code builds successfully

## Requirements

- Go 1.23.2+
- Dagger (v0.17.0-llm.4+)
- Docker

## Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/toy-programmer.git
cd toy-programmer
```

## Usage

### Basic Code Generation

```go
// Create an instance of ToyProgrammer
programmer := &ToyProgrammer{}

// Generate a Go program based on an assignment
result := programmer.GoProgram("write a simple HTTP server", false)
```

### With QA Testing

```go
// Create an instance of ToyProgrammer
programmer := &ToyProgrammer{}

// Generate a Go program with QA testing
result := programmer.GoProgram("write a simple HTTP server", true)
```

## How It Works

1. The user provides a programming assignment as a text description
2. ToyProgrammer uses an AI model to interpret the assignment
3. The AI generates Go code in a ToyWorkspace container
4. The code is built to ensure it compiles successfully
5. If QA testing is enabled, another AI instance tests and documents the functionality

## Project Structure

- `main.go`: Contains the ToyProgrammer implementation
- `toy-workspace/`: Contains the ToyWorkspace implementation
- `internal/`: Internal packages and generated code

## AI Development Tools

This project includes AI-assisted development tools in the `.ai` folder for improving code quality and consistency. See [.ai/README.md](.ai/README.md) for details.

## License

[Add license information here]

## Contributing

[Add contribution guidelines here] 