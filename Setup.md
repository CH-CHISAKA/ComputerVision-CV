
# Python virtual environment (.venv): 
Here’s how to create one:

## 1. Make sure Python is installed

Open the **Terminal** on **VS Code** and run the following commands
Check with:
```bash
python --version
```
or 

```bash 
python3 --version
```

## 2. Create a virtual environment

Navigate to your project folder and run:

```bash
python -m venv .venv
```
or 

```bash
python3 -m venv .venv
```
This creates a folder named `.venv` in your project.

## 3. Activate the virtual environment
Run the command on the terminal based on your operating system
### On macOS/Linux:
```bash 
source .venv/bin/activate
```

### On Windows (Command Prompt):
```bash
.venv\Scripts\activate
```
Once activated, your terminal should show (.venv) at the beginning.

## 4. Deactivate when done
Run in the terminal: 
```bash
deactivate
```


# Create requirements.txt

## 1. Create requirements.txt

In your project folder, create a file named:
```text 
requirements.txt
```

You can do it manually or via terminal:

```bash 
touch requirements.txt
```

## 2. Add dependencies

Inside requirements.txt, list the packages you need, one per line:

*Recommended*

Example

```text
requests
flask
numpy
```

You can also pin exact versions (recommended for consistency):
``` text
requests==2.31.0
flask==3.0.0
numpy==1.26.4
```
*Note: The exact version can also result in incompatibility errors/issues with python/python3 version you have*

## 3. Install from requirements.txt
After activating your .venv, run *this if your virtual environment is deactivated*

Run the command on the terminal based on your operating system
### On macOS/Linux:
```bash 
source .venv/bin/activate
```

### On Windows (Command Prompt):
```bash
.venv\Scripts\activate
```
Once activated, your terminal should show (.venv) at the beginning.

Then Run 

```bash
pip install -r requirements.txt
```
This installs everything listed in the file into your virtual environment.

## 4. Generate requirements.txt automatically

If you’ve already installed packages and want to save them:

```bash
pip freeze > requirements.txt
```

# TL;DR
A clean setup usually looks like this:
```bash
python -m venv .venv
source .venv/bin/activate   # or Windows equivalent
pip install <your-packages>
pip freeze > requirements.txt
```











