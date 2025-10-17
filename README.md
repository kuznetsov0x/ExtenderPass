# ExtenderPass

A Python script that generates strong, deterministic passwords from simple input strings using cryptographic hashing.

## How It Works

Instead of remembering complex passwords, you only need to remember:
- Your simple base password
- The length requirement

The script combines these with cryptographic hashing to generate a strong, reproducible password.

## Installation

1. **Requirements**: Python 3.6+
2. **No additional dependencies** - uses only Python standard library

## Usage

### Basic Syntax
```bash
python3 extenderpass.py -s "input_string" -l length [options]
```

## Command Line Options

| Option | Description |
|--------|-------------|
| `-s, --string` | Input string |
| `-l, --length` | Output password length |
| `-n, --no-symbols` | Exclude symbols from generated password |
| `-d, --digits-only` | Generate digits only |
| `-a, --letters-only` | Generate letters only |
| `-v, --verbose` | Show generation details |
| `-h, --help` | Show help message |

## Recommended Usage Pattern

1. **Choose a base password** you can remember easily
2. **Add service identifier** to make it unique per service
3. **Specify required length** for the service

## Features

- **Deterministic**: Same input always produces same output
- **Cryptographically secure**: Uses SHA-512 and SHA-256 hashing
- **Customizable**: Control character sets and length
- **Reproducible**: No external dependencies or random factors
- **Verbose mode**: See how your password is generated
