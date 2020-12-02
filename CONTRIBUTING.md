# Contributing

If you want to contribute to Neos and want to set up a development environment, then follow these steps:

``composer create-project neos/neos-development-distribution neos-development dev-master --keep-vcs``

Note the **-distribution** package you create a project from, instead of just checking out this repository.

The code of the CMS can then be found inside ``Packages/Neos``, which itself is the neos-development-collection Git repository (due to the ``--keep-vcs`` option above). You commit changes and create pull requests from this repository.
To commit changes to Neos switch into the ``Neos`` directory (``cd Packages/Neos``) and do all Git-related work (``git add .``, ``git commit``, etc) there.

If you want to contribute to the Neos UI, please take a look at the explanations at https://github.com/neos/neos-ui#contributing on how to work with that.

If you want to contribute to the Flow Framework, you find that inside the ``Packages/Framework`` folder. See https://github.com/neos/flow-development-collection

In the root directory of the development distribution, you can do the following things:

- To run tests, run ``./bin/phpunit -c ./Build/BuildEssentials/PhpUnit/UnitTests.xml`` for unit or ``./bin/phpunit -c ./Build/BuildEssentials/PhpUnit/FunctionalTests.xml`` for functional/integration tests.

- To switch the branch you intend to work on: ``git checkout 3.3 && composer update``

.. note:: We use an upmerging strategy, so create all bugfixes to lowest maintained branch that contains the issue (typically the second last LTS release, which is 3.3 currently), or master for new features.

For more detailed information, see https://discuss.neos.io/t/development-setup/504 and https://discuss.neos.io/t/creating-a-pull-request/506
