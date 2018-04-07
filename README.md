# Python Linters

It's probably a best practice to use linters, __especially__ with interpreted languages such as PHP or Python.

Here I am trying out [pycodestyle](http://pycodestyle.pycqa.org/en/latest/) and [pylint](https://www.pylint.org/).

## pycodestyle

This is probably the linter to use, specifically for the `PEP 8` integration.

#### Installation

Run the following command:

    $ pip install --user pycodestyle

#### Running

Run `pycodestyle` as follows:

    $ pycodestyle xxxxx.py

Limit `pycodestyle` to the first occurrence of a lint:

    $ pycodestyle --first xxxxx.py

Show the offending source code and the relevant text from PEP 8:

    $ pycodestyle --show-source --show-pep8 xxxxx.py

## pylint

I'm kind of a sucker for UML and pylint ships with an interesting-looking tool (`pyreverse`) which I wanted to try out.

#### Installation

Run the following command:

    $ pip install --user -r requirements-pylint.txt

#### Running

Run `pylint` as follows:

    $ pylint xxxxx.py

For any obsessive-compulsives, `pylint` provides a code score (and monitors progress).

Run `pyreverse` as follows:

    $ pyreverse -f PUB_ONLY -o png -p <package> *.py

[The default output format is `dot`, here we are specifying the graphic format `png`.]
