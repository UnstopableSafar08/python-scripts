# Python Scripts

## Installing the Scripts

1. Clone the repo:<br> `git clone https://github.com/UnstopableSafar08/python-scripts.git`
2. Make the scripts executable: <br> `chmod +x python-scripts/install-python && chmod +x python-scripts/uninstall-python`
3. Add the scripts to your path by adding the following to your .bashrc/.zshrc/etc.:<br> `PATH=$PATH:/path/to/python-scripts`
4. Apply the changes:<br>`source .bashrc`

## Installing Python

You can install Python using the following command:

```sh
python-scripts/install-python <ver1> [ver2 ...]
# For Single Version: python-scripts/install-python 3.8.1
# For Multiple Version:  python-scripts/install-python 3.8.1 3.9.5 
```

This command will Download the Python from the official FTP server and then install the python on the machine.
While this means you can install any Python version you want, the installation process will take significantly longer.
Alpha, beta, and release candidate versions can also be installed, and multiple version can be installed at once.


**Note:** If you do not use a Debian-based system, you will need to edit the script to use your distribution's package manager.

## Uninstalling Python

You can uninstall Python using the following command:

```sh
python-scripts/uninstall-python <ver1> [ver2 ...]
# For e.g.(single version): python-scripts/uninstall-python 3.8.1
# For e.g. (Multiple Version): python-scripts/uninstall-python 3.8.1 3.9.5 3.10.2
```

This removes all files related to the given Python versions.

For example, if you ran the following command...

```sh
python-scripts/uninstall-python 3.8
```

...the following directories and files will be deleted:

* /usr/local/bin/2to3-3.9
* /usr/local/bin/idle3.9
* /usr/local/bin/pip3.9
* /usr/local/bin/pydoc3.9
* /usr/local/bin/python3.9
* /usr/local/bin/python3.9-config
* /usr/local/lib/libpython3.9.a
* /usr/local/lib/python3.9
* /usr/local/lib/python3.9-embed.pc
* /usr/local/lib/python3.9.pc

Like when installing Python, multiple versions can be uninstalled at once.

**Warning:** If you have two installations for a single minor version of Python (i.e. 3.10.1 and 3.10.5), they will both be removed.

**Warning:** Attempting to uninstall Python versions bundled with your OS may render your OS unusable.
