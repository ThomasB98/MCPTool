# Comprehensive Dev Server

A comprehensive MCP server for development and infrastructure management.

## Features

This server provides a wide range of tools to assist with development and infrastructure management, including:

*   **Database Explorer & ERD Generator:** Connect to various databases, explore schemas, and generate ERD diagrams.
*   **API Documentation Generator:** Scan codebases to generate OpenAPI specifications.
*   **Code Quality Analyzer:** Analyze code for quality, complexity, and security vulnerabilities.
*   **Infrastructure Monitor:** Connect to cloud providers to monitor resources.
*   **Development Environment Manager:** Orchestrate Docker containers and manage development environments.

## Setup

1.  **Install dependencies:**

    ```bash
    pip install -r requirements.txt
    ```

2.  **Run the server:**

    ```bash
    python main.py
    ```

## Usage

The server communicates over stdio and follows the MCP specification. You can interact with it using any MCP-compliant client.

### Example: Connect to a database

```json
{
    "tool": "connect_database",
    "arguments": {
        "connection_string": "postgresql://user:password@host:port/database",
        "db_type": "postgresql"
    }
}
```

### Example: Generate an ERD

```json
{
    "tool": "generate_erd",
    "arguments": {
        "database_name": "my_database",
        "format": "svg"
    }
}
