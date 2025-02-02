# datascipsych
Data Science for Psychology course code

## Getting the source code

To use this project in Visual Studio Code, you must first "clone" it from GitHub. If you are reading this `README` file in Visual Studio Code, you are probably done with this step.

To clone the code project from GitHub, open a new window in Visual Studio Code. In the Welcome tab, you should see an option to `Clone Git Repository...`. Click that, then enter `https://github.com/mortonne/datascipsych.git`. Select a destination folder, such as your desktop. Choose to open the repository either in the current window or in a new window. When asked whether you trust the authors of the files in this folder, select "Yes". After a moment, you should see the code project files in the Explorer.

To get the latest code from GitHub, open the Command Palette and run `Git: Pull`, or click on the refresh icon in the lower right of the VSCode window.

## Installation

To check whether you installed the project correctly, first open a terminal (`View > Terminal`). You should see `(.venv)` on the left side of the command prompt. This means that you have a local virtual environment set up for Python. Next, run `pip list`. If the package is installed, this should display a list of many Python packages. If not, then follow the instructions below to set up the project.

### Using Visual Studio Code commands (recommended)

Go to the Command Palette and run `Python: Create Environment...`, then `Venv`. Select a Python 3.12.8 interpreter.  If you don't see one, install it from the Windows Store (Windows) or python.org (macOS and Linux), then try again. You may have to click the refresh button on the right of the Command Palette to make a newly installed interpreter show up. Wait for VS Code to set up your environment and install the necessary packages.

### Using the terminal

First, go to the Command Palette and run `Python: Select Interpreter...` and select a Python 3.12.8 interpreter. Open a new terminal in VS Code (`View > Terminal`, then click + on the right pane if necessary to open a new terminal). Run `python --version` to check that you are running Python 3.12.8.

To create a virtual environment, run:

```bash
python -m venv .venv
```

You should see a prompt asking you if you want to select the virtual environment for the workspace folder.  Select `Yes`. Open a new terminal window again. You should see `(.venv)` at the start of the line in the terminal.

Finally, install the packages specified in `pyproject.toml` using pip:

```bash
pip install -e .
```

You should now have a Python environment with all the necessary packages installed.

## Running Jupyter Lab

### In Visual Studio Code

Open a Jupyter file (these have a file extension of `.ipynb`) by clicking on it in the Explorer pane.  For example, you can open `assignments/assignment3/python_basics.ipynb`. You should see a button on the upper right that says `Select Kernel`. Click it to select a kernel to run the notebook. Select `Python Environments`, then select the virtual environment you set up previously. You should now see `.venv (Python 3.12.8)` in the upper right of the notebook.

### In a browser

Before you can run notebooks in your browser, you will have to install your Python virtual environment as a Jupyter kernel. Open a terminal in VS Code (`View > Terminal`), then run:

```bash
python -m ipykernel install --user --name datascipsych
```

You should see `Installed kernelspec datascipsych in ...` with a path to where the kernel is installed on your computer.

To run Jupyter Lab, open the terminal and run `jupyter lab`. This should open your default browser with a tab running Jupyter Lab. When you open a notebook, there should be a kernel name in the upper right, showing `datascipsych`. It should use the correct kernel automatically.

If you need to change the kernel, click on the kernel name (this will be No Kernel if no kernel is currently selected) and select the kernel you want to use.
