# Linux Commands I Have Learned

My notes on the Linux commands I use, each with a one-line explanation in my own words and an example.

## date
**What it does (my words):** Prints the current date and time.

**Example:**
`date` prints `Sat Oct 17 10:03:52 WAT 2026`

## uptime
**What it does (my words):** Shows the current time and how long the computer has been up and running.

**Example:**
`uptime` prints `10:09:40 up 1:12, 1 user, load average: 0.00, 0.00, 0.00`

## df
**What it does (my words):** Checks how much disk space is used and how much is free.

**Example:**
`df` displays:

```
Filesystem     1K-blocks      Used   Available Use% Mounted on
/dev/sdd      1055762868   2905560   999153836   1% /
rootfs           3030304      3396     3026908   1% /init
none             3035432         0     3035432   0% /dev/shm
```

## free
**What it does (my words):** Checks how much memory (RAM) is used and how much is free.

**Example:**
`free` displays:

```
               total        used        free      shared  buff/cache   available
Mem:         6070864      473584     5547600        4160      192124     5597280
Swap:        4194304           0     4194304
```

## exit
**What it does (my words):** Closes the current terminal session.

## pwd
**What it does (my words):** Prints the directory I am currently in.

**Example:**
`pwd` prints `/mnt/c/Users/LENOVO/Downloads`

## cd
**What it does (my words):** Changes directory. On its own, it takes me back to my home directory.

**Example:**
`cd playground` moves me into the `playground` folder.

## cd ..
**What it does (my words):** Moves me one step back, to the parent directory.

**Example:**
`cd ..` from `.../Downloads/playground` puts me in `.../Downloads`.

## file
**What it does (my words):** Describes what kind of thing a file is.

**Example:**
`file playground` prints `playground: directory`

## less
**What it does (my words):** Lets me view a text file's content one screen at a time. Press `q` to quit.

**Example:**
`less LMMD.docx`

## ls
**What it does (my words):** Lists the files and folders in the current directory.

**Example:**
`ls -l` lists them in long format.

### Common `ls` options

| Option | What it does |
|--------|--------------|
| `-a` | Lists all files, including hidden ones (dot files) |
| `-A` | Lists almost all files (leaves out `.` and `..`) |
| `-F` | Adds a marker after names: `/` for folders, `*` for executable files |
| `-h` | Shows sizes in human-readable format (with `-l`) |
| `-r` | Shows results in reverse order |
| `-S` | Sorts by file size |
| `-t` | Sorts by modification time |

## cp
**What it does (my words):** Copies a file or directory to another place.

**Example:**
`cp /mnt/c/Users/LENOVO/Downloads/README.md ~/linux-commands/` copies my README into the `linux-commands` folder.

## mv
**What it does (my words):** Moves a file or folder somewhere else, or renames it if the destination is a new name.

**Example:**
`mv money ego` renames the file `money` to `ego`.
`mv dir1/ego .` moves `ego` out of `dir1` into the folder I'm standing in.

## mkdir
**What it does (my words):** Creates a new directory (folder).

**Example:**
`mkdir ~/linux-commands` creates a folder called `linux-commands` in my home directory.

## touch
**What it does (my words):** Creates a new, empty file.

**Example:**
`touch money` creates an empty file called `money`.

## rm
**What it does (my words):** Deletes a file or folder.

**Example:**
`rm money/ego` deletes the file `ego` from `money`.

## ln
**What it does (my words):** Creates a hard link or a symbolic link to a file.

### Common options for `cp`, `ls`, `mv` and `rm`

| Option | What it does |
|--------|--------------|
| `-a` | (`cp`) Copies everything, keeping attributes, ownership and permissions |
| `-i` | Asks before overwriting or deleting an existing file |
| `-r` | (`cp`) Recursively copies folders and their contents |
| `-u` | (`cp`, `mv`) Only copies or moves files that are new or newer than the destination |
| `-v` | Shows messages about what is being done |
| `-f` | Forces the action without asking, overriding `-i`. Often used with `rm` |

> Note: some options mean different things for different commands. For example, `ls -a` lists hidden files, while `cp -a` copies with all attributes.

---

## Keyboard shortcuts

| Shortcut | What it does |
|----------|--------------|
| `Ctrl+C` | Cancels the process that is currently running |
| `Ctrl+Shift+C` | Copies highlighted text in the terminal |

---

## Wildcards

| Wildcard | What it matches |
|----------|-----------------|
| `*` | Any characters |
| `?` | Any single character |
| `[characters]` | Any character that is in the set |
| `[!characters]` or `[^characters]` | Any character that is not in the set |
| `[[:class:]]` | Any character that belongs to the given class |

### Wildcard examples

| Pattern | What it matches |
|---------|-----------------|
| `g*` | Any file starting with `g` |
| `b*.txt` | Any file starting with `b` and ending with `.txt` |
| `Data???` | Any file starting with `Data` followed by exactly three characters |
| `[abc]*` | Any file starting with `a`, `b` or `c` |
| `BACKUP.[0-9][0-9][0-9]` | Any file starting with `BACKUP.` followed by three digits |

### Character classes

