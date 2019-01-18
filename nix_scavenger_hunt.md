# *nix Scavenger Hunt

Complete the following challenges using the command-line interface on your favorite
Unix or Linux operating system. You are welcome and encouraged to consult any
additional documentation online or in books.

Please add your answers/responses/text pastes to the document after each prompt.

Note: For some of the challenges you will need to reference files included with
this repository, so you will need to fork the repo into your own Github account
and then clone it to your development environment.

## The Challenges

### Navigating the Filesystem

* Get an idea of where you are in the operating system. Use the `pwd` command to find your "path to working directory"--your current location in the filesystem of your devbox. *Paste the output of the `pwd` command here:*
/c/Users/Nate/projects/wats1030-intro-to-unix

* Discover more about this filesystem. Use `ls` (the "list" command)to see what is in this directory. *What directories and files do you see when you run `ls`?*
challenge_files  nix_scavenger_hunt.md          README.md
LICENSE          nix_scavenger_hunt_stretch.md  super_scavengers.md

* You can use *options* to modify how a command runs. Try using `ls -alh` to see the contents of your current directory. *How are the results different when you use the `-alh` options?*
total 78K
drwxr-xr-x 1 Nate 197609    0 Jan 17 17:42 .
drwxr-xr-x 1 Nate 197609    0 Jan 17 17:41 ..
drwxr-xr-x 1 Nate 197609    0 Jan 17 17:42 .git
drwxr-xr-x 1 Nate 197609    0 Jan 17 17:42 challenge_files
-rw-r--r-- 1 Nate 197609 1.1K Jan 17 17:42 LICENSE
-rw-r--r-- 1 Nate 197609 5.7K Jan 17 17:57 nix_scavenger_hunt.md
-rw-r--r-- 1 Nate 197609  325 Jan 17 17:42 nix_scavenger_hunt_stretch.md
-rw-r--r-- 1 Nate 197609 2.8K Jan 17 17:42 README.md
-rw-r--r-- 1 Nate 197609  268 Jan 17 17:42 super_scavengers.md
``It looks like it pulls the individual files out, rather than just the folders``

