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

## PyData sphinx theme
I found [PyData's sphinx theme](https://pydata-sphinx-theme.readthedocs.io/en/stable/index.html) to be much more useful for big projects. The structure of the theme is more complicated than the default jupyter book theme. [Here](https://pydata-sphinx-theme.readthedocs.io/en/stable/index.html) is a nice documentation about the layout of the theme.

All we need to do is rearrange the TOC in `_toc.yml`. Each chapter will have its own `index.md` file  as a lander. The sections will be the individual ipynb files. A small problem is I can't add caption to anything else other than Parts, so all the contents in a specific top bar will be continuous. There must be a way to do it, but I am too lazy to find it.

We also need to adjust the `_config.yml`. We need to make a number of changes. You can see my changes. [Here](https://pydata-sphinx-theme.readthedocs.io/en/latest/user_guide/layout.html#references) is a list of all the possible changes and [this](https://github.com/pydata/pydata-sphinx-theme/blob/main/docs/conf.py) is how PyData has implemented it.