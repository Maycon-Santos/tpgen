tgen
=================

tgen is a versatile Command Line Interface (CLI) tool that empowers developers to effortlessly generate custom folder and file structures based on their specific requirements. With tgen, you can define a directory structure pattern in the configuration file and swiftly create that layout in your project with a single command.

No more tedious manual setup of repetitive folder structures for various projects. Whether you seek consistency in organizing your team's projects or simply want to expedite your project's initialization, tgen has you covered. Its configuration file enables you to tailor the structure pattern, leaving you more time to focus on your development tasks.

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![CircleCI](https://circleci.com/gh/oclif/hello-world/tree/main.svg?style=shield)](https://circleci.com/gh/oclif/hello-world/tree/main)
[![GitHub license](https://img.shields.io/github/license/oclif/hello-world)](https://github.com/oclif/hello-world/blob/main/LICENSE)

#### Key Features:

- Rapid and automated generation of folder and file structures.
- Configuration file for customizable structure patterns.
- Intuitive command-line interface for seamless interactions.
- Versatility to support projects of all scales and technologies.
- Facilitates team collaboration with standardized organization across projects.

# Topics
<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g tgen
$ tgen COMMAND
running command...
$ tgen (--version)
tgen/0.0.0 linux-x64 node-v16.20.1
$ tgen --help [COMMAND]
USAGE
  $ tgen COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`tgen hello PERSON`](#tgen-hello-person)
* [`tgen hello world`](#tgen-hello-world)
* [`tgen help [COMMANDS]`](#tgen-help-commands)
* [`tgen plugins`](#tgen-plugins)
* [`tgen plugins:install PLUGIN...`](#tgen-pluginsinstall-plugin)
* [`tgen plugins:inspect PLUGIN...`](#tgen-pluginsinspect-plugin)
* [`tgen plugins:install PLUGIN...`](#tgen-pluginsinstall-plugin-1)
* [`tgen plugins:link PLUGIN`](#tgen-pluginslink-plugin)
* [`tgen plugins:uninstall PLUGIN...`](#tgen-pluginsuninstall-plugin)
* [`tgen plugins:uninstall PLUGIN...`](#tgen-pluginsuninstall-plugin-1)
* [`tgen plugins:uninstall PLUGIN...`](#tgen-pluginsuninstall-plugin-2)
* [`tgen plugins update`](#tgen-plugins-update)

## `tgen hello PERSON`

Say hello

```
USAGE
  $ tgen hello PERSON -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Who is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ oex hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [dist/commands/hello/index.ts](https://github.com/Maycon-Santos/tgen/blob/v0.0.0/dist/commands/hello/index.ts)_

## `tgen hello world`

Say hello world

```
USAGE
  $ tgen hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ tgen hello world
  hello world! (./src/commands/hello/world.ts)
```

## `tgen help [COMMANDS]`

Display help for tgen.

```
USAGE
  $ tgen help [COMMANDS] [-n]

ARGUMENTS
  COMMANDS  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for tgen.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.2.11/src/commands/help.ts)_

## `tgen plugins`

List installed plugins.

```
USAGE
  $ tgen plugins [--core]

FLAGS
  --core  Show core plugins.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ tgen plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v2.4.7/src/commands/plugins/index.ts)_

## `tgen plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ tgen plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ tgen plugins add

EXAMPLES
  $ tgen plugins:install myplugin 

  $ tgen plugins:install https://github.com/someuser/someplugin

  $ tgen plugins:install someuser/someplugin
```

## `tgen plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ tgen plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ tgen plugins:inspect myplugin
```

## `tgen plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ tgen plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ tgen plugins add

EXAMPLES
  $ tgen plugins:install myplugin 

  $ tgen plugins:install https://github.com/someuser/someplugin

  $ tgen plugins:install someuser/someplugin
```

## `tgen plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ tgen plugins:link PLUGIN

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Links a plugin into the CLI for development.
  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.


EXAMPLES
  $ tgen plugins:link myplugin
```

## `tgen plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ tgen plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ tgen plugins unlink
  $ tgen plugins remove
```

## `tgen plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ tgen plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ tgen plugins unlink
  $ tgen plugins remove
```

## `tgen plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ tgen plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ tgen plugins unlink
  $ tgen plugins remove
```

## `tgen plugins update`

Update installed plugins.

```
USAGE
  $ tgen plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```
<!-- commandsstop -->