| Class | What it matches |
|-------|-----------------|
| `[:alnum:]` | Any letter or number |
| `[:alpha:]` | Any letter |
| `[:digit:]` | Any number |
| `[:lower:]` | Any lowercase letter |
| `[:upper:]` | Any uppercase letter |

### Class examples

| Pattern | What it matches |
|---------|-----------------|
| `[[:upper:]]*` | Any file starting with an uppercase letter |
| `[![:digit:]]*` | Any file not starting with a number |
| `*[[:lower:]123]` | Any file ending with a lowercase letter or the numbers 1, 2 or 3 |

---

## Command Discovery & Types

### type
**What it does (my words):** Prints the type of a command, e.g., executable programs, builtins, shell functions, or aliases.

### which
**What it does (my words):** Prints where a command script or program lives inside the system.

### help
**What it does (my words):** Displays helpful information about a command if it is a valid shell builtin.

### man
**What it does (my words):** Short for manual; used to get the complete arguments and manuals that can be used with a command.

### apropos
**What it does (my words):** Displays a list of appropriate commands matching a keyword description.

### info
**What it does (my words):** Displays an advanced, hyperlinked command info entry.

### whatis
**What it does (my words):** Close to man, but instead of showing the full manual page, it displays a single-line summary of what a command does.

### alias
**What it does (my words):** The magic word used to create custom shortcuts for long commands so you can run them with shorter words.

---

## Advanced Text Processing & Redirection

### cat
**What it does (my words):** Short for concatenation; it is used to write about anything, view files, or store text into an existing file.

### sort
**What it does (my words):** Used to arrange output data in a desired alphanumerical pattern.

### uniq
**What it does (my words):** Short for unique; used to remove duplicate lines sitting right next to each other in a file or stream.

### grep
**What it does (my words):** Used to print out words or lines that match a specified text pattern within a file.

### wc
**What it does (my words):** Word count; used to display the total number of lines, words, and byte counts of a specified file.

### head
**What it does (my words):** Used to display the first 10 lines of files within a directory by default unless a specific number is specified.

### tail
**What it does (my words):** Used to display the last 10 lines of files within a directory by default unless a specific number is specified.

### tee
**What it does (my words):** Does two things at the same time: copies the original stream data and stores it into a file while still sending it to the screen.

### echo
**What it does (my words):** Displays a given parameter or string back in many different patterns. Use man to check for more advanced flags.

### clear
**What it does (my words):** Clears the active terminal screen display.

### history
**What it does (my words):** Used to view past command history that has been saved in the command buffer.

---

## Users, Groups & Administration Permissions

### id
**What it does (my words):** Displays the IDs of users, groups, and others.

### chmod
**What it does (my words):** Changes file system permissions for users, groups, and others by the file owner or superuser.

#### Permission Reference Chart

| Octal | Binary | File Mode |
|-------|--------|-----------|
| **0** | 000    | `---`     |
| **1** | 001    | `--x`     |
| **2** | 010    | `-w-`     |
| **3** | 011    | `-wx`     |
| **4** | 100    | `r--`     |
| **5** | 101    | `r-x`     |
| **6** | 110    | `rw-`     |
| **7** | 111    | `rwx`     |

### umask
**What it does (my words):** Used to set default permissions for a new file that will be created on the next prompt.

### su
**What it does (my words):** Substitute user; allows you to switch your terminal session identity to another user.

### sudo
**What it does (my words):** Substitute user and run for only the current command on a prompt, then return back to your normal user account.

### chown
**What it does (my words):** Changes who owns a file or directory for a specific user, group, or others.

### usermod
**What it does (my words):** Modifies an existing user account's properties and groups.

### passwd
**What it does (my words):** Changes or updates a user's password.

---

## Processes, Jobs & Signal Control

### ps
**What it does (my words):** Displays a quick snapshot of tasks and processes that are currently running.

### top
**What it does (my words):** Displays live, running tasks and system processes that dynamically update every 3 seconds.

### jobs
**What it does (my words):** Displays the active background processes that you created in the current shell session.

### bg
**What it does (my words):** Resumes a stopped process in the background and returns you to the prompt.

### fg
**What it does (my words):** Runs a process and brings the tasks running in the background forward onto the screen.

### kill
**What it does (my words):** Sends a specific control signal to terminate an individual running task.

### killall
**What it does (my words):** Sends a signal to terminate all running tasks of a specific program name at once.

### nice
**What it does (my words):** Lets you prioritize a task before it starts running.

### renice
**What it does (my words):** Reprioritizes the execution level of a process that is already running.

### shutdown
**What it does (my words):** Shuts down the system from the terminal with arguments to reboot, halt, and more.

---

## Advanced Keyboard Navigation Shortcuts

| Shortcut | What it does |
|----------|--------------|
| `Ctrl+A` | Moves the cursor back to the beginning of the line |
| `Ctrl+E` | Moves the cursor forward to the end of the line |
| `Ctrl+T` | Exchanges the character on the cursor with the preceding character |
| `Ctrl+U` | Kills all commands on the terminal line (deletes text as it copies them) |
| `Ctrl+Y` | Yanks (pastes) the text back from the kill ring |
| `Alt+T`  | Exchanges the word on the cursor with the next word preceding it |
| `Alt+F`  | Moves the cursor forward one word |
| `Alt+B`  | Moves the cursor backward one word |

