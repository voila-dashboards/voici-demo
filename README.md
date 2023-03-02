# Voici demo

<!-- [![lite-badge](https://jupyterlite.rtfd.io/en/latest/_static/badge.svg)](https://jupyterlite.github.io/xeus-python-demo/retro/notebooks/?path=demo.ipynb) -->

[Voici](https://github.com/voila-dashboards/voici) deployed as a static site to GitHub Pages, for demo purposes.

It uses

## ✨ Try it in your browser ✨

TODO

<!-- https://jupyterlite.github.io/xeus-python-demo/retro/notebooks/?path=demo.ipynb -->

## 💡 How to make your own deployment

TODO
<!-- ![Deploy your own](deploy.gif) -->

Then your site will be published under https://{USERNAME}.github.io/{DEMO_REPO_NAME}

## 📦 How to install extra packages

You can pre-install extra packages for xeus-python by adding them to the ``environment.yml`` file.

Only ``no-arch`` packages from ``conda-forge`` and packages from ``emscripten-forge`` can be installed.

For example, if you want to create a Voici deployment with NumPy and Matplotlib pre-installed, you would need to edit the ``environment.yml`` file as following:

```yml
name: voici
channels:
  - https://repo.mamba.pm/emscripten-forge
  - https://repo.mamba.pm/conda-forge
dependencies:
  - numpy
  - matplotlib
```
