![PyPI - Python Version](https://img.shields.io/pypi/pyversions/mkdocs-add-number-plugin)
![PyPI](https://img.shields.io/pypi/v/mkdocs-add-number-plugin)
![PyPI - Downloads](https://img.shields.io/pypi/dm/mkdocs-add-number-plugin)
![GitHub contributors](https://img.shields.io/github/contributors/timvink/mkdocs-add-number-plugin)
![PyPI - License](https://img.shields.io/pypi/l/mkdocs-add-number-plugin)

# mkdocs-render-otherfile-plugin

[MkDocs](https://www.mkdocs.org/) plugin to render other format files in mkdocs build. This only affects your rendered HTML and does not affect the markdown files.

## Setup

Install the plugin using pip3:

```bash
pip3 install mkdocs-render-otherfile-plugin
```

Next, add the following lines to your `mkdocs.yml`:

```yml
plugins:
  - search
  - render-otherfile
```

> If you have no `plugins` entry in your config file yet, you'll likely also want to add the `search` plugin. MkDocs enables it by default if there is no `plugins` entry set.

## Usage

Example of multiple options set in the `mkdocs.yml` file:

```yml
plugins:
    - search
    - render-otherfile
        ext:
            - .c
            - .cpp
            - .py
```

## Options

- `ext`: mkdocs 默认只渲染markdown文件，配置其他的文件后缀以支持渲染成HTML页面

**注意** 当前实现的是渲染源代码文件，简单的把源码文件放入 "\``` \``` "中实现。