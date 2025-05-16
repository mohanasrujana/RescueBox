# RescueBox

Please refer to the [CONTRIBUTING](CONTRIBUTING.md) file for more information on how to contribute to this project.

Documentation is available on the [Wiki](https://github.com/UMass-Rescue/RescueBox/wiki)
Please do not add any documentation to the root README.md file. Add it to the [Wiki](https://github.com/UMass-Rescue/RescueBox/wiki) instead.

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

Special thanks to Brian Levine.

# RescueBox

RescueBox is a Python and Node.js-based desktop application designed to manage resources and run plugin-based services with a responsive UI and modular backend.


## 🚀 Features

- Modular plugin system with shared dependencies  
- Backend server with Python 3.12 and Poetry  
- UI built with Node.js and Electron  
- Built-in testing using `pytest`  


## 🧰 Setup Instructions (macOS)

```bash
# 1. Install Python 3.12
brew install python@3.12
# Tell poetry to use this interpreter
poetry env use 3.12  

# 2. Install Poetry
curl -sSL https://install.python-poetry.org | python3 -

# 3. Install ffmpeg 
brew install ffmpeg

# 4. (OPTIONAL) If using an Intel Mac, Torch dropped support after v2.2.2.
# Modify the root-level `pyproject.toml` to the following:

# Replace the first few lines under [tool.poetry.dependencies] with:
# [tool.poetry.dependencies]
# torch = "2.2.2"
# requests = "^2.32.3"
# python = ">=3.11,<3.13"
# pyyaml = "^6.0.2"
# typer = "^0.12.5"
# llvmlite = "^0.44.0"
# pytest = "^8.3.4"
# httpx = "^0.28.1"
# numpy = "1.26.4"

# 5. Install project dependencies
poetry install

# 6. Run tests to verify setup
poetry run pytest src/

# 7. Run the backend server
./run_server

# 8. (Optional) Setup Node and Python tools before installing UI dependencies
# Upgrade Node.js if your version is less than 14
brew install node@20
echo 'export PATH="/usr/local/opt/node@20/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc

# Install setuptools for Python 3.12
brew install python-setuptools
# Or use pip: pip install setuptools

# 9. Install UI dependencies
cd RescueBox-Desktop
npm install

# 10. Run the UI
npm start
