# Installing BigchainDB

We're developing BigchainDB on Ubuntu 14.04, but it should work on any OS that runs RethinkDB Server and Python 3.4+. (BigchainDB is built on top of RethinkDB Server.)

## Install and Run RethinkDB Server

The RethinkDB documentation has instructions for how to install RethinkDB Server on a variety of operating systems. Do that (using their instructions for your OS): [Install RethinkDB Server](http://rethinkdb.com/docs/install/).

RethinkDB Server doesn't require any special configuration. You can run it by opening a Terminal and entering:
```shell
$ rethinkdb
```

## Install Python 3.4+

If you don't already have it, then you should [install Python 3.4+](https://www.python.org/downloads/) (maybe in a virtual environment, so it doesn't conflict with other Python projects you're working on).

## Install BigchainDB

BigchainDB has some OS-level dependencies. In particular, you need to install the OS-level dependencies for the Python **cryptography** package. Instructions for installing those dependencies on your OS can be found in the [cryptography package documentation](https://cryptography.io/en/latest/installation/).

On Ubuntu 14.04, we found that the following was enough (YMMV):
```shell
$ sudo apt-get update
$ sudo apt-get install libffi-dev g++ libssl-dev
```

With OS-level dependencies installed, you can install BigchainDB with `pip` or from source.

### How to Install BigchainDB with `pip`

BigchainDB is distributed as a Python package on PyPI. Installing is simple using `pip`:
```shell
$ pip install bigchaindb
```

### How to Install BigchainDB from Source

BigchainDB is in its early stages and being actively developed on its [GitHub repository](https://github.com/bigchaindb/bigchaindb). Contributions are highly appreciated.

Clone the public repository:
```shell
$ git clone git@github.com:bigchaindb/bigchaindb.git
```

Install from the source:
```shell
$ python setup.py install
```

### How to Install BigchainDB Using Docker

Coming soon...

## Run BigchainDB

After installing BigchainDB, run it with:
```shell
$ bigchaindb start
```

During its first run, BigchainDB takes care of configuring a single node environment.