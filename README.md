# CodeExecutor

CodeExecutor is a code execution package that supports multiple programming languages.

## Features

- Support for multiple programming languages
- Secure code execution environment
- Directory management functionality
- Code execution management through solution wrapper

## Installation

```bash
pip install CodeExecutor
```

## Requirements

- Python 3.6 or higher

## Project Structure

```
code_executor/
├── __init__.py          # Package initialization file
├── configs/             # Configuration directory
├── toolchain.py         # Toolchain functionality
├── executor.py          # Code executor
├── directory_manager.py # Directory management functionality
└── solution_wrapper/    # Solution wrapper directory
```

## Usage

```python
from code_executor import CodeExecutor

# Create code executor instance
executor = CodeExecutor()

# Execute code
result = executor.execute(code, language)
```

## License

This project is licensed under the MIT License.

## Authors

- CJH
- CYH 
