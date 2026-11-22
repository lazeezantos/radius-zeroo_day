# Task 2: Linux Command Line Practice

## 1. Commands Practised
During this task, I practised using the following Linux terminal commands:
* `cp`
* `mv`
* `rm`
* `wc`
* `ls -l` (for inspecting permissions)

---

## 2. Brief Explanation of Commands

* **`cp` (Copy):** Copies files or directories from a source location to a destination without removing the original.  
  *Example:* `cp notes.txt backup_notes.txt`

* **`mv` (Move):** Moves files or directories from one location to another, or renames them if kept in the same directory.  
  *Example:* `mv old_name.txt new_name.txt`

* **`rm` (Remove):** Permanently deletes files or directories from the file system (unlike moving them to a trash bin).  
  *Example:* `rm temp_file.txt`

* **`wc` (Word Count):** Counts and displays the number of lines, words, and bytes (characters) in a specified file.  
  *Example:* `wc -l README.md` (counts the number of lines)

---

## 3. Difference Between `>` and `>>`

Both operators are used to redirect standard output from a command into a file, but they handle existing file content differently:

* **`>` (Overwrite):** Redirects output to a file and **replaces** any existing content. If the file does not exist, it creates a new one.  
  *Example:* `echo "Hello" > file.txt` (erases previous text and writes "Hello").

* **`>>` (Append):** Redirects output to the **end** of a file without deleting existing content. If the file does not exist, it creates a new one.  
  *Example:* `echo "World" >> file.txt` (adds "World" on a new line below "Hello").

---

## 4. Observations from Inspecting File Permissions

When inspecting files using `ls -l`, each entry displays a 10-character permission string (such as `-rw-r--r--` or `drwxr-xr-x`):

1. **File Type (1st character):** `-` indicates a regular file, while `d` indicates a directory.
2. **Permission Groups (next 9 characters):** Divided into three sets of three characters representing **Owner (user)**, **Group**, and **Others**:
   * `r` = Read permission
   * `w` = Write (modify/delete) permission
   * `x` = Execute permission
3. **Default Behavior:** Newly created text files typically have read and write permissions (`rw-`) for the owner, read-only (`r--`) for the group and others, and no execute (`x`) permission by default for security.

