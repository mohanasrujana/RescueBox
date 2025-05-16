# RescueBox

Please refer to the [CONTRIBUTING](CONTRIBUTING.md) file for more information on how to contribute to this project.

Documentation is available on the [Wiki](https://github.com/UMass-Rescue/RescueBox/wiki)
Please do not add any documentation to the root README.md file. Add it to the [Wiki](https://github.com/UMass-Rescue/RescueBox/wiki) instead.

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

Special thanks to Brian Levine.

## 🧰 Setup Instructions (macOS)

1. **Clone the repository**
git clone https://github.com/UMass-Rescue/RescueBox.git
cd RescueBox

1. **Install Python 3.12**  
Run: `brew install python@3.12`  

2. **Tell Poetry to use this interpreter**  
Run: `poetry env use 3.12` (or full path, e.g., `/usr/local/bin/python3.12`)  

3. **Install Poetry**  
Run: `curl -sSL https://install.python-poetry.org | python3 -`  

4. **Install ffmpeg**  
Run: `brew install ffmpeg`  

5. **(OPTIONAL) If using an Intel Mac** — Torch deprecated support after v2.2.2. Modify the root-level `pyproject.toml` file and replace the first few lines under `[tool.poetry.dependencies]` with:  
 
[tool.poetry.dependencies] <br>
torch = "2.2.2" <br>
requests = "^2.32.3"<br>
python = ">=3.11,<3.13"<br>
pyyaml = "^6.0.2"<br>
typer = "^0.12.5"<br>
llvmlite = "^0.44.0"<br>
pytest = "^8.3.4"<br>
httpx = "^0.28.1"<br>
numpy = "1.26.4"<br>


6. **Install project dependencies**  
Run: `poetry install`  

7. **Run tests in the source folder**  
Run: `poetry run pytest src/` 

8. **Run the backend server**  
Run: `./run_server`  

9. **(Optional) Prepare environment before installing UI dependencies**  
Upgrade Node.js if version < 14:  
Run: `brew install node@20`  
Then: `echo 'export PATH="/usr/local/opt/node@20/bin:$PATH"' >> ~/.zshrc`  
Then: `source ~/.zshrc`  

Install setuptools for Python 3.12:  
Run: `brew install python-setuptools`  
Or: `pip install setuptools`  

10. **Install UI dependencies**  
Navigate to the UI folder: `cd RescueBox-Desktop`  
Then run: `npm install`  

11. **Run the UI**  
Run: `npm start`  

## ✅ You're All Set!

Your server and UI should now be up and running. If you run into issues, make sure your Python, Node, and environment paths are correctly configured.






