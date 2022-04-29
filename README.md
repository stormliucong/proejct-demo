# Proejct Demo for Linux.
1. Create a Git Repository
```sh
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/stormliucong/proejct-demo.git
git push
```
2. Building a Project folder structure
```sh
|-- project-demo
|   |-- data
|   |   |-- example.csv
|   |-- notebooks
|   |   | -- example.ipynb
|   |-- src
|   |   | -- __init__.py
|   |   | -- example.py
|   |-- requirements.txt
|   |-- README.md
```
3. Create a Virtual Environment
```bash
# install pip3 and virtualenv
sudo apt-get install python3-pip -y
# create the virutual environment in the project root
pip3 install virtualenv
virtualenv -p python3 .venv
# Or use python directly.
python3 -m venv .venv # hidden file with prefix .
# activate the virtual environment
source .venv/bin/activate
# install packages you will need
pip3 install -r setup/requirements.txt
```
4. Create a Custom Kernel.
```bash
python3 -m ipykernel install — user — name project_name_env — display-name "my kernel"
```
5. Setup .gitignore
```bash
# Byte-compiled / optimized / DLL files
__pycache__/
*.py[cod]
*$py.class
# C extensions
*.so
# Environments
.venv
```
6. freeze requirements.txt
```sh
pip freeze > requirements.txt
```
7. push to github
```
git add .
git commit -m 'updated'
git push
```