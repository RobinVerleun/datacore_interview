# Datacore Take Home Assignment

This repository is a small [monorepo](https://en.wikipedia.org/wiki/Monorepo) with two projects in two different languages.

## Instructions

1. Configure a build system for a go and a python project.
    * Builds should run automatically on commit.
    * Individual projects should only be built if there have been changes within the project. e.g. The go build should either not run or stop immediately after starting when changes to the python project are committed.
2. Some builds require that some steps only be executed when there is a commit to a specific branch. Details are included in the associated language project folders.
3. Care should be taken to make sure project builds are isolated from each other.

## Deliverables

1. A publicly accessible link to the git repository (e.g. GitHub, Bitbucket, etc.)
2. A publicly accessible link to the output of your build pipeline

## Helpful Tips

1. Assume that all builds should be run on a *nix like operating system
2. Assume that the underlying version control system is git
3. Each language folder contains a `Makefile` with the same 4 make targets that should be run in the following order
    1. `deps` - Install dependencies
    2. `test` - Run unit tests
    3. `build` - Produce an artefact
    4. `publish` - Simulate publishing a successfully built artefact to a package repository. **This target should not be run on any git branch other than master i.e. only run this target when building the master branch**
4. The README.md file in each language folder contains more detailed instructions for the various make targets and how to run them with the `make` command

## Free Build Services

Please use which ever build system you are the most comfortable with, we want to know what you are capable of using a tool you are already familiar with. If you are not familiar with an existing CI/CD tool here are some recommendations for free cloud-based build services you could use:

* [CircleCI](https://circleci.com/)
* [Travis CI](https://www.travis-ci.com/)
* [GitHub Actions](https://github.com/features/actions)
* [Bitbucket Pipelines](https://bitbucket.org/product/features/pipelines)