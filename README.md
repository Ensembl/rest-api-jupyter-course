# rest-api-jupyter-course
Python and R notebooks to be used by Jupyter

# Using Binder

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/Ensembl/rest-api-jupyter-course/master)

You can use Binder to execute our Jupyter notebooks. Click on the above image to launch it.

# Running locally using Docker

## Dependencies

1. Git (should be installed on your system)
2. Docker 
    - [Mac](https://docs.docker.com/docker-for-mac/install/)
    - [Windows](https://docs.docker.com/docker-for-windows/)
    - [Linux](https://docs.docker.com/engine/install/)

## To run

Open your terminal/command window and type the following.

```bash
git clone https://github.com/Ensembl/rest-api-jupyter-course.git
cd rest-api-jupyter-course
docker run -it --rm -p 8888:8888 -v "$PWD":/home/jovyan/work jupyter/r-notebook
```

This will produce output which looks like:

```
Executing the command: jupyter notebook
[I 16:54:34.267 NotebookApp] Writing notebook server cookie secret to /home/jovyan/.local/share/jupyter/runtime/notebook_cookie_secret
[I 16:54:35.394 NotebookApp] JupyterLab extension loaded from /opt/conda/lib/python3.8/site-packages/jupyterlab
[I 16:54:35.396 NotebookApp] JupyterLab application directory is /opt/conda/share/jupyter/lab
[I 16:54:35.405 NotebookApp] Serving notebooks from local directory: /home/jovyan
[I 16:54:35.405 NotebookApp] The Jupyter Notebook is running at:
[I 16:54:35.406 NotebookApp] http://2d01bcf7895c:8888/?token=93244e3e79efe261a2d7600037dfd5d3d5c61c49b52e9328
[I 16:54:35.408 NotebookApp]  or http://127.0.0.1:8888/?token=93244e3e79efe261a2d7600037dfd5d3d5c61c49b52e9328
[I 16:54:35.408 NotebookApp] Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).
[C 16:54:35.415 NotebookApp]

    To access the notebook, open this file in a browser:
        file:///home/jovyan/.local/share/jupyter/runtime/nbserver-7-open.html
    Or copy and paste one of these URLs:
        http://2d01bcf7895c:8888/?token=93244e3e79efe261a2d7600037dfd5d3d5c61c49b52e9328
     or http://127.0.0.1:8888/?token=93244e3e79efe261a2d7600037dfd5d3d5c61c49b52e9328
```

The final line shows a URL formatted as `http://127.0.0.1:8888/?token=NNNNNNNNNNNNNNN` where `NNNNNNNNNNNNNNN` is a unique token to allow you to log into your Jupyter notebook instance. Click on this link or copy/paste it into your web-browser. You will be presented with the default Jupyter file-explorer. Click on `work`, then on `Python3` or `R` to select your course of interest.
