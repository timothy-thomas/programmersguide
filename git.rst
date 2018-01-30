.. _git:

git
===

Creating a Repository
---------------------

You can create a repository with a ``git init`` command.

Diffing
-------

Exclude Directory
~~~~~~~~~~~~~~~~~

To ignore a certain directory, for example ``bin/R``, when diffing do something like this:

.. 

``git diff master.. -- . ':!bin/R'``

Adjust Diff Behaviour Per File
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

You can create a dummy diff like this:

.. code-block:: batch

   git config diff.nodiff.command /bin/true

``/bin/true`` can be anything that returns true or zero.
Then create or append a line to ``.git/info/attributes`` or add it to the
``.gitattributes`` file in the project root if you want to share this
setting:

.. code-block:: batch

   example-file.xml    diff=nodiff
   *.xme               diff=nodiff
