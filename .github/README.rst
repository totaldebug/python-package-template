.. raw:: html

   <h1 align="center">


.. raw:: html

   </h1>

   <h1 align="center">

Cookiecutter Python Package Template

|Dependencies Status|

|black| |Security: bandit| |Pre-commit| |Semantic Versions| |License|

    .. |Dependencies Status| image:: https://img.shields.io/badge/dependencies-up%20to%20date-brightgreen.svg?style=flat-square&logoColor=white
       :target: https://github.com/totaldebug/python-package-template/pulls?utf8=%E2%9C%93&q=is%3Apr%20author%3Aapp%2Fdependabot

    .. |black| image:: https://img.shields.io/badge/code%20style-black-000000.svg?style=flat-square&logoColor=white)](https://github.com/psf/black
       :target: ttps://github.com/psf/black

    .. |Security: bandit| image:: https://img.shields.io/badge/security-bandit-green.svg?style=flat-square&logoColor=white
       :target: https://github.com/PyCQA/bandit

    .. |Pre-commit| image:: https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&style=flat-square&logoColor=white
       :target: https://github.com/totaldebug/python-package-template/blob/master/.pre-commit-config.yaml

    .. |Semantic Versions| image:: https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--versions-e10079.svg?style=flat-square
       :target: https://github.com/totaldebug/python-package-template/releases

    .. |License| image:: https://img.shields.io/github/license/totaldebug/python-package-template?style=flat-square&logoColor=white
       :target: https://github.com/totaldebug/python-package-template/blob/master/LICENSE

.. raw:: html

   </h1>
   <p align="center">

`About`_ • `Usage`_ • `Releases`_ • `Support`_ • `Donate`_

.. raw:: html

   </p>

--------------

*****
About
*****

.. raw:: html

   <table>
   <tr>
   <td>

`Cookiecutter` is a Python package to generate templated projects.
This repository is a template for `cookiecutter` to generate a Python project which
contains following:

-   A directory structure for your project
-   Poetry package manager
-   Prebuilt `pyproject.toml` file to help you develop and install your package
-   Continuous integration
    -   Preconfigured to generate project documentation
    -   Preconfigured to automatically run tests every time you push to GitHub
    -   Preconfigured to help you release your package publicly (PyPI)

.. raw:: html

   </td>
   </tr>
   </table>

*****
Usage
*****

To use this template use the following commands and then follow the prompts from the
terminal.

1. ``pip install cookiecutter``
2. ``cookiecutter gh:totaldebug/python-package-template``

Then:

- Create a repo and put it there.
- Add a ``secret`` to github for PyPi Token with name ``pypi_password``
- Install the dev requirements ``make install``
- Release your package by pushing a new tag to master.

********
Releases
********

You can see the list of available releases on the `GitHub Releases <https://github.com/totaldebug/python-package-template/releases>`_ page.

We follow `Semantic Versions <https://semver.org/>`_ specification.

We use `action gh-release <https://github.com/marketplace/actions/gh-release>`_. As new version tags are created, release will be generated listing the changes.
You can categorize pull requests in release notes using labels.

List of labels and corresponding titles
=======================================

+----------------------------------------+--------------------------+
|               **Label**               |  **Title in Releases**  |
+========================================+==========================+
| :-----------------------------------: | :---------------------: |
|       ``type/feature``        |       🚀 Exciting New Features       |
+----------------------------------------+--------------------------+
| ``type/bug``, ``type/patch``  | 🐛 Patches & Bug Fixes  |
+----------------------------------------+--------------------------+
|       ``type/ci``        | 📦 Build System & CI/CD |
+----------------------------------------+--------------------------+
|      ``flag/breaking changes``      |   💥 Breaking Changes   |
+----------------------------------------+--------------------------+
|            ``type/docs``            |    📚 Documentation     |
+----------------------------------------+--------------------------+
|            ``type/language``            |    📔 Language     |
+----------------------------------------+--------------------------+
|            ``type/dependencies``       | ⬆️ Dependencies updates |
+----------------------------------------+--------------------------+

You can update it in `release.yml <https://github.com/totaldebug/python-package-template/blob/master/.github/release.yml>`_.

*******
Support
*******

Reach out to me at one of the following places:

-  `Discord <https://discord.gg/6fmekudc8Q>`__
-  `Discussions <https://github.com/totaldebug/python-package-template/discussions>`__
-  `Issues <https://github.com/totaldebug/python-package-template/issues/new/choose>`__

******
Donate
******

Please consider supporting this project by sponsoring, or just donating
a little via `our sponsor
page <https://github.com/sponsors/marksie1988>`__.

**********
🛡 License
**********

[![License](https://img.shields.io/github/license/totaldebug/python-package-template)](https://github.com/totaldebug/python-package-template/blob/master/LICENSE)

This project is licensed under the terms of the license. See `LICENSE <https://github.com/totaldebug/python-package-template/blob/master/LICENSE>`_ for more details.
