# Knowledge-Base
Notes on various topics.

## Packages to install

* `ghp-import`
* `jupyter-book`

## Build the docs

```sh
source .venv/bin/activate
```


```sh
jupyter-book build docs/
```

## Force build the docs

```sh
jupyter-book build --all docs/
```
# Push to github

```sh
ghp-import -n -p -f docs/_build/html
```