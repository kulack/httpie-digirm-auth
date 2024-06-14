## Building

https://packaging.python.org/en/latest/tutorials/packaging-projects/

```bash
pip install --upgrade build twine
python -m build

# PyPi test
python3 -m twine upload --repository testpypi dist/*

# OR

# PyPi main
python3 -m twine upload --repository pypi dist/*
```

## Local Build, Install and Test

### Local

```bash
pip install --upgrade build

python3 -m build

# HTTPie Local testing
httpie plugins install dist/httpie_digirm_auth-*-py3-none-any.whl
```

### Install Via PyPi Test

First update your credentials in `~/.pypirc`:

```bash
# Install PyPi test testing
python -m venv digirm-test.env

. ./digirm-test.env/bin/activate

pip install --index-url https://test.pypi.org/simple/ --no-deps httpie-digirm-auth
```

