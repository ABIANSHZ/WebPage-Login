# MongoDB PHP Library

![Tests](https://github.com/mongodb/mongo-php-library/workflows/Tests/badge.svg)
![Coding Standards](https://github.com/mongodb/mongo-php-library/workflows/Coding%20Standards/badge.svg)

This library provides a high-level abstraction around the lower-level
[PHP driver](https://github.com/mongodb/mongo-php-driver) (`mongodb` extension).

While the extension provides a limited API for executing commands, queries, and
write operations, this library implements a full-featured API similar to that of
other MongoDB drivers. It contains abstractions for client, database, and
collection objects, and provides methods for CRUD operations and common commands
(e.g. index and collection management).

If you are developing an application with MongoDB, you should consider using
this library, or another high-level abstraction, instead of the extension alone.

Additional information about the architecture of this library and the `mongodb`
extension may be found in
[Architecture Overview](https://php.net/manual/en/mongodb.overview.php).

## Documentation

 - https://www.mongodb.com/docs/php-library/current/
 - https://www.mongodb.com/docs/drivers/php/

## Installation

The preferred method of installing this library is with
[Composer](https://getcomposer.org/) by running the following from your project
root:

    $ composer require mongodb/mongodb

Additional installation instructions may be found in the
[library documentation](https://mongodb.com/docs/php-library/current/tutorial/install-php-library/).

Since this library is a high-level abstraction for the driver, it also requires
that the `mongodb` extension be installed:

    $ pecl install mongodb
    $ echo "extension=mongodb.so" >> `php --ini | grep "Loaded Configuration" | sed -e "s|.*:\s*||"`

Additional installation instructions for the extension may be found in its
[PHP.net documentation](https://php.net/manual/en/mongodb.installation.php).

## Release Integrity

Releases are created automatically and the resulting release tag is signed using
the [PHP team's GPG key](https://pgp.mongodb.com/php-driver.asc). To verify the
tag signature, download the key and import it using `gpg`:

```shell
gpg --import php-driver.asc
```

Then, in a local clone, verify the signature of a given tag (e.g. `1.19.0`):

```shell
git show --show-signature 1.19.0
```

> [!NOTE]
> Composer does not support verifying signatures as part of its installation
> process.

## Reporting Issues

Issues pertaining to the library should be reported in the
[PHPLIB](https://jira.mongodb.org/secure/CreateIssue!default.jspa?project-field=PHPLIB)
project in MongoDB's JIRA. Extension-related issues should be reported in the
[PHPC](https://jira.mongodb.org/secure/CreateIssue!default.jspa?project-field=PHPC)
project.

For general questions and support requests, please use one of MongoDB's
[Technical Support](https://mongodb.com/docs/manual/support/) channels.

### Security Vulnerabilities

If you've identified a security vulnerability in a driver or any other MongoDB
project, please report it according to the instructions in
[Create a Vulnerability Report](https://mongodb.com/docs/manual/tutorial/create-a-vulnerability-report).

## Development

Development is tracked in the
[PHPLIB](https://jira.mongodb.org/projects/PHPLIB/summary) project in MongoDB's
JIRA. Documentation for contributing to this project may be found in
[CONTRIBUTING.md](CONTRIBUTING.md).
