# Contributing Guide

Want to contribute to RESTEasy? We try to make it easy, and all contributions, even the smaller ones,
are more than welcome. This includes bug reports, fixes, documentation, etc. First though, please read this page
(including the small print at the end).

## Legal

All original contributions to RESTEasy are licensed under the
[ASL - Apache License](https://www.apache.org/licenses/LICENSE-2.0), version 2.0 or later, or, if another license is
specified as governing the file or directory being modified, such other license.

All contributions are subject to the [Developer Certificate of Origin (DCO)](https://developercertificate.org/).
The DCO text is also included verbatim in the [dco.txt](./dco.txt) file in the root directory of the repository.

## Reporting an issue

Most RESTEasy repositories use GitHub Issues for bug reports and feature requests. The main [resteasy](https://github.com/resteasy/resteasy)
repository uses [JIRA](https://issues.redhat.com/browse/RESTEASY), which requires an account. If you do not wish to signup for a JIRA account,
you can open a [discussion](https://github.com/resteasy/resteasy/discussions) and we will assist you in filing an issue.

If you believe you found a bug, please indicate a way to reproduce it, what you are seeing and what you would expect to see.

## Before you contribute

To contribute, use GitHub Pull Requests, from your **own** fork.

Also, make sure you have set up your Git authorship correctly:

```
git config --global user.name "Your Full Name"
git config --global user.email your.email@example.com
```

If you use different computers to contribute, please make sure the name is the same on all your computers.

We use this information to acknowledge your contributions in release announcements.

## Setup

If you have not done so on this machine, you need to:

* Install Git and configure your GitHub access
* Install Java SDK 11+ (OpenJDK recommended)

### IDE Config and Code Style

RESTEasy has a strictly enforced code style. Code formatting is done by the Eclipse code formatter, using the config files
found in the [eclipse-code-formatter.xml](https://raw.githubusercontent.com/resteasy/resteasy-dev-tools/main/ide-config/src/main/resources/eclipse-code-formatter.xml)
file. By default, when you run `./mvnw install`, the code will be formatted automatically.
When submitting a pull request the CI build will fail if running the formatter results in any code changes, so it is
recommended that you always run a full Maven build before submitting a pull request.

If you want to run the formatting without doing a full build, you can run `./mvnw process-sources`.

#### Eclipse Setup

Open the *Preferences* window, and then navigate to *Java* -> *Code Style* -> *Formatter*. Click *Import* and then
select the `eclipse-code-formatter.xml` downloaded from the above link or clone the repository and navigate to the file.

Next navigate to *Java* -> *Code Style* -> *Organize Imports*. Click *Import* and select the [eclipse.importorder](https://raw.githubusercontent.com/resteasy/resteasy-dev-tools/main/ide-config/src/main/resources/eclipse.importorder) file.

#### IDEA Setup

Install the [Adapter for Eclipse Code Formatter](https://plugins.jetbrains.com/plugin/6546-adapter-for-eclipse-code-formatter/).
See the [documentation](https://github.com/krasa/EclipseCodeFormatter#instructions) on how to configure the plugin.

## Contributing Your Changes

### Creating a Pull Request

1. Fork the repository you want to contribute to
2. Create a feature branch from the default branch (usually `main`)
3. Make your changes and commit them with descriptive commit messages
4. Push your branch to your fork
5. Open a Pull Request against the original repository

By submitting a pull request, you agree to the [Developer Certificate of Origin (DCO)](https://developercertificate.org/)
as outlined in the Legal section above.

### Testing

Before submitting a pull request, ensure that all tests pass. Each project may have different test commands -
refer to the project's README for specific build and test instructions.

### Getting Help

If you have questions or need help with your contribution:

* Open a [discussion](https://github.com/orgs/resteasy/discussions) in the RESTEasy organization
* Ask in the pull request itself
* For project-specific questions, check the individual project's README or documentation
