# scala-glm

### Scala library for regression modelling (fitting linear and generalised linear statistical models, diagnosing fit, making predictions)

## Installation/Getting started

This library is simplest to use with [`sbt`](http://www.scala-sbt.org/). You should install `sbt` before attempting to use this library.

To use the pre-built binary, add the following lines to your `build.sbt`:
```scala
libraryDependencies += "com.github.darrenjw" %% "scala-glm" % "0.4"
```
The current [stable release](ReleaseNotes.md) is "0.4". It is cross-built for both Scala 2.12 and 2.13 and published to the [central repository](http://central.sonatype.org/). Version 0.3 was the final release for Scala 2.11.

There is a [giter8](http://www.foundweekends.org/giter8/) template for `scala-glm`, so using recent versions of SBT you can create a minimal `scala-glm` project template with:
```bash
sbt new darrenjw/scala-glm.g8
```

If you just want to try out the library without setting up any kind of project, you can do so with a session like:
```
$ sbt
> set scalaVersion := "2.13.4"
> set libraryDependencies += "com.github.darrenjw" %% "scala-glm" % "0.4"
> console
scala> import scalaglm._
```
See below for documentation links.

This library has a dependence on [Breeze](https://github.com/scalanlp/breeze), so if you have a dependence on `scala-glm` you don't need to add an additional dependence on Breeze. Some familiarity with Breeze is assumed for effective use of this library.

### Latest snapshot

If you want to use the latest snapshot, add the following to your `build.sbt`:

```scala
libraryDependencies += "com.github.darrenjw" %% "scala-glm" % "0.5-SNAPSHOT"
resolvers += "Sonatype Snapshots" at "https://oss.sonatype.org/content/repositories/snapshots/"
```

### Building from source

If building from source, running `sbt console` from this directory should give a Scala REPL with a dependence on the library. Running `sbt test` will run all tests (but note that an [**R**](https://www.r-project.org/) installation is required for many of the tests, which cross-check results against **R**). Running `sbt doc` will generate ScalaDoc API documentation.

## Documentation

* [QuickStart Guide](https://darrenjw.github.io/scala-glm/QuickStart.html) - start with this to get a feeling for what the library can do
* The [examples subdirectory](examples/src/main/scala/) of this repo contains more interesting, self-contained runnable examples
* The [example scripts](example-scripts/scripts/) directory contains scripts which can be pasted into the REPL
* [API documentation](https://darrenjw.github.io/scala-glm/api/scalaglm/) - ScalaDoc (for the most recent snapshot)
* For anyone not very familiar with Scala or Breeze, it may be worth working through my [Scala for Statistical Computing short course](https://github.com/darrenjw/scala-course). This library originated from example code prepared for that course.

## Author

This library is Copyright (C) 2017-2021 [Darren J Wilkinson](https://github.com/darrenjw), but released as open source software under an Apache 2.0 license.


