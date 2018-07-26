# [Jupyter](http://jupyter.org/) notebooks for [Dyalog APL](https://www.dyalog.com/)

## What is a Jupyter notebook?

A Jupyter notebook document combines an interactive coding session with narrative text according to [Donald Knuth's *literate programming*](https://en.wikipedia.org/wiki/Literate_programming) paradigm. This format is advantageous for teaching APL, explaining algorithms, and sharing ideas. The consumer of a notebook can modify the code and see the effects of their modification, but can also modify the running text and republish the notebook.

Jupyter notebook documents can be used interactively on the user's local machine after installing Jupyter and [an appropriate language kernel](https://github.com/Dyalog/dyalog-jupyter-kernel) or run in dedicated online environments. Dyalog APL Jupyter notebooks may also be used on [TryAPL](https://tryapl.org/) with no installation necessary (although to protect the server and ensure a consistent experience, restrictions on the code apply). Furthermore, a notebook may be statically viewed by any Jupyter notebook viewer (including zero-footprint online viewers), or exported to multiple formats with wide support, e.g. HTML or PDF.

## Offline usage

1. Follow the [installation instructions for the Dyalog APL Jupyter kernel](https://github.com/Dyalog/dyalog-jupyter-kernel#installation).
1. [Clone](https://help.github.com/articles/cloning-a-repository/) this repository.
1. From a command line, navigate to the directory you cloned this repository to, then run `jupyter-notebook`. This should launch your browser with a directory view. Click on the notebook you want to open.

### APL keyboard and language bar

A zero footprint in-browser language bar, key-bindings, and character compositions is available using [a bookmarklet](https://abrudz.github.io/lb/apl). After installation, launch a Jupiter notebook and then click on the bookmarklet.

## Online usage

These notebooks are available to try through [TryAPL](http://tryapl.org)'s **Learn** tab. Note however that TryAPL only allows a subset of APL to be used.

## Contributing

Feel free to submit pull requests with additional notebooks.
