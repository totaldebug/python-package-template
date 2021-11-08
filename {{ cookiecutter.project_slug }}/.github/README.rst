.. raw:: html

   <h1 align="center">


.. raw:: html

   </h1>

   <h1 align="center">

{{ cookiecutter.project_name }}

|Python Version|

    .. |Python Version| image:: https://img.shields.io/pypi/pyversions/{{ cookiecutter.project_name }}.svg?style=flat-square&logoColor=white
       :target: https://pypi.org/project/{{ cookiecutter.project_name }}/

|Dependencies Status|

    .. |Dependencies Status| image:: https://img.shields.io/badge/dependencies-up%20to%20date-brightgreen.svg?style=flat-square&logoColor=white
       :target: https://github.com/{{ cookiecutter.github_name }}/{{ cookiecutter.project_name }}/pulls?utf8=%E2%9C%93&q=is%3Apr%20author%3Aapp%2Fdependabot

|black|

    .. |black| image:: https://img.shields.io/badge/code%20style-black-000000.svg?style=flat-square&logoColor=white)](https://github.com/psf/black
       :target:

|Security: bandit|

    .. |black| image:: https://img.shields.io/badge/security-bandit-green.svg?style=flat-square&logoColor=white
       :target: https://github.com/PyCQA/bandit

|Pre-commit|

    .. |Pre-commit| image:: https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&style=flat-square&logoColor=white
       :target: https://github.com/{{ cookiecutter.github_name }}/{{ cookiecutter.project_name }}/blob/master/.pre-commit-config.yaml

|Semantic Versions|

    .. |Semantic Versions| image:: https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--versions-e10079.svg?style=flat-square
       :target: https://github.com/{{ cookiecutter.github_name }}/{{ cookiecutter.project_name }}/releases

|License|

    .. |License| image:: https://img.shields.io/github/license/{{ cookiecutter.github_name }}/{{ cookiecutter.project_name }}?style=flat-square&logoColor=white
       :target: https://github.com/{{ cookiecutter.github_name }}/{{ cookiecutter.project_name }}/blob/master/LICENSE

.. raw:: html

   </h1>

   <p align="center">

`About`_ • `Install`_ • `Contribute`_ • `Author`_ • `Support`_ • `Donate`_ • `Full Documentation <https://docs.totaldebug.uk/{{ cookiecutter.project_name }}>`_

.. raw:: html

   </p>

   <p align="center">

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

{{ cookiecutter.project_description }}

.. raw:: html

   </td>
   </tr>
   </table>

*******
Install
*******

{% if cookiecutter.use_pypi_deployment_with_actions == 'y' -%}
This package is distributed on PyPI_ and can be installed with ``pip``:

.. code:: bash

   pip install -U {{ cookiecutter.project_name }}

or install with ``Poetry``

.. code:: bash

   poetry add {{ cookiecutter.project_name }}

{%- else -%}



{% endif %}

For more information read the full documentation on `installing the package`_

.. _PyPI: https://pypi.python.org/pypi/{{ cookiecutter.project_name }}
.. _installing the package: https://docs.totaldebug.uk/{{ cookiecutter.project_name }}/installing.html


Makefile usage
==============

[`Makefile`](https://github.com/{{ cookiecutter.github_name }}/{{ cookiecutter.project_name }}/blob/master/Makefile) contains a lot of functions for faster development.

.. raw:: html

   <details>
   <summary>1. Download and remove Poetry</summary>
   <p>

To download and install Poetry run:

.. code:: bash

   make poetry-download

To uninstall

.. code:: bash

   make poetry-remove

.. raw:: html

   </p>
   </details>
   <details>
   <summary>2. Install all dependencies and pre-commit hooks</summary>
   <p>

Install requirements:

.. code:: bash

   make install

Pre-commit hooks coulb be installed after `git init` via

.. code:: bash

   make pre-commit-install

.. raw:: html

   </p>
   </details>
   <details>
   <summary>3. Codestyle</summary>
   <p>

Automatic formatting uses ``pyupgrade``, ``isort`` and ``black``.

.. code:: bash

   make codestyle

   # or use synonym
   make formatting

Codestyle checks only, without rewriting files:

.. code:: bash

   make check-codestyle

> Note: ``check-codestyle`` uses ``isort``, ``black`` and ``darglint`` library

.. raw:: html

   <details>
   <summary>4. Code security</summary>
   <p>

.. code:: bash

   make check-safety

This command launches ``Poetry`` integrity checks as well as identifies security issues with `Safety` and `Bandit`.

.. code:: bash

   make check-safety

.. raw:: html

   </p>
   </details>
   </p>
   </details>
   <details>
   <summary>5. Type checks</summary>
   <p>

Run `mypy` static type checker

.. code:: bash

   make mypy

.. raw:: html

   </p>
   </details>
   <details>
   <summary>6. Tests</summary>
   <p>

Run `pytest`

.. code:: bash

   make test

.. raw:: html

   </p>
   </details>
   <details>
   <summary>7. All linters</summary>
   <p>

Of course there is a command to ~~rule~~ run all linters in one:

.. code:: bash

   make lint

the same as:

.. code:: bash

   make test && make check-codestyle && make mypy && make check-safety

.. raw:: html

   </p>
   </details>
   <details>
   <summary>8. Cleanup</summary>
   <p>
Delete pycache files

.. code:: bash

   make pycache-remove

Remove package build

.. code:: bash

   make build-remove

Or to remove pycache and build:

.. code:: bash

   make clean-all

.. raw:: html

   </p>
   </details>


************
📈 Releases
************

You can see the list of available releases on the `GitHub Releases <https://github.com/{{ cookiecutter.github_name }}/{{ cookiecutter.project_name }}/releases>`_ page.

We follow [Semantic Versions](https://semver.org/) specification.

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

You can update it in `release.yml <https://github.com/{{ cookiecutter.github_name }}/{{ cookiecutter.project_name }}/blob/master/.github/release.yml>`_.

**********
Contribute
**********

Got **something interesting** you'd like to **share**? Learn about
contributing in our `contributing guide`_.

.. _contributing guide: https://docs.totaldebug.uk/{{ cookiecutter.project_name }}/contributing.html

*******
Support
*******

Reach out to me at one of the following places:

-  `Discord <https://discord.gg/6fmekudc8Q>`__
-  `Discussions <https://github.com/{{ cookiecutter.github_username }}/{{ cookiecutter.project_name }}/discussions>`__
-  `Issues <https://github.com/{{ cookiecutter.github_username }}/{{ cookiecutter.project_name }}/issues/new/choose>`__

******
Donate
******

Please consider supporting this project by sponsoring, or just donating
a little via `our sponsor
page <https://github.com/sponsors/{{ cookiecutter.github_sponsor }}>`__.

**********
🛡 License
**********

[![License](https://img.shields.io/github/license/{{ cookiecutter.github_name }}/{{ cookiecutter.project_name }})](https://github.com/{{ cookiecutter.github_name }}/{{ cookiecutter.project_name }}/blob/master/LICENSE)

This project is licensed under the terms of the `{{ cookiecutter.license }}` license. See `LICENSE <https://github.com/{{ cookiecutter.github_name }}/{{ cookiecutter.project_name }}/blob/master/LICENSE>`_ for more details.
