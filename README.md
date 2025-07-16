<img src="images/kw_logo.png" width="600" alt="kworkflow">

![Build Status](https://github.com/kworkflow/kworkflow/actions/workflows/unit_tests.yml/badge.svg?branch=master)

# Notes for CBSoft 2025 - Artifacts Festival

This repository is a modified version of the [upstream GitHub repository of kworkflow](https://github.com/kworkflow/kworkflow/) to fit the requirements for the **Available** and **Functional** badges as described in the [call for the Artifacts Festival of CBSoft 2025](https://cbsoft.sbc.org.br/2025/artefatos/?lang=en).

This modified version is based on the commit `8358ca2ee84059553729` of the master branch of the upstream repository. The only divergences are:

- The addition of this section to the `README.md` file
- The related paper's PDF file was submitted to the *Tools Track* of the *39th Brazilian Symposium on Software Engineering*

Below are the necessary entries to obtain the badges described in the call.

### Artifact description and repository organization

This artifact is a modified version (as aforementioned) of the repository containing the tool `kworkflow` (`kw`) source code, the object of the submitted paper.

The files and directories relative to the root of this repository worth highlighting are:

- `README.md`: README file
- `LICENSE`: file containing the project license, the *GNU General Public License Version 2 plus* (GPL-2.0+)
- `pre-print.pdf`: PDF file with pre-print version of the paper
- `kw`: entry point file of the tool
- `src`: directory with implementation of features, libraries, and plugins
- `tests`: directory with test suites
- `setup.sh`: installation script
- `run_tests.sh`: entry point file to run test suites

### Requirements

The only absolute requirement to install and run `kw` is to have a GNU/Linux distro based on Debian, Arch, or Fedora. Technically, any distro that has `apt`, `pacman`, or `dnf` as package managers available should work.

Regarding hardware requirements, `kw` does not need specific computing power to work. To run heavier commands that require kernel compilation from source code, i.e., some `kw build` commands, the faster your hardware, the better. However, this is a limitation of compiling the task of kernel compiling, not `kw` itself.

### Installation and Uninstallation

To install `kw`, you need to be at the root of this repository and run **one** of the following commands

```
./setup.sh --install # install kw normally
./setup.sh --full-installation # install kw w/ dependencies for kernel building
```

To remove `kw`, you can run **one** of the following commands (also at the root of the repository)

```
./setup.sh --uninstall # uninstall kw normally
./setup.sh --completely-remove # uninstall kw and all files under its responsibility
```

# About

kw has a simple mission: reduce the setup overhead of working with the Linux
kernel and provide tools to support developers in their daily tasks. If you
have a set of repeatable tasks that you usually perform while working in your
favorite kernel subsystem or similar, consider adding it as a part of kw.

# Install

Take a look at
[Install and Uninstall](documentation/content/installanduninstall.rst).

# How to

If you want to know more about kw's usage and its commands, take a look at
[Kw man](documentation/man/kw.rst) or, with kw installed, run `kw man`.

# Tests

If you want to know more about kw's tests take a look at
[kw tests](documentation/content/tests.rst).

# Generate Sphinx Documentation

If you want to generate the Sphinx documentation, you can use:

```
./setup.sh --docs
```

Finally, you can use your browser to look at the **index.html** page. For
example:

```
firefox build/index.html
```

# Contributing

We are happy that you want to help us! If you are looking for a good starting
point, check
[those issues](https://github.com/kworkflow/kworkflow/issues?q=is%3Aopen+label%3A%22good+first+issue%22+-label%3A%22done%3A+wait+for+stable%22)
and don't forget to read our
[Contribuitor's Guide](https://kworkflow.org/content/howtocontribute.html)
(or [howtocontribute file](documentation/content/howtocontribute.rst)).

# Reach Out

The best way to get help or make suggestions is by creating
[issues](https://github.com/kworkflow/kworkflow/issues) or making a
[pull request](https://github.com/kworkflow/kworkflow/pulls), someone is
likely to reply to these in little time.

# License

Kworkflow is under GPL-2.0+
