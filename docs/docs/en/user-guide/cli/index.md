# FastAgency CLI Overview

The **FastAgency Command Line Interface (CLI)** enables developers to manage and run FastAgency projects directly from the terminal. The CLI simplifies interactions with FastAgency apps, providing options for running, testing, and managing workflows efficiently. Below is an overview of the key commands and options available in the FastAgency CLI.

## CLI Commands

### `dev`
```bash
$ fastagency dev [OPTIONS] [PATH]
```
The `dev` command runs a FastAgency app in **development mode**, which is equivalent to running `fastapi` but with live reload enabled. This is useful for testing and development, as it listens on `127.0.0.1` and automatically detects the Python module or package that needs to be imported based on the file or directory path provided.

#### Command Details:
- If no path is provided, it will try to locate the application using common file names like `main.py`, `app.py`, `api.py`, or from the `app` directory.
- It automatically detects the **FastAgency app** object to use, typically looking for an object named `app` or `api`.

#### Common Options:
- `--app`: The name of the variable that contains the FastAgency app in the imported module. It defaults to automatic detection.
- `--workflow (-w)`: Specifies the name of the workflow to run.
- `--initial_message (-i)`: Sets the initial message sent to the workflow.

### `run`
```bash
$ fastagency run [OPTIONS] [PATH]
```
The `run` command starts a FastAgency app in **production mode**, similar to the `dev` command, but optimized for production environments.

#### Common Options for `run`:
- `--app`: Specifies the name of the app variable to run, like in `dev`.
- `--workflow (-w)`: Specifies a particular workflow to run.
- `--initial_message (-i)`: Sends a custom initial message to the workflow.

### `version`
```bash
$ fastagency version
```
The `version` command shows the currently installed version of FastAgency.

### Global Options
- `--version`: Displays the current version of FastAgency.
- `--install-completion`: Installs shell completion for supported shells (bash, zsh, etc.).
- `--show-completion`: Shows the shell completion script for manual installation or customization.
- `--help`: Displays detailed help information for commands.

---

## Example Usage

### Running a FastAgency App in Development Mode
```bash
fastagency dev path/to/app.py
```

### Running a FastAgency App with a Specific Workflow
```bash
fastagency run path/to/app.py --workflow simple_workflow
```

### Setting an Initial Message
```bash
fastagency run path/to/app.py --initial_message "Hello, let's start!"
```

---

For more information, visit the [FastAgency Docs](https://fastagency.ai/latest/) or join our [**Discord community**](https://discord.gg/kJjSGWrknU).