# 🧩 Toy Programmer

```
████████╗ ██████╗ ██╗   ██╗    ██████╗ ██████╗  ██████╗ ███╗   ███╗██████╗ 
╚══██╔══╝██╔═══██╗╚██╗ ██╔╝    ██╔══██╗██╔══██╗██╔════╝ ████╗ ████║██╔══██╗
   ██║   ██║   ██║ ╚████╔╝     ██████╔╝██████╔╝██║  ███╗██╔████╔██║██████╔╝
   ██║   ██║   ██║  ╚██╔╝      ██╔═══╝ ██╔══██╗██║   ██║██║╚██╔╝██║██╔══██╗
   ██║   ╚██████╔╝   ██║       ██║     ██║  ██║╚██████╔╝██║ ╚═╝ ██║██║  ██║
   ╚═╝    ╚═════╝    ╚═╝       ╚═╝     ╚═╝  ╚═╝ ╚═════╝ ╚═╝     ╚═╝╚═╝  ╚═╝
```

> **A next-generation AI-powered code generation system that transforms natural language into production-ready Go applications**

[![Go Version](https://img.shields.io/badge/Go-1.23.2+-00ADD8?style=flat-square&logo=go)](https://golang.org)
[![Dagger Version](https://img.shields.io/badge/Dagger-v0.17.0--llm.4+-137CBD?style=flat-square&logo=dagger)](https://dagger.io)
[![Docker Required](https://img.shields.io/badge/Docker-Required-2496ED?style=flat-square&logo=docker)](https://www.docker.com)

## 🌟 Overview

Toy Programmer represents a paradigm shift in AI-assisted software development, combining containerized environments with large language models to create a fully autonomous code generation pipeline. Unlike traditional code assistants that merely suggest snippets, Toy Programmer delivers complete, buildable Go applications from natural language descriptions, with built-in verification and testing.

### 🔄 The Toy Programmer Difference

Traditional AI coding assistants operate in isolation from the build environment, leading to code that often fails to compile or execute properly. Toy Programmer solves this fundamental problem through:

1. **Containerized Generation**: Code is created within isolated Docker environments that match production conditions
2. **Build-Verify Loop**: Generated code is automatically compiled to ensure it builds successfully
3. **AI-Powered QA**: Optional autonomous testing and documentation of the generated code's functionality
4. **Institutional Memory**: AI context management preserves knowledge across development sessions

## 🏗️ Architecture

Toy Programmer is built on a modular architecture that separates concerns while maintaining a cohesive workflow:

```
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│                 │     │                 │     │                 │
│  ToyProgrammer  │────▶│  ToyWorkspace   │────▶│  QA Automation  │
│                 │     │                 │     │                 │
└─────────────────┘     └─────────────────┘     └─────────────────┘
        │                       │                       │
        ▼                       ▼                       ▼
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│                 │     │                 │     │                 │
│   LLM Engine    │     │ Docker Container│     │ Documentation   │
│                 │     │                 │     │                 │
└─────────────────┘     └─────────────────┘     └─────────────────┘
```

### Core Components

- **ToyProgrammer**: The main orchestrator that processes assignments and manages the generation workflow
- **ToyWorkspace**: A containerized environment for code generation with built-in build verification
- **Model Context Protocol**: A structured framework for optimizing AI-code interactions
- **AI Development Tools**: A comprehensive suite of tools for maintaining project knowledge and context

## 🚀 Features

### 🤖 AI-Powered Code Generation

- **Natural Language Input**: Describe your desired program in plain English
- **Complete Applications**: Generates entire, working applications, not just code snippets
- **Idiomatic Go Code**: Produces clean, maintainable Go code following best practices
- **Build Verification**: Ensures all generated code compiles successfully

### 📦 Containerized Development

- **Isolated Environments**: Each generation runs in a clean, isolated container
- **Dependency Management**: Automatically handles Go module dependencies
- **Reproducible Results**: Consistent environment ensures reproducible code generation
- **Efficient Caching**: Optimized container caching for faster iterations

### 🧪 Autonomous QA

- **Self-Testing**: Optional AI-driven testing of generated code
- **Functionality Verification**: Ensures the code meets the original requirements
- **Automated Documentation**: Generates comprehensive documentation of findings
- **Command Logging**: Records all commands run and their results

### 🧠 AI Context Management

- **Model Context Protocol (MCP)**: Structured rules for consistent AI-code interactions
- **Codex Knowledge Repository**: Maintains project-specific knowledge and learnings
- **Session Continuity**: Preserves context between development sessions
- **Error Prevention**: Learns from past mistakes to improve future generations

## 📋 Requirements

- **Go 1.23.2+**: Modern Go installation with modules support
- **Dagger v0.17.0-llm.4+**: Dagger with LLM integration capabilities
- **Docker**: Container runtime for isolated environments

## 🛠️ Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/toy-programmer.git
cd toy-programmer

# Build the project
go build ./...
```

## 📝 Usage

### Basic Code Generation

```go
// Create an instance of ToyProgrammer
programmer := &ToyProgrammer{}

// Generate a Go program based on an assignment
result := programmer.GoProgram("write a simple HTTP server that serves static files from a directory", false)
```

### With QA Testing

```go
// Create an instance of ToyProgrammer
programmer := &ToyProgrammer{}

// Generate a Go program with QA testing
result := programmer.GoProgram("create a REST API with CRUD operations for a user management system", true)
```

## 🔍 How It Works

1. **Assignment Processing**: The user provides a programming assignment as a text description
2. **Container Initialization**: A clean ToyWorkspace container is created with the Go development environment
3. **LLM Code Generation**: The AI model interprets the assignment and generates Go code within the container
4. **Build Verification**: The generated code is automatically compiled to ensure it builds successfully
5. **Iterative Refinement**: If build fails, the AI refines the code until it compiles correctly
6. **QA Testing (Optional)**: A separate AI instance tests the functionality and documents findings

## 📂 Project Structure

```
toy-programmer/
├── main.go                 # ToyProgrammer implementation
├── toy-workspace/          # ToyWorkspace implementation
│   └── main.go             # Container environment setup
├── internal/               # Internal packages
│   └── dagger/             # Generated Dagger code
├── .ai/                    # AI development tools
│   ├── codex/              # Knowledge repository
│   ├── blueprints/         # Architecture templates
│   ├── session/            # Session management
│   ├── rules/              # AI behavior patterns
│   └── status/             # Development tracking
└── dagger.json             # Dagger configuration
```

## 🧩 AI Development Tools

The `.ai` folder contains a comprehensive suite of AI-assisted development tools that enhance code quality, maintain project continuity, and accelerate development workflows:

- **Codex System**: Maintains a repository of project-specific knowledge, learnings, and error prevention
- **MCP Framework**: Model Context Protocol rules optimize AI interactions with Go, Dagger, and Docker
- **Blueprints**: Ready-to-implement architecture guides for technical implementations
- **Session Management**: Maintains context between development sessions with status tracking
- **Code Snippets**: Reusable templates for consistent code generation
- **Custom Rules**: Defines AI behavior patterns for specialized development tasks

These tools create an AI-augmented development environment that ensures consistency, reduces repetitive tasks, and preserves institutional knowledge throughout the project lifecycle.

## 🔮 Future Directions

Toy Programmer is continuously evolving with several exciting directions planned:

- **Multi-Language Support**: Extending beyond Go to support additional programming languages
- **Learning from Success**: Analyzing successful code generation patterns to improve future attempts
- **Multi-Agent Collaboration**: Enabling specialized AI models to collaborate on different aspects of code generation
- **IDE Integration**: Seamless integration with popular development environments
- **Automated Refactoring**: AI-driven code refactoring with guaranteed functionality

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Contributing

Contributions to Toy Programmer are welcome! Here's how you can contribute:

1. **Fork the repository** and create your feature branch
2. **Make your changes**, ensuring they follow the project's coding standards
3. **Add tests** for any new functionality
4. **Ensure all tests pass** by running the test suite
5. **Submit a pull request** with a clear description of your changes

Please read our [Code of Conduct](CODE_OF_CONDUCT.md) before contributing.

🙏 Acknowledgements
Special thanks to:
Solomon Hykes for creating the original toy-programmer
The udecode team for developing the original dotai (.ai) framework
These foundational contributions made this project possible.


