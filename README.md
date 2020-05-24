# Quarkus Integration for JetBrains IntelliJ IDEA

![build](https://github.com/conceptivesolutions/quarkus-intellij-plugin/workflows/build/badge.svg)
![version](https://img.shields.io/github/v/release/wglanzer/quarkus-intellij-plugin)

This plugin adds features to JetBrains IntelliJ IDEA to integrate [quarkus.io](http://quarkus.io) a lot better and make it behave like
a "normal IntelliJ IDEA application". This means that this plugin will execute all necessary build steps automatically and attaches a debugger if you want to.
Debug your quarkus applications without effort!  

:white_check_mark: IntelliJ Version 2020.1 ( https://plugins.jetbrains.com/plugin/14242-quarkus-integration )

:white_check_mark: Maven Plugin

:white_check_mark: Gradle Plugin


## Features
### Quarkus Run Configuration Type
#### Build Tool: Maven
This plugin adds a run configuration type, named "Quarkus (Maven)". 
It will execute the "quarkus:dev" maven goal in background and attach a new debugger instance via remote config if necessary.

![Quarkus Run Configuration Type](.github/docs/runconfig_maven.png)

Working Directory: The root maven module to execute maven in

VM Options: A list of parameters which will be delegated to maven

JRE: Maven will use this JRE to run

Environment Variables: Variables that will be passed to maven execution environment

Compile before launch: check this option, if you want to execute the "clean" and "compile" tasks before launching "quarkus:dev"

#### Build Tool: Gradle
This plugin adds a run configuration type, named "Quarkus (Gradle)" for gradle too.
It will execute the "quarkusDev" gradle task in background and attach a new debugger isntance via remote config if necessary.

![Quarkus Run Configuration Type](.github/docs/runconfig_gradle.png)

Gradle Project: The root gradle project to start the quarkus build in

VM Options: A list of parameters which will be delegated to gradle

Arguments: Arguments that will be delegated to gradle

Environment Variables: Variables that will be passed to gradle execution environment

Compile before launch: check this option, if you want to execute the "clean" and "build" tasks before launching "quarkusDev"

### Debug your Quarkus applications
![Debug Window](.github/docs/debug.png)

If you want to debug your quarkus application, just start the newly added run configuration type within debug mode.
It will automatically assign a new port to the "quarkus:dev" step and connects via remote debug config - 
so seamless, that you won't notice any difference to your other java projects.

## How to install?
### Official Release
You can download this plugin within the official JetBrains plugin dialog integrated in IntelliJ IDEA.
![Plugin Dialog](.github/docs/plugin_dialog.png)

### GitHub Release
There can be some releases which are not supposed to be publicly available yet.
Those releases can be installed manually by downloading the latest releases on github.

[https://github.com/conceptivesolutions/quarkus-intellij-plugin/releases/latest](https://github.com/conceptivesolutions/quarkus-intellij-plugin/releases/latest)

The downloaded .zip file can be installed within the official JetBrains plugin dialog too.
Just click "Install Plugin from Disk..." and select your previously downloaded file.
![Plugin Dialog](.github/docs/plugin_manually.png)
