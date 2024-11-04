# Introduction

## Setup

**Supported Python Versions**: 3.10, 3.11, 3.12

**Supported Operating Systems**: macOS, Linux

Clone the repository on your machine:

```bash
git clone https://github.com/lotzma/L2Gv2.git
```

Setup the virtual environment

1. Create and activate a virtual environment:
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   ```
2. Install the dependencies:
   ```bash
   pip install -r requirements.txt
   ```

The unified `requirements.in` file includes both shared and platform-specific dependencies with version constraints where necessary. To update dependencies, modify `requirements.in` and then recompile `requirements.txt`:

```bash
pip-compile requirements.in --verbose
```

## Generate documentation

The project is setup to generate documentation with [Sphinx]([https://www.sphinx-doc.org/en/master/index.html](https://www.sphinx-doc.org/en/master/index.html)).

Generate html or markdown documentation

```bash
sphinx-build -M html docs/source/ docs/build/
sphinx-build -M markdown docs/source/ docs/build/
```

Automatically update the html documentation and serve it at [[http://127.0.0.1:8000](http://127.0.0.1:8000](http://127.0.0.1:8000](http://127.0.0.1:8000)) on file update:

```bash
sphinx-autobuild docs/source docs/build/html
```