# ipyaladin

## Description

A bridge between Jupyter and Aladin Lite, enabling interactive sky visualization in IPython notebooks.

![ipyaladin example](ipyaladin-screenshot.png)

With a couple of lines, you can display Aladin Lite, center it on the target of your choice, and overlay an Astropy table:

![ipyaladin example](ipyaladin-screencast.gif)

## Examples

Some example notebooks can be found in the [examples directory](examples).

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/cds-astro/ipyaladin/master). You can also try it directly [in mybinder](https://mybinder.org/v2/gh/cds-astro/ipyaladin/master), without installing anything.

## Installation

To install use pip:

    $ pip install ipyaladin

Then, make sure to enable widgetsnbextension:

    $ jupyter nbextension enable --py widgetsnbextension

Finally, enable ipyaladin:

    $ jupyter nbextension enable --py --sys-prefix ipyaladin

For a jupyterlab usage:

    $ jupyter labextension develop ipyaladin --overwrite

There is also an experimental conda package that can be installed with:

    $  conda install -c tboch ipyaladin

For a development installation (requires [Node.js](https://nodejs.org) and [Yarn version 1](https://classic.yarnpkg.com/)),

    $ git clone https://github.com/cds-astro/ipyaladin.git
    $ cd ipyaladin
    $ npm install yarn
    $ pip install -e .
    $ jupyter nbextension install --py --symlink --overwrite --sys-prefix ipyaladin
    $ jupyter nbextension enable --py --sys-prefix ipyaladin

When actively developing your extension for JupyterLab, you will need to run this command too:

    $ jupyter labextension develop --overwrite ipyaladin

Then you need to rebuild the JS when you make a code change:

    $ cd js
    $ yarn run build

You then need to refresh the JupyterLab page when your javascript changes.
