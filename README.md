# Python Linters

It's probably a best practice to use linters, __especially__ with interpreted languages such as PHP or Python.

If you are a beginner they will generally catch any ___n00b___ errors - which will probably save everyone some
time and/or embarrassment. And for most people they will often catch potential problems that were not spotted. For
anyone who frequently uses different languages, they suggest a style and idiom appropriate for the language. Often
these seem to be very minor things - but they may have specific meanings in any particular language. For instance,
whether or not a variable or function is __capitalised__ can be significant - but often it will simply be such
useful suggestions as using underscores instead of hyphens, and whether or not camel-case is appropriate.

All in all, it's generally a best practice to keep code as idiomatic as possible. And linters are great for this.

Here I am trying out [pycodestyle](http://pycodestyle.pycqa.org/en/latest/), [pylint](https://www.pylint.org/),
and [pydocstyle](https://github.com/PyCQA/pydocstyle).

## pycodestyle

This is probably the linter to use, specifically for the `PEP 8` integration.

However, I still like `pylint` quite a lot, for one thing it will complain if a file is not named in a Pythonesque
way. And they've gamified `pylint` pretty well, it's oddly satisfying to clean up formatting and see the code score
improve.

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

## pydocstyle

While not strictly a linter, having well-formed docstrings allows for the use of automated documentation generators.

#### Installation

Run the following command:

    $ pip install --user pydocstyle

#### Running

Run `pydocstyle` as follows:

    $ pydocstyle xxxxx.py

There are a number of configurable options. For instance, it's possible to list PEP257 conventions to ignore as follows:

    $ pydocstyle xxxxx.py --ignore=D210,D213,D401

A full list of pydocstyle errors may be found [here](http://www.pydocstyle.org/en/latest/error_codes.html).

[My personal feeling is that `pydocstyle` should be run from time to time, but is
 probably a bit too finicky for regular use. Your mileage may vary.]
