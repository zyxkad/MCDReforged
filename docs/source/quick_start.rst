
Quick Start
===========

This is a quick start tutorial of `MCDReforged <https://github.com/Fallen-Breath/MCDReforged>`__ (abbreviated as MCDR, omitted below)

Requirements
------------

MCDR requires python3 runtime. The python version need to be at least 3.6

Install
-------

MCDR is available in `pypi <https://pypi.org/project/mcdreforged>`__. It can be installed via ``pip`` command

.. code-block:: bash

    pip install mcdreforged

For Chinese users, you can added a ``-i https://pypi.tuna.tsinghua.edu.cn/simple`` prefix to the command to use `Tsinghua tuna mirror <https://mirrors.tuna.tsinghua.edu.cn/help/pypi/>`__ to speed up the installation

.. code-block:: bash

    pip install mcdreforged -i https://pypi.tuna.tsinghua.edu.cn/simple

Start up
--------

Let's say your are going to start MCDR in a folder named ``my_mcdr_server``. Then you can run the following commands to initialize the environment for MCDR first:

.. code-block:: bash

    cd my_mcdr_server
    python -m mcdreforged init

MCDR will generated the default configure and permission files, as well as some default folders. The file structure will be like this

.. code-block::

   my_mcdr_server/
    ├─ config/
    ├─ logs/
    │   └─ MCDR.log
    ├─ plugins/
    ├─ server/
    ├─ config.yml
    └─ permission.yml

Now put your server files into the server folder (``server`` by default), then modify the configuration file ``config.yml`` and permission file ``permission.yml`` correctly

After that you can launch MCDR, and it will start handling the server correctly

.. code-block:: bash

    python -m mcdreforged

Upgrade
-------

With the help of `pypi <https://pypi.org/project/mcdreforged/>`__, MCDR can be easily upgraded via a single command

.. code-block:: bash

    pip install mcdreforged --upgrade

That's it! 

For Chinese users, you can use tuna mirror to speed up the upgrading too

.. code-block:: bash

    pip install mcdreforged --upgrade -i https://pypi.tuna.tsinghua.edu.cn/simple

Development builds are available in `Test PyPi <https://test.pypi.org/project/mcdreforged/#history>`__, you can install them if you have special needs

Launch from source
------------------

Instead of installing MCDR from pypi, you can execute the source file of MCDR directly. **Notes: This is mostly for development purpose, DO NOT use it under a production environment**

Download the source files of MCDR via cloning the repository or github action, and decompress the file if needed

.. code-block::

   my_mcdr_server_in_source/
    ├─ mcdreforged/
    │   └─ ..
    ├─ MCDReforged.py
    ├─ setup.py
    └─ ..

MCDR will delay to start if the mcdreforged python package is not detected

So enter the directory ``my_mcdr_server_in_source/``, and run the following command to create egg_info to pass the detection

.. code-block:: bash

    python setup.py egg_info

After that, MCDR can be launched normally

.. code-block:: bash

    python -m mcdreforged

Alternatively you can execute ``MCDReforged.py`` with python to start MCDR

.. code-block:: bash

    python MCDReforged.py

``MCDReforged.py`` is just a simple wrapper for launching MCDR with the following codes

.. code-block:: python

    import sys

    from mcdreforged.__main__ import main

    if __name__ == '__main__':
        sys.exit(main())

``MCDReforged.py`` also works for MCDR installed by ``pip`` command

For windows users, if you have bound a correct python interpreter to ``*.py`` files you can also double click the ``MCDReforged.py`` to start MCDR
