# CodeExecutor

CodeExecutor is a code execution package that supports multiple programming languages.

## Features

- Support for multiple programming languages
- Safe code execution environment
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
│   ├── compile_config.py    # Compilation configuration
│   └── execute_config.py    # Execution configuration
├── toolchain.py         # Toolchain functionality
├── executor.py          # Code executor
├── directory_manager.py # Directory management functionality
└── solution_wrapper/    # Solution wrapper directory
    ├── cpp/            # C++ solution wrapper
    │   ├── main.cpp    # Main C++ solution implementation
    │   └── nlohmann/   # JSON library for C++
    │       └── json.hpp    # JSON parsing library
    ├── java/           # Java solution wrapper
    │   ├── Main.java   # Main Java solution implementation
    │   └── lib/        # Java dependencies
    │       ├── jackson-annotations-2.18.2.jar    # Jackson annotations
    │       ├── jackson-core-2.18.2.jar          # Jackson core library
    │       └── jackson-databind-2.18.2.jar      # Jackson data binding
    ├── javascript/     # JavaScript solution wrapper
    │   ├── main.js     # Main JavaScript solution implementation
    │   └── solution_adder.js
    └── python/         # Python solution wrapper
        └── main.py     # Python solution implementation
```

## Usage

### Basic Usage

```python
from code_executor import CodeExecutor
from code_executor.directory_manager import CleanupPolicy

# Create code executor instance
executor = CodeExecutor(
    language="python",           # Programming language
    solution_code="def solution()",  # Code to execute
    testcase="test input",      # Test case
    base_dir="/path/to/base",   # Base directory (optional)
    timeout=10,                 # Execution time limit (seconds)
    cleanup_policy=CleanupPolicy.NONE  # Cleanup policy
)

# Execute code
result = executor.run()
```

### Cleanup Policy (CleanupPolicy)

- `CleanupPolicy.NONE`: No cleanup performed
- `CleanupPolicy.HASH_ONLY`: Only hash-based cleanup
- `CleanupPolicy.SAFE_ALL`: Perform all safe cleanups

### Step-by-Step Execution

```python
# Compile only
executor.compile()

# Execute only
executor.execute()

# Compile and execute
result = executor.run()
```

## License

This project is licensed under the MIT License.

## Authors

- CJH
- CYH 
