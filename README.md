# bcolors

ANSI terminal color and style constants for Python, with no runtime dependencies.
Requires Python 3.9 or later and a terminal that supports ANSI escape sequences.

## Install

Once the packaging files are pushed to GitHub, install directly into another
project's virtual environment:

```sh
python -m pip install "bcolors @ git+https://github.com/Mavhawk64/bcolors.git"
```

Or add this line to that project's `requirements.txt`:

```text
bcolors @ git+https://github.com/Mavhawk64/bcolors.git
```

For reproducible installs, append `@<commit-sha>` to the Git URL, replacing
`<commit-sha>` with the full commit hash you want to use.

To install from a local checkout:

```sh
python -m pip install /path/to/bcolors
```

For development, run this from the repository root:

```sh
python -m pip install -e .
```

These instructions install this repository directly; it has not been published
to PyPI.

## Usage

```python
from bcolors import bcolors

print(f"{bcolors.OKGREEN}Success!{bcolors.ENDC}")
print(f"{bcolors.BOLD}{bcolors.RED_FG}Important{bcolors.ENDC}")
print(f"{bcolors.WHITE_FG}{bcolors.BLUE_BG}Highlighted{bcolors.ENDC}")
```

Use `ENDC` to reset colors and styles after the text. The module also includes
standard and bright foreground/background colors, `UNDERLINE`, and convenience
constants such as `HEADER`, `WARNING`, and `FAIL`.

## Build distributions

```sh
python -m pip install build
python -m build
```

The wheel and source distribution are written to `dist/`.
