---
layout: default
title: Repository Structure
nav_order: 8
---
[//]: # (SPDX-License-Identifier: CC-BY-4.0)

# Common Repository Structure

Green Software Foundation projects are required to maintain a standard set of files in each repository. This
document describes the required and recommended files.

## Required Files with Specified Content

Repositories MUST have these files with the specific content in the linked files, or a file with a
link to the specified content with minimal exposition. These files MUST be at the root of the
repository.

-   [`LICENSE`](https://opensource.org/licenses/MIT) - https://opensource.org/licenses/MIT\
    (Or whatever licence is approved for use for this project)
-   [`CODE_OF_CONDUCT.md`](https://greensoftware.foundation/code-of-conduct) - https://greensoftware.foundation/code-of-conduct


## Required Files with Variable Content

Repositories MUST have these files. Named files MUST be at the root of the repository, and may have
format suffixes such as `.md`, `.rst`, or `.txt`.

-   `README` \
    A description of the project and contain information or links to information such as
    -   A reference to the license (required).
    -   The current and important past releases
    -   Documentation for developers and users
-   `CONTRIBUTING` \
    Directions on how to contribute code to the project, or a pointer to the Wiki page with that information.
-   `CHANGELOG` \
    A human readable list of recent changes. Changes should at least include the current release. This
    file may be maintainer curated or mechanically produced.
-   Continuous Integration / Continuous Delivery (CICD) configurations \
    Configurations needed to run CICD on Green Software Foundation provided systems.

## Recommended

Repositories SHOULD have these files. Named files SHOULD be at the root of the repository

-   Build files consistent with the implementation language, such as...
    -   For JavaScript/Node.js a `package.json` file
    -   For Ruby a `Gemfile` file
    -   For Java one of a Maven `pom.xml`, an Apache Ant `build.xml`, or a Gralde `build.gradle`
        file
    -   For Python `setup.py` and `requirements.txt` files
    -   For Go `go.mod` and optionally `go.sum` 
    -   For Rust a `cargo.toml` file
    -   For multi-lingual repositories a `Makefile` or executable `build.sh` script
    -   For other languages, other standard build files a practitioner of the language would expect.
-   Testing code \
    Code to test the code in the repository (such as unit tests), in a location appropriate for the language.
    \
    Not all repositories can be tested (homebrew, docs), which is the only reason this is a SHOULD.

## Prohibited

Repositories MUST NOT have these files

-   Executable binaries and shared library files built by code in the repository \
    This includes `.exe`, `.dll`, `.so`, `.a` and `.dylib` files not otherwise part of a third party
    library.

