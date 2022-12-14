oclif-hello-world
=================

oclif example Hello World CLI

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![CircleCI](https://circleci.com/gh/oclif/hello-world/tree/main.svg?style=shield)](https://circleci.com/gh/oclif/hello-world/tree/main)
[![Downloads/week](https://img.shields.io/npm/dw/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![License](https://img.shields.io/npm/l/oclif-hello-world.svg)](https://github.com/oclif/hello-world/blob/main/package.json)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g chatgpt-cli
$ chatgpt-cli COMMAND
running command...
$ chatgpt-cli (--version)
chatgpt-cli/0.0.0 linux-x64 node-v16.17.1
$ chatgpt-cli --help [COMMAND]
USAGE
  $ chatgpt-cli COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`chatgpt-cli hello PERSON`](#chatgpt-cli-hello-person)
* [`chatgpt-cli hello world`](#chatgpt-cli-hello-world)
* [`chatgpt-cli help [COMMAND]`](#chatgpt-cli-help-command)
* [`chatgpt-cli plugins`](#chatgpt-cli-plugins)
* [`chatgpt-cli plugins:install PLUGIN...`](#chatgpt-cli-pluginsinstall-plugin)
* [`chatgpt-cli plugins:inspect PLUGIN...`](#chatgpt-cli-pluginsinspect-plugin)
* [`chatgpt-cli plugins:install PLUGIN...`](#chatgpt-cli-pluginsinstall-plugin-1)
* [`chatgpt-cli plugins:link PLUGIN`](#chatgpt-cli-pluginslink-plugin)
* [`chatgpt-cli plugins:uninstall PLUGIN...`](#chatgpt-cli-pluginsuninstall-plugin)
* [`chatgpt-cli plugins:uninstall PLUGIN...`](#chatgpt-cli-pluginsuninstall-plugin-1)
* [`chatgpt-cli plugins:uninstall PLUGIN...`](#chatgpt-cli-pluginsuninstall-plugin-2)
* [`chatgpt-cli plugins update`](#chatgpt-cli-plugins-update)

## `chatgpt-cli hello PERSON`

Say hello

```
USAGE
  $ chatgpt-cli hello [PERSON] -f <value>

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

_See code: [dist/commands/hello/index.ts](https://github.com/mabry1985/chatgpt-cli/blob/v0.0.0/dist/commands/hello/index.ts)_

## `chatgpt-cli hello world`

Say hello world

```
USAGE
  $ chatgpt-cli hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ chatgpt-cli hello world
  hello world! (./src/commands/hello/world.ts)
```

## `chatgpt-cli help [COMMAND]`

Display help for chatgpt-cli.

```
USAGE
  $ chatgpt-cli help [COMMAND] [-n]

ARGUMENTS
  COMMAND  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for chatgpt-cli.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.1.19/src/commands/help.ts)_

## `chatgpt-cli plugins`

List installed plugins.

```
USAGE
  $ chatgpt-cli plugins [--core]

FLAGS
  --core  Show core plugins.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ chatgpt-cli plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v2.1.7/src/commands/plugins/index.ts)_

## `chatgpt-cli plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ chatgpt-cli plugins:install PLUGIN...

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
  $ chatgpt-cli plugins add

EXAMPLES
  $ chatgpt-cli plugins:install myplugin 

  $ chatgpt-cli plugins:install https://github.com/someuser/someplugin

  $ chatgpt-cli plugins:install someuser/someplugin
```

## `chatgpt-cli plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ chatgpt-cli plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ chatgpt-cli plugins:inspect myplugin
```

## `chatgpt-cli plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ chatgpt-cli plugins:install PLUGIN...

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
  $ chatgpt-cli plugins add

EXAMPLES
  $ chatgpt-cli plugins:install myplugin 

  $ chatgpt-cli plugins:install https://github.com/someuser/someplugin

  $ chatgpt-cli plugins:install someuser/someplugin
```

## `chatgpt-cli plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ chatgpt-cli plugins:link PLUGIN

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
  $ chatgpt-cli plugins:link myplugin
```

## `chatgpt-cli plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ chatgpt-cli plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ chatgpt-cli plugins unlink
  $ chatgpt-cli plugins remove
```

## `chatgpt-cli plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ chatgpt-cli plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ chatgpt-cli plugins unlink
  $ chatgpt-cli plugins remove
```

## `chatgpt-cli plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ chatgpt-cli plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ chatgpt-cli plugins unlink
  $ chatgpt-cli plugins remove
```

## `chatgpt-cli plugins update`

Update installed plugins.

```
USAGE
  $ chatgpt-cli plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```
<!-- commandsstop -->
