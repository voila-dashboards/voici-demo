# Voici demo

[![lite-badge](https://jupyterlite.rtfd.io/en/latest/_static/badge.svg)](https://voila-dashboards.github.io/voici-demo)

[Voici](https://github.com/voila-dashboards/voici) deployed as a static site to GitHub Pages, for demo purposes.

It uses [jupyterlite-xeus-python](https://github.com/jupyterlite/xeus-python-kernel) as a default kernel with a pre-built Emscripten environment.

## ✨ Try it in your browser ✨

https://voila-dashboards.github.io/voici-demo

## 💡 How to make your own deployment

https://user-images.githubusercontent.com/21197331/223079815-0ea78df4-5173-4adc-a2e4-e10b9593a9f4.webm

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
