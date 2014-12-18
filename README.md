# Jervis - [![Build Status][status-build]][travis-jervis]

* *Project status:* pre-alpha
* *Initially Targeted platforms:* Linux

Jervis is a combination of some letters in the words Jenkins and Travis: JEnkins
tRaVIS.  [Jenkins][jenkins] is a [continuous integration][wiki-ci] tool which is
typically installed on premises.  [Travis][travis] is a hosted, distributed
continuous integration system used by many [open source][wiki-os] projects.
Both Jenkins and Travis have paid and enterprise offerings.

Jervis uses Travis-like job generation using the [Job DSL
plugin][jenkins-plugin-job-dsl] and groovy scripts.  It reads the
[.travis.yml][travis-yaml] file of a project and generates a job in Jenkins
based on it.

For development planning and other documentation see the [Jervis
wiki][jervis-wiki].

# Building Jervis

## Dependencies

Groovy and Gradle must be installed.  Here are some of my system components.

* Gradle 1.4
* Groovy 1.8.6
* JVM 1.7.0\_65 (Oracle Corporation 24.65-b04)

## Build

Assemble dependencies.

    gradle assemble

Run unit tests.

    gradle check

Create a `jervis.jar` (only useful if using Jervis as a library class for your
own development).

    gradle build

[jenkins]: https://jenkins-ci.org/
[jenkins-plugin-job-dsl]: https://wiki.jenkins-ci.org/display/JENKINS/Job+DSL+Plugin
[jervis-wiki]: https://github.com/samrocketman/jervis/wiki
[status-build]: https://travis-ci.org/samrocketman/jervis.svg?branch=master
[travis]: https://travis-ci.org/
[travis-jervis]: https://travis-ci.org/samrocketman/jervis
[travis-yaml]: http://docs.travis-ci.com/user/build-configuration/
[wiki-ci]: https://en.wikipedia.org/wiki/Continuous_integration
[wiki-os]: http://en.m.wikipedia.org/wiki/Open_source