* The `man` ("manual") command tells you more about how any given command works. (*WARNING:* CodeAnywhere does not support the man command. You can click the following link to complete this task: http://man.he.net/). Run `man` to see instructions about how to use `man`. Then use `man` to learn what the `a`, `l`, and `h` options mean when used with the `ls` command. *Write down what those options do?*
ls   -a, --all
              do not ignore entries starting with .
   
     -l     use a long listing format
   -h, --human-readable
              with -l, print sizes in human readable format (e.g., 1K 234M 2G)

* Commands can also take *arguments*, which are usually the names of files or locations that you want the command to work with. Try running `ls /` to see what files are in the *root* directory of the filesystem. *What files and directories do you see listed?*
bin  dev  git-bash.exe  LICENSE.txt  proc               tmp           unins000.exe  usr
cmd  etc  git-cmd.exe   mingw64      ReleaseNotes.html  unins000.dat  unins000.msg

* A Unix filesystem has a few special shortcuts to refer to specific locations. `/` indicates the *root* of the filesystem, meaning the top-most directory in the filesystem hierarchy. Use the `cd` ("change directory") command to move to the root directory. (Hint: Use `man` to look up the `cd` command if you have any issues) *Then run `pwd` and paste the output here:*
/c/Users/Nate

* Another special shortcut in Unix is the `~` location. This indicates the *user root* directory, meaning the top-most directory in the hierarchy that comes below your user account. Use `cd` to move to `~`. *Run `pwd` and paste the response here:*
/c/Users/Nate (I was in the topmost directory before)

* Change directory into the `challenge_files` directory. Use `ls` to find only the files with a `.demo` pattern. *How many files do you find?*
3

* Use the `cd` command to move "up" one directory. *Where are you in the filesystem now?*
/c/Users/Nate/projects/wats1030-intro-to-unix

* Press the up arrow on your keyboard. *What just happened?* 
It replaced my last command...like a quick use of history 

* Press the up arrow a few more times. *What do you see?*
It kept running through the last several commands...

* Run the `history` command. *What do you see?*
a list of my last (feeble attempts) of commands 
$ history
    1  is
    2  is file
    3  mkdir
    4  mkdir --help
    5  find project
    6  find creative writing
    7  cat
    8  pwd
    9  dd
   10  chkdsk
   11  fing
   12  find
   13  pwd
   14  cd challenge_files
   15  pwd
   16  pwd
   17  ls
   18  cd wats10-intro-to-unix
   19  cd wats1030-intro-to-unix
   20  cd ~wats1030-intro-to-unix
   21  pwd
   22  cd up
   23  cd ..
   24  pwd
   25  history

### Observing the System

* Discover what account you are logged into using the `whoami` command. *What username are you currently using?*
Nate

* Discover who else is on your system with the `who` command. *Are any other users using your system? If so, list them here:*
There are no others 

* How long has your system been running? Use `uptime` to see, and *paste the result here:*


* Run `ps aux` and review the results. (Hint: Use `man` to learn more about the `ps` command and options.) *How do you interpret what you see here?*
$ ps aux
      PID    PPID    PGID     WINPID   TTY         UID    STIME COMMAND
     3884       1    3884       3884  cons9     197609 18:57:43 /usr/bin/bash
    12584       1   10248       7888  cons1     197609   Jan 13 /usr/bin/vim
     6868   13640    6868      15964  cons3     197609   Jan 13 /mingw64/bin/git
     5104       1    5104       5104  cons2     197609   Jan 13 /usr/bin/bash
    10248    3424   10248       6660  cons1     197609   Jan 13 /mingw64/bin/git
     3424       1    3424       3424  cons1     197609   Jan 13 /usr/bin/bash
     4236       1   14556      14392  cons0     197609   Jan 13 /usr/bin/vim
    19168    3884   19168       9764  cons9     197609 19:05:22 /usr/bin/ps
    13640       1   13640      13640  cons3     197609   Jan 13 /usr/bin/bash
    18836       1   18836      18836  ?         197609 17:40:10 /usr/bin/mintty
     7260       1    6868       5896  cons3     197609   Jan 13 /usr/bin/vim
     9276       1    9276       9276  cons8     197609 18:18:34 /usr/bin/bash
    15708       1   15708      15708  cons6     197609 17:54:09 /usr/bin/bash
     3144       1    3144       3144  cons4     197609   Jan 13 /usr/bin/bash
    14556    1188   14556       8848  cons0     197609   Jan 13 /mingw64/bin/git
    12428    5104   12428      14576  cons2     197609   Jan 13 /mingw64/bin/git
    10840   18836   10840      18484  pty0      197609 17:40:10 /usr/bin/bash
    18800       1   18800      18800  cons5     197609 17:53:45 /usr/bin/bash
     1188       1    1188       1188  cons0     197609   Jan 13 /usr/bin/bash
     6304       1   12428      13736  cons2     197609   Jan 13 /usr/bin/vim
    19488       1   19488      19488  cons7     197609 17:54:22 /usr/bin/bash
* Run `top` and review the results. (Hint: You may need to use `ctrl-c` to get out of this app.) *How do you interpret what you see here?*
$ ps top
      PID    PPID    PGID     WINPID   TTY         UID    STIME COMMAND
    10580    3884   10580      10828  cons9     197609 19:09:40 /usr/bin/ps
     3884       1    3884       3884  cons9     197609 18:57:43 /usr/bin/bash
    18836       1   18836      18836  ?         197609 17:40:10 /usr/bin/mintty
     9276       1    9276       9276  cons8     197609 18:18:34 /usr/bin/bash
    15708       1   15708      15708  cons6     197609 17:54:09 /usr/bin/bash
    10840   18836   10840      18484  pty0      197609 17:40:10 /usr/bin/bash
    18800       1   18800      18800  cons5     197609 17:53:45 /usr/bin/bash
    19488       1   19488      19488  cons7     197609 17:54:22 /usr/bin/bashpwd

### Finding and Viewing Files

* Make sure you are in the `challenge_files` directory. Use the `*` wildcard to find all the files that have the word "credit" in the filename. *How many files did you find?*
2

* Use the `more` command to view one of the `credit_cards` files you just discovered. (Hint: Type `q` to quit viewing the file. Press the `spacebar` to page down. Use your keyboard arrows to move up/down.) *What is the date in the file you have viewed?*
(more command did not work in BAsh, date is 01-15-2015)

* Use the `find` command to search for files more effectively. Search the sub-directories under `challenge_files` to find the location of the file named `modi_laboriosam.txt`. *Where is that file located?*
./tmp/modi_laboriosam.txt

* Use the `grep` command to search for text within a file. Use `grep` on all the `.user` files in `challenge_files` to find which files contain "WA" (the abbreviation for Washington state). *How many files did you find?*
4
Binary file ./.git/index matches
Binary file ./.git/objects/pack/pack-311e7b80bfadcbb1a5255c2c827565e329960508.idx matches
./challenge_files/Britt-Erdman.user:O'Harachester, WA 37261
./challenge_files/Lissie-Strosin.user:Jewessfurt, WA 00816-7241

* Use the `-r` option of `grep` to *recursively* find the text "Waldo" hidden in a file somewhere under the `challenge_files` directory. *Paste the result showing the file and line where the word "Waldo" shows up.*
./challenge_files/serial-numbers/eaque_molestiae.txt

### Pipes and Connecting Commands

* Sometimes it's useful to output the results of a command to a text file for further analysis, reference, or processing. Try running `ls > files.txt`. Notice that the file `files.txt` was created. View that file using `more`. *What do you see in the `files.txt` file?*
* Notice that if you run `ls -alh` in the `challenge_files` directory, the files scroll by very quickly. Sometimes it would be better to get the results in a paginated format. Try running `ls -alh | more`. *Describe what you see when you run `ls -alh | more`.*
* Earlier, when you viewed the list of active processes on your devbox using `ps aux`, the list was probably really long. You can make this list more manageable by using the pipe (`|`) to filter the results of `ps` using `grep`. Run `ps aux | grep <your_username>` to see what processes are running for your specific user. *Paste the list of processes that reference your username here:*
