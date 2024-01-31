# Projector CLI

Projector CLI is a simple command-line tool that allows you to manage configuration values associated with specific directories.

## Installation

```bash
npm install
```

## Usage

### Options

- **args**: List of arguments for the operation.
- **config (-c)**: Path to the configuration file. If not provided, it defaults to `$HOME/.projector.json` or `$XDG_CONFIG_HOME/projector/.projector.json`.
- **pwd (-p)**: Path to the working directory. If not provided, it defaults to the current working directory.

### Operations

#### Print

To print all values associated with the current and parent directories:

```bash
npx ts-node index.ts
```

To print a specific value associated with the current or parent directory:

```bash
npx ts-node index.ts key
```

#### Add
To add or update a configuration value:

```bash
npx ts-node index.ts add key value
```

#### Remove
To remove a configuration value:

```bash
npx ts-node index.ts rm key
```

### Configuration File

The configuration file (default: $HOME/.projector.json or $XDG_CONFIG_HOME/projector/.projector.json) stores the configuration data. The structure is as follows:

```json
{
  "projector": {
    "/path/to/directory": {
      "key": "value"
    }
  }
}
```