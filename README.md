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

You can pre-install extra packages by adding them to the ``environment.yml`` file.

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

Only ``no-arch`` packages from ``conda-forge`` and ``emscripten-forge`` can be installed.
- **How do I know if a package is ``no-arch`` on ``conda-forge``?** ``no-arch`` means that the package is OS-independent, usually pure-python packages are ``no-arch``. To check if your package is ``no-arch`` on ``conda-forge``, check if the "Platform" entry is "no-arch" in the https://beta.mamba.pm/channels/conda-forge?tab=packages page. If your package is not ``no-arch`` but is a pure Python package, then you should probably update the feedstock to turn your package into a ``no-arch`` one.
![](https://raw.githubusercontent.com/jupyterlite/xeus-python-demo/main/noarch.png)
- **How do I know if my package is on ``emscripten-forge``?** You can see the list of packages pubished on ``emscripten-forge`` [here](https://beta.mamba.pm/channels/emscripten-forge?tab=packages). In case your package is missing, or it's not up-to-date, feel free to open an issue or a PR on https://github.com/emscripten-forge/recipes.
