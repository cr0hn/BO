booleans.io hider (Codename: SagaTo)
====================================

Hider/Unhider information to/from booleans.io.

Booleans.io is a curious service that provices *Booleans as a service (BaaS)*.

What's is Boolean-header
========================

This project allows to hide small chunks of text using boolean.io service. It's get a text, and transform into binary representation and store bit by bit into booleans.io.

Then Boolean-header (BO) save a .db file with the information, that you can use to recover remote info.

Install
=======

BO only have one dependency, you can install it doing:

.. code-block:: bash

    # pip install -r requirements.txt

Examples
========

**Hide** the content of a file:

.. code-block:: bash

    # echo "a\n" > my_text.txt
    # python hide.py -f my_text.txt -o hidden.db
    [i] Storing char: 'a'
        |- Storing bit '0'
        |- Storing bit '1'
        |- Storing bit '1'
        |- Storing bit '0'
        |- Storing bit '0'
        |- Storing bit '0'
        |- Storing bit '0'
        |- Storing bit '1'
    [i] Storing char: '
    '
        |- Storing bit '0'
        |- Storing bit '0'
        |- Storing bit '0'
        |- Storing bit '0'
        |- Storing bit '1'
        |- Storing bit '0'
        |- Storing bit '1'
        |- Storing bit '0'

**Unhide** with the file content:

.. code-block:: bash

    # python unhide.py -f hidden.db
