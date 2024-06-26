# enviserv
`enviserv` is a Python project designed to find and check Python virtual environments and dependencies. It is particularly suited for working within Docker container scopes. The main functionality includes identifying paths to virtual environments, retrieving Conda/Venv environments and their dependencies, checking virtual environments, and more.

## Features
- Search for virtual environments based on the operating system.  
- Retrieve and analyze Conda/Venv environments and their dependencies.  
- Check and compare dependencies across different virtual environments.  
- Execute shell commands and manage environment variables.  
- Custom logging functionality.

## Modules

1. **depsgetter.py**
Contains the `DepsGetter` class with the following functionalities:

- `get_venvs_paths`: Search for virtual environment paths.
- `get_conda_envs`: Retrieve Conda environments.
- `get_dependencies_conda`: Get dependencies for a specific Conda environment.
- `check_venv_founded`: Check if a virtual environment is found.
- `get_dependencies`: Retrieve dependencies for a specific virtual environment.
- `get_all_dependencies`: Retrieve dependencies for all specified virtual environments.
- `get_some_dependencies`: Retrieve dependencies for specified virtual environments.
- `run_autoshell_command`: Execute shell commands and return output.
- `get_base_win_paths`: Retrieve base Windows paths for Python installations.
- `get_base_win_deps`: Get dependencies for a given Python virtual environment.
- `check_library_in_current_venv`: Check if a specified library is installed in the current virtual environment.
- `count_specifed_venv_deps_is_in_current_venv`: Count specified dependencies in the current virtual environment.
- `get_current_dependencies`: Retrieve current dependencies in the virtual environment.
- `count_current_deps_is_in_specifed_venv`: Count current dependencies in a specified virtual environment.
- `print_dashes`: Print a series of lines with increasing length.
- `check_current_venv_path`: Check the current virtual environment path and update paths and dependencies if needed.

2. **dictan.py**
Contains the `DictAnalyzer` class with the following functionalities:

- `dict_info`: Generate information about the keys and values of a dictionary.
- `compare_dicts_info`: Compare two dictionaries and identify matching, similar, and unique elements.
- `print_dict_json`: Print a dictionary in JSON format.
- `print_dict`: Print a dictionary with options to control output.

3. **environcheck.py**
Contains the `EnvironCheck` class with the following functionalities:

- `print_environment_variables`: Print environment variables.
- `check_in_container`: Check if the program is running inside a container.
- `get_save_folder_path`: Retrieve the path to save environment variables.
- `save_env_to_file`: Save environment variables to a file.

4. **mylog.py**
Contains the `MyLogger` class with the following functionalities:

- Custom logging setup.
- Log messages with specified levels.
- Enable or disable logging dynamically.
- `find_logging_objects` - finding all logging objects in program scope

5. **venvsfinder.py**
Contains the `VenvsFinder` class with the following functionalities:

- `get_actual_folder_name`: Get the actual name of the final folder in a path.
- `get_actual_path`: Get the actual path of a folder considering case sensitivity.
- `universalize_path`: Convert a path into a format understandable by both Windows and Linux.
- `check_shells`: Check the availability of various shells.
- `search_venvs_path`: Search activation files in a given path using various shells or Python itself.

## Installation
Clone the repository and install the required packages:
```bash
git clone https://github.com/yourusername/depsgetter.git
cd depsgetter
```
No additional dependencies are required as the project uses only the standard Python library. Therefore, no need to install any packages via pip, and there is no requirements file.

## Usage
Import the necessary classes and use their methods as required
```python
from depsgetter import DepsGetter, DictAnalyzer, EnvironCheck, MyLogger, VenvsFinder

# Example usage
deps_getter = DepsGetter()
venvs_paths = deps_getter.get_venvs_paths(envs_path_list_linux=["/path/to/venvs"], verbose=True)
print(venvs_paths)
```

## Contributing
Contributions are welcome! Please submit a pull request or open an issue for any enhancements or bug fixes.

## License
This project is licensed under the MIT License.

## Authors
Grigory Kozhanov - kogriv

Feel free to reach out with any questions or feedback!
