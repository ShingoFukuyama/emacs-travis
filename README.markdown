Overview
========

Travis CI recipe for Emacs libraries.

Quickstart
----------

* Add the included .travis.yml and Makefile to your Emacs project on GitHub.

* Adapt the `make test` target to your taste.

* Create an account on http://travis-ci.org, and follow the instructions
  there to enable builds.

* Add `[![Build Status](https://secure.travis-ci.org/my-github-id/my-library.png)](http://travis-ci.org/my-github-id/my-library)`
  to your Markdown README file.

.travis.yml
-----------

The .travis.yml file included here supports

	Emacs 22
	Emacs 23
	Emacs 24 (stable)
	Emacs 24 (snapshot)

By default, the Emacs 23 and 24 environments are expected to build and test
your library successfully.  Emacs 22 and Emacs 24 (snapshot) are permitted
to fail.  See the `allow_failures:` section to change this.

It is not required to use the included example Makefile, but the .travis.yml
file expects working targets for `make test` and `make downloads`.  (The
`downloads` target fetches dependencies needed to run tests.)  You must
either

1. provide these targets, or
2. replace the `make` commands in .travis.yml with new build/test commands.
   See the `script` and `before_script` sections.  The `before-script` may be
   removed entirely.

See Also
--------

[http://about.travis-ci.org/docs/user/build-configuration/](http://about.travis-ci.org/docs/user/build-configuration/)