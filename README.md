<h1 align="center">Sumario</h1>
<h2 align="center">Build a changelog in the Fatiando a Terra style</h2>
<p align="center">
Part of the <a href="https://www.fatiando.org"><strong>Fatiando a Terra</strong></a> project
</p>
<p align="center">
<a href="https://pypi.python.org/pypi/sumario"><img src="http://img.shields.io/pypi/v/sumario.svg?style=flat-square" alt="Latest version on PyPI"></a>
<a href="https://github.com/conda-forge/sumario-feedstock"><img src="https://img.shields.io/conda/vn/conda-forge/sumario.svg?style=flat-square" alt="Latest version on conda-forge"></a>
<a href="https://pypi.python.org/pypi/sumario"><img src="https://img.shields.io/pypi/pyversions/sumario.svg?style=flat-square" alt="Compatible Python versions."></a>
</p>

## About

*Sumario* is a small command-line program for generating a Markdown changelog
from the git history. It follows the format currently used in the Fatiando
projects and tries to automate some of our release process.

## Installing

*Sumario* is available from PyPI:

```
python -m pip install sumario
```

and conda-forge:

```
conda install sumario -c conda-forge
```

## Using

Generate a changelog skeleton based on changes since the last git tag:

```
$ sumario > changelog.md
Gathering changes since tag v0.3.2
Adding list of contributors
Formatting the changelog
Printing changes to standard output
Done!

$ cat changelog.md
## vX.Y.Z

**Released on:** 2022/08/19

**DOI**: [XXX](https://doi.org/XXX)

Highlights:

Breaking changes:

Deprecations:

Bug fixes:

New features:

Documentation:

Maintenance:

This release contains contributions from:

* Person A
* Person B
* Person C

* First commit message title And the body of the commit appended
  ([#123](https://github.com/fatiando/project/pulls/123)
* Second commit message title And the body of the commit appended
  ([#321](https://github.com/fatiando/project/pulls/321)
```

### Limitations

The current implementation is a proof-of-concept and has some limitations:

* No customizable templates for the changelog
* Changes are copied manually to the corresponding documentation page
* Zenodo DOI is assigned manually (it would be great to do this automatically
  using the Zenodo API, including adding new authors to the project and
  publishing the source archive)
* Entries are sorted manually

Of course, all of these could be addressed if there is enough interest.
Issues and PRs are welcome!

## Dependencies

We use the following dependencies (see `setup.cfg` for specific version
constraints):

* [click](https://click.palletsprojects.com) for building the command-line
  interface.

## Getting involved

🗨️ **Contact us:**
Find out more about how to reach us at
[fatiando.org/contact](https://www.fatiando.org/contact/).

👩🏾‍💻 **Contributing to project development:**
Please read our
[Contributing Guide](https://github.com/fatiando/community/blob/main/CONTRIBUTING.md)
to see how you can help and give feedback.

🧑🏾‍🤝‍🧑🏼 **Code of conduct:**
This project is released with a
[Code of Conduct](https://github.com/fatiando/community/blob/main/CODE_OF_CONDUCT.md).
By participating in this project you agree to abide by its terms.

> **Imposter syndrome disclaimer:**
> We want your help. **No, really.** There may be a little voice inside your
> head that is telling you that you're not ready, that you aren't skilled
> enough to contribute. We assure you that the little voice in your head is
> wrong. Most importantly, **there are many valuable ways to contribute besides
> writing code**.
>
> *This disclaimer was adapted from the*
> [MetPy project](https://github.com/Unidata/MetPy).

## License

This is free software: you can redistribute it and/or modify it under the terms
of the **BSD 3-clause License**. A copy of this license is provided in
[`LICENSE.txt`](https://github.com/fatiando/sumario/blob/main/LICENSE.txt).
