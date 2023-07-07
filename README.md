# Shell Script Backup Utility

This is a simple shell script that performs backup operations from a source directory to a destination directory. The script checks if the correct number of arguments is provided, validates the directory paths, and performs the backup based on specific tasks.

## Prerequisites

- This script requires Bash to be installed on your system.

## Usage

```shell
./backup.sh target_directory_name destination_directory_name
```

- `target_directory_name`: The path to the directory you want to back up.
- `destination_directory_name`: The path to the directory where the backup file will be stored.

## Functionality

1. Checks if the correct number of arguments is provided. If not, it displays an error message and exits.
2. Validates the provided directory paths, ensuring they exist.
3. Prints the target directory and destination directory paths.
4. Generates a backup file name using the current timestamp.
5. Saves the current working directory as the original absolute path.
6. Changes the working directory to the destination directory.
7. Saves the destination directory's absolute path.
8. Calculates the timestamp for yesterday.
9. Iterates through the files in the target directory.
10. Displays each file's modification date and compares it with yesterday's timestamp.
11. Adds files modified within the last 24 hours to the backup list.
12. Creates a tar.gz backup file using the generated backup file name and the files in the backup list.
13. Moves the created backup file to the destination directory.

## Example

```shell
./backup.sh /path/to/source /path/to/destination
```

- The script will perform a backup operation from the `/path/to/source` directory to the `/path/to/destination` directory. It will create a backup file with a name like `backup-[timestamp].tar.gz` containing files modified within the last 24 hours.
