description: Building Orion from source code
<!--- END of page meta data -->

# Build from source

## Prerequisites

* [Java JDK](http://www.oracle.com/technetwork/java/javase/downloads/index.html)

!!!important
    Orion requires Java 11+; earlier versions are not supported.

* [Git](https://git-scm.com/downloads) or [GitHub Desktop](https://desktop.github.com/)

* [libsodium](Dependencies.md)

## Installation on Linux / Unix / MacOS X

### Clone the Orion repository

Clone the `PegaSysEng/orion` repository:

```bash
git clone https://github.com/PegaSysEng/orion.git
```

### Build Orion

After cloning, go to the `orion` directory.

Build Orion with the Gradle wrapper `gradlew`, omitting tests as follows:

```bash
./gradlew build -x test
```

Go to the distribution directory:

```bash
cd build/distributions/
```

Expand the distribution archive:

```bash
tar -xzf orion-<version>.tar.gz
```

Move to the expanded folder and display the Orion help to confirm installation.

````bash
cd orion-<version>/
bin/orion --help
````

## Installation on Windows

### Install Orion

Clone the `PegaSysEng/orion` repository:

```bat
git clone https://github.com/PegaSysEng/orion.git
```

### Build Orion

Go to the `orion` directory:

```bat
cd orion
```

Build Orion with the Gradle wrapper `gradlew`, omitting tests as follows:

```bat
.\gradlew build -x test
```

!!!note
    To run `gradlew`, you must have the **JAVA_HOME** system variable set to the Java installation directory.
    For example: `JAVA_HOME = C:\Program Files\Java\jdk1.8.0_181`.

Go to the distribution directory:

```bat
cd build\distributions
```

Expand the distribution archive:

```bat
tar -xzf orion-<version>.tar.gz
```

Go to the expanded folder and display the Orion help to confirm installation.

```bat
cd orion-<version>
bin\orion --help
```
