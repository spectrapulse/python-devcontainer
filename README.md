# Python Dev Environment
Powered by VSCode's dev environments.

## What is this repository for?
It's just a simple template that I use for starting a Python project. There isn't much special about it.

## What does it set up for me?
It prepares a docker container with my default collection of tooling.

This includes:
- [Poetry](https://python-poetry.org/) - I use this for my dependency management because it is powerful with minimal configuration.
- [Nox](https://nox.thea.codes/en/stable/) and [pytest](https://docs.pytest.org/) - Usually, when I do test-driven development or require testing in my code, this is my go-to solution for the job. This combination is ideal for testing in multiple Python environments.
- [Black](https://black.readthedocs.io/) - Black handles my formatting. Due to its more sensible and beautiful approach to formatting while respecting the [PEP 8](https://pep8.org/) coding convention.
- [Flake8](https://flake8.pycqa.org/) - I use Flake8 because it has a modular nature. It is allowing me to enforce style guides more granularly. This is especially useful when a project practices [CI/CD](https://en.wikipedia.org/wiki/CI/CD) or has multiple collaborators. Being able to automate this is essential for a nicer overall workflow.
- [Pyright]() - Pyright is here to do the heavy lifting while developing. Type Checking is essential to avoid headaches in the future. Pyright is excellent for its use case, especially since it's already included with the VSCode Python extension by default. Most people already use it, and it ensures perfect integration with VSCode.