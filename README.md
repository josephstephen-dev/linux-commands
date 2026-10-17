## date
**What it does (my words):** Prints out the currrent date including the time.

**Example:**
`date` prints `Sat Oct 17 10:03:52 WAT 2025`

## uptime
**what it does (my words):** Prints out the date and time for how far long the system/computer has been up and running.

**Example:**
`uptime` prints `10:09:40 up 1:12, 1 user, load average: 0.00, 0.00, 0.00`

## df
**what it does (my words):** This is used to check the current amount of free disk space.

**Example:**
`df` displays:

` Filesystem		1k-blocks	    Used	 Available		Use%	Mounted on `
` /dev/sdd       1055762868   2905560     999153836        1%    / `
` rootfs            3030304      3396       3026908        1%    /init `
` none              3035432         0       3035432        0%    /dev/shm `

## free
**what it does (my words):** Checks the amount of free space in the memory (RAM).

**Example:**
`free` displays:
`               total        used        free      shared  buff/cache   available`
`Mem:         6070864      473584     5547600        4160      192124     5597280`
`Swap:        4194304           0     4194304`

## exit
**what it does (my words):** Closes the entire terminal.

## pwd
**what it does (my words):** Prints current working directory.

**Example:**
`pwd` prints `/mnt/c/Users/LENOVO/Downloads`

## cd/cd ..
**what it does (my words):** Changes directory back to the home directory and one step backward respectively.

## CTRL+SHIFT+C
**what it does (my words):** To cancle a working process.

## file
**what it does (my words):** To describe a file's content.

**Example:**
`file playground` prints `playground: directory`

## less
**what it does (my words):** Views text file's content.

## ls
**what it does (my words):** Lists files and folders under the current directory.

**Common ls arguments**:
`-a` prints all files including hidden files such as dot files.
`-A` lists almost all files.
`-F` indicator for both files and folders with * and / symbol respectively.
`-h` display results in human readable format.
`-r` display the reverse order of files.
`-S` sort results by file size.
`-t` sort results by modification time.

## cp
**what it does (my words):** copies a specified file or directory.

## mv
**What it does (my words):** Moves a file or folder somewhere else, or renames it if the destination is a new name.

**Example:**
`mv money ego` renames the file `money` to `ego`.
`mv dir1/ego .` moves `ego` out of `dir1` into the folder I'm standing in.

## mkdir
**what it does (my words):** Creates a new directory/folder.

## touch
**what it does (my words):** Creates a new file.

## rm
**What it does (my words):** Deletes a file or folder.

**Example:**
`rm money/ego` deletes the file `ego` from `money`.

## ln
**what it does (my words):** Creates a hard or symbolic link.

**Common cp, ls, mv, rm arguments**:
`-a` copy all files/folders including all their attributes, ownerships and permissions.
`-i` prompts the user before overwriting an existing file.
`-r` recursively copy folders and their contents.`
`-u` used to copy large numbers of files while skipping files that don't need to be copied.
`-v` displays informative messages as the copy is performed.
`-f` perform an action with force, overriding the -I option. Sometimes used with the rm command.

**Wildcards**
`*` matches any character.
`?` matches any single character.
`[characters]` matches any character that is a member of the set characters.
`[!characters] or [^characters]` matches any characters that is not of the set characters.
`[[:class:]]` matches characters that is a member of the specified class.
`g*` matches any characters starting from letter g.
`b* .txt` any character beginning with b, followed by any characters and ending with .txt.
`Data???` any file beginning with Data, followed by exactly three characters.
`[abc]*` any file beginning with either a, b or c.
`BACKUP. [0-9][0-9][0-9]` any file beginning with BACKUP. Followed by three numbers.

**Classes**
`[:alnum:]` matches any alphanumeric characters.
`[:alpha:]` matches any alphabetic characters.
`[:digit:]` matches any numeral.
`[:lower:]` matches any lowercase letter.
`[:upper:]*` any file beginning with uppercase letters followed by any character.
`[![:digit:]]*` any file not beginning with a number.
`*[[:lower:]123]` any file ending with lowercase letter or the numerals 1, 2, or 3.
