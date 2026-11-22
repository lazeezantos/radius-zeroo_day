# Task 3: Using `find` and `grep`

## Purpose of `find`
The `find` command is used to search for files and directories within a specified directory hierarchy based on various criteria such as file name, type, size, permissions, or modification time.

## Purpose of `grep`
The `grep` (Global Regular Expression Print) command is used to search for specific text patterns or strings inside the contents of one or more files, printing out the lines that match the pattern.

## Finding a Filename vs. Searching Inside a File
* **Finding a Filename (`find`):** Looks at file metadata and directory structures (e.g., searching for a file named `config.txt`). It does not read the actual data written inside the file.
* **Searching Inside a File (`grep`):** Opens and reads the text content within files to locate specific words, phrases, or regular expressions (e.g., searching for the word `"ERROR"` inside log files), regardless of what the file is named.

## Combined `find` and `grep` Command
Combining `find` and `grep` allows you to first locate a specific subset of files (such as all `.log` or `.txt` files) and then search inside only those matched files for a specific text pattern.

### Example
```bash
find . -type f -name "*.txt" -exec grep -H "search_term" {} +
```

### How It Works
* `find . -type f -name "*.txt"`: Searches the current directory (`.`) for regular files (`-type f`) whose names end with `.txt`.
* `-exec grep -H "search_term" {} +`: Passes the list of found files (`{}`) to the `grep` command, which searches inside each of them for `"search_term"` and prints the filename (`-H`) alongside every matching line.

