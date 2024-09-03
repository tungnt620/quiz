# 2. Use poetry as package management tool

Date: 2024-09-03

## Status

Accepted

## Context

We need to manage the dependencies of the project.
Usually we use `pip` and `requirements.txt` to manage the dependencies of the project.
but sometimes it's hard to manage the dependencies and the versions of the dependencies.
For example, we must manually update the version of the dependencies in the `requirements.txt` file.
Sometimes I miss the version of the dependencies and the project doesn't work as expected.


## Decision

We will use `poetry` as a package management tool. 
Peotry automatically generates the `pyproject.toml` file that contains the dependencies of the project.
and `peotry.lock` file that contains the versions of the dependencies.
All files are automatically updated when we add or remove a dependency.
When another developer clones the project, they can install the dependencies with a single command `poetry install`.

## Consequences

Very easy for developers to install the dependencies of the project.
