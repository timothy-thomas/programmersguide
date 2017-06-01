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

``git diff master.. -- . ':!bin/R'``