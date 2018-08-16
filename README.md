# [Jupyter](http://jupyter.org/) notebooks for [Dyalog APL](https://www.dyalog.com/)

A kernel for using these notebooks is available [here](https://github.com/Dyalog/dyalog-jupyter-kernel).

## What is a Jupyter notebook?

A Jupyter notebook document combines an interactive coding session with narrative text according to [Donald Knuth's *literate programming*](https://en.wikipedia.org/wiki/Literate_programming) paradigm. This format is advantageous for teaching APL, explaining algorithms, and sharing ideas. The consumer of a notebook can modify the code and see the effects of their modification, but can also modify the running text and republish the notebook.

Jupyter notebook documents can be used in the following ways:
1. Offline, on the user's local machine: This requires installing Jupyter (a Python program, so installation of Python is required as well) and [an appropriate language kernel](https://github.com/Dyalog/dyalog-jupyter-kernel). This is the only interactive way to create notebook documents.
1. Online, in a dedicated sandboxed environment. Dyalog APL Jupyter notebooks can for example be used on [TryAPL](https://tryapl.org/) with no installation necessary. Note however, that to protect the server and ensure a consistent experience, restrictions on the code apply.
1. Statically, in that a notebook can be viewed by most any general Jupyter notebook viewer (including online viewers which do not require installation).
1. Exported to any of a number of widely supported formats, for example HTML or PDF, which may then be used accordingly.

## Offline usage

1. Follow the [installation instructions for the Dyalog APL Jupyter kernel](https://github.com/Dyalog/dyalog-jupyter-kernel#installation).
1. [Download this repository](https://github.com/Dyalog/dyalog-jupyter-notebooks/archive/master.zip) and extract it to your Documents folder (on Windows) or home directory (on Linux and macOS) or a subdirectory thereof.
1. Start Jupyter Noteboook:  
Windows: Launch *Jupyter Notebook* from your start menu  
Linux and macOS: From a command line, navigate to your home directory, then run `jupyter-notebook`.
1. This should open a directory view in your browser. Navigate to and click on the notebook document you want to open or click the *New▾* button and to create a new empty one.

### Entering APL characters

You can get an APL language bar and enable key-bindings and character compositions using just a [a bookmarklet](https://abrudz.github.io/lb/apl) (a browser bookmark that contains commands which add new features to the browser). After adding the bookmarklet to your language bar, and opening a Jupyter notebook document in your browser, click on the bookmarklet. You can now insert APL characters in three ways:

1. Click a symbol on the language bar.
1. Type *Backtick* (`` ` ``) and then the associated symbol (hover over symbols on the language bar to see associations), e.g. *Backtick*+*r* makes `⍴` and *Backtick*+*Shift*+*e* makes `⍷`.
1. Type two symbols which roughly make up the APL symbol, then press the *Tab* key to combine them. The two symbols are chosen to be easy to guess according to one of the following systems:
    1. The symbols roughly make up the APL symbol when overlaid. For example, `O-` *Tab* makes `⊖` and `A|`*Tab*  makes `⍋`.
    1. The symbols roughly make up the APL symbol when juxtaposed. For example, `<>` *Tab* makes `⋄` and `[]` *Tab* makes `⎕`
    1. The symbols are identical, and are visually similar to the APL symbol. For example, `ee` makes `∊` and `xx` makes `×`.

### Creating content
Click on any code to begin editing it, then press *Ctrl*+*Enter* to execute the code.

Use the `➕︎` button to insert a new cell, then select cell type (*Code* or *Markdown*) from the dropdown. Additional commands can be found by clicking the `⌨︎` button.

### Defining functions

Single-line dfns and tacit functions may be defined among other code in a code cell:

```
AddNext←{⍵,+/¯2↑⍵}
Fibonacci←AddNext/⌽∘⍳
Fibonacci 10
```

Tradfns may be defined in a cell by beginning the first line with a `∇` and having a sole `∇` after the last line:

```
∇Greet name
 ⎕←'Hello, ',name
∇
```

To define a multi-line dfn, begin a Code cell with the line `]dinput`. For example:

```
]dinput
root←{
    ⍺←2
    ⍵*÷⍺
}
```

### Rich content

You can indicate that the result of a statement should be rendered as HTML by using the `]html` user command:

```
p←'<p>Please:</p>'
b←'<button onclick="alert(''Thank you!'')">Click</button>'
]html p,b
```

You can plot data with with the `]plot` user command:
```
x←(⍳100)÷20
y←(⊢*÷)x
]plot y x
```

Choose chart type with the `-type=` modifier:

```
]plot 3 1 4 1 6 -type=pie
```

## Online usage<sup>Coming soon!</sup>

1. Click on [TryAPL](https://tryapl.org/)'s **Learn** tab.

1. Select tutorial (or enter the URL of an online Jupyter notebook document.<sup>Coming soon!</sup>)

1. Click *Next* to proceed through the tutorial steps.

1. At any time, you may click on APL expressions in the tutorial pane to re-insert them in the session pane, or press the up arrow key to recall previous statements.

### Entering APL characters

You can get an APL language bar and enable key-bindings and character compositions using just a [a bookmarklet](https://abrudz.github.io/lb/apl) (a browser bookmark that contains commands which add new features to the browser). After adding the bookmarklet to your language bar, and opening a Jupyter notebook document in your browser, click on the bookmarklet. You can insert APL characters in three ways:

1. Click on *APL Keyboard*. Click on an APL symbol, or on *Shift*, then an APL symbol. 
1. Click on the *Primer* tab. Click on an APL symbol.
1. Type *Backtick* (`` ` ``) and then the associated symbol (hover over symbols on *Primer* tab bar to see associations), e.g. *Backtick*+*r* makes `⍴` and *Backtick*+*Shift*+*e* makes `⍷`.

## Static usage

Go to [nbviewer.jupyter.org](https://nbviewer.jupyter.org/) and enter the address of any Jupyter notebook to render it right in your browser. No installation of anything is required. Please note that when viewed like this, the content of the notebook may not be modified, so no experimentation is allowed.

## Export to other formats

1. Follow the [instructions for offline usage](#offline-usage).
1. Open the *File* menu, click on *Download as* and select format. Note that some target formats may require installation of third party tools.

## Contributing

Feel free to contribute additional notebooks to our collection through emailing notebooks@dyalog.com or submitting [pull requests](https://help.github.com/articles/about-pull-requests/).
