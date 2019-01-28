# Data Science Framework

Jupyter setup to run some data science on the data available in the cluster, like monitoring data or log data.
- [ ] Describe the content in more details ( python libraries included, Jupyter extensions included, ... )
- [ ] Provide Quickstart example

## Setup

### Docker

- Image based on Debian ( https://hub.docker.com/r/conda/miniconda3 )
- Used: Alternative ( more new )
  - https://hub.docker.com/r/continuumio/miniconda3

#### Note on Alpine

- Currently ( 2019-01-26 ) no Alpine support available

"""
This “glibc workaround” is a very ugly hack that may lead to unexpected behaviour and errors. It’s not and never will be supported by Alpine developers, we strongly discourage from using it.
"""
- https://stackoverflow.com/questions/47177538/installing-miniconda-on-alpine-linux-fails
- https://github.com/frol/docker-alpine-miniconda3/blob/master/Dockerfile
- https://github.com/datarevenue-berlin/alpine-miniconda

### TODOs

- [x] Docker Container setup
- [x] Nomad job file
- [x] Find a way to get rid of the token - https://jupyter-notebook.readthedocs.io/en/stable/config.html#options
- [x] Persistency to a certain extend - ephemeral disk - https://www.nomadproject.io/docs/job-specification/ephemeral_disk.html
- [x] Notebook import - git repository: https://stackoverflow.com/questions/52741983/import-a-github-into-jupyter-notebook-directly - Execute `Import Git Repositories.ipynb`
- [x] URL Prefix: https://jupyter-notebook.readthedocs.io/en/stable/public_server.html#running-the-notebook-with-a-customized-url-prefix
  - [ ] Verify Fabio support
- [ ] Check if all python libraries required by the Jupyter Notebook extensions are provided.
- [ ] Verify nomad agent volume directory support - which directory should be used on the agents? Maybe `/mnt/data/`
- [ ] Increase flexibility of the Docker Container description using environment variables.
- [ ] Improve conda setup: https://medium.com/@chadlagore/conda-environments-with-docker-82cdc9d25754


## Usage

- [ ] Provide usage examples
- https://towardsdatascience.com/advanced-jupyter-notebooks-a-tutorial-3569d8153057

### Access JupyterLab

- "http://<url>:<port>/dfs/lab"
- https://jupyterlab.readthedocs.io/en/stable/getting_started/starting.html

- Extensions: https://github.com/topics/jupyterlab-extension, https://www.npmjs.com/search?q=keywords:jupyterlab-extension

- http://bokeh.pydata.org/en/latest/docs/user_guide/quickstart.html#userguide-quickstart
  - https://github.com/bokeh/bokeh-notebooks/tree/master/tutorial

### Creating Notebooks

#### Units

- [ ] Provide example with using `pint`

#### Widgets

- [ ] Provide examples on how to use notebooks
- https://towardsdatascience.com/the-next-level-of-data-visualization-in-python-dd6e99039d5e

- General: https://ipywidgets.readthedocs.io/en/stable/
- Maps: https://github.com/jupyter-widgets/ipyleaflet
- 2D: https://github.com/bloomberg/bqplot
- 3D: https://github.com/maartenbreddels/ipyvolume
- https://github.com/jupyter-widgets/pythreejs

### Import of Notebooks

- [ ] Provide description how to use the git clone example
  - https://github.com/jupyter/notebook/blob/master/docs/source/examples/Notebook/Importing%20Notebooks.ipynb

### Export of Notebooks

- [ ] Describe how to export notebooks to be examined without Jupyter Notebook running

- https://help.github.com/articles/working-with-jupyter-notebook-files-on-github/

## References

- https://jupyter.org
- https://docs.conda.io/en/latest/miniconda.html

### Further Ideas

- https://github.com/mwouts/jupytext