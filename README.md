# Log Archive Tool

A simple command-line tool for archiving and compressing log files on Unix-based systems. This project is created for educational purposes as part of the roadmap.sh DevOps learning path(https://roadmap.sh/projects/log-archive-tool).

## Description

This tool archives log directories by compressing them into timestamped `.tar.gz` files.

## Project requirements

The tool should run from the command line, accept the log directory as an argument, compress the logs, and store them in a new directory. The user should be able to:

Provide the log directory as an argument when running the tool.

```bash
log-archive <log-directory>
```
The tool should compress the logs in a tar.gz file and store them in a new directory.

The tool should log the date and time of the archive to a file.

```bash
logs_archive_20240816_100648.tar.gz
```

## Features

- Compress log directories into `.tar.gz` archives
- Automatic timestamped archive names (format: `log_archive_YYMMDD_HHMMSS.tar.gz`)
- Configurable archive storage location


## Requirements

- Unix-based operating system 
- Bash shell
- `tar` command 

## Installation

1. Clone or download the script
2. Make it executable:
```bash
chmod +x log-archive
```

3. (Optional) Move to a directory in your PATH for global access:
```bash
sudo mv log-archive /usr/local/bin/
```

## Usage

### Basic Usage

```bash
./log-archive <log-directory>
```

**Example:**
```bash
./log-archive /var/log
```

This will create an archive in the current directory.

### Specify Archive Storage Location

```bash
./log-archive <log-directory> <archive-storage-directory>
```

**Example:**
```bash
./log-archive /var/log /home/user/log-archives/
```

## Arguments

| Argument | Required | Description | Default |
|----------|----------|-------------|---------|
| `<log-directory>` | Yes | Path to the directory containing logs to archive | - |
| `<archive-storage-directory>` | No | Directory where the archive will be stored | Current directory (`./`) |

## Output

The tool creates a compressed archive with the following naming format:
```
log_archive_YYMMDD_HHMMSS.tar.gz
```

**Example:** `log_archive_240816_100648.tar.gz`
