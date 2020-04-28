# Python Project Template


This project is a template project for python projects. The idea is to have a starting point for any kind of python project.

---

## Requirements

 - Make
 - Python 3.8+


## Development Environment
 
 
### Automation tool

This project uses `Makefile` as automation tool. Replace `myproject` label to your project name.

### Set-up Virtual Environment

The following commands will install and set-up `pyenv` tool (https://github.com/pyenv/pyenv) used to create/manage virtual environments:

- Just replace `zshrc` with the configuration file of your interpreter, like `bashrc`

```bash
$ git clone https://github.com/pyenv/pyenv.git ~/.pyenv
$ echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zshrc
$ echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc
$ echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n eval "$(pyenv init -)"\nfi' >> ~/.zshrc
$ exec "$SHELL"
$ git clone https://github.com/pyenv/pyenv-virtualenv.git $(pyenv root)/plugins/pyenv-virtualenv
$ echo 'eval "$(pyenv virtualenv-init -)"' >> ~/.zshrc
$ exec "$SHELL"
```

After that, access the project directory and execute `make create-venv` to create and recreate the virtual environment.


### Run tests
- Tests will run with coverage minimum at 90%.

Running code style
```bash
make code-convention
```
Running unit tests
```bash
make test
```
Running code style and all tests
```bash
make
```
