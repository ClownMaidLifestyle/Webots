# Bash Commands

`pwd` - Print working directory. Shows the absolute path to your
current directory.

`ls` and `ll` - list and long list. ls is the basic version and shows
all files and directories at your current path. `ll` (alias for `ls -l`)
shows full details of files and directories including permissions.
`ls -a` can be used to show all files including hidden ones.

`cd <PATH>` - Change directory. `cd` on it's own will take you back to
your home directory. `<PATH>` can either be a relative or absolute path.

`mkdir <NAME>` - Make directory. Creates a directory with the given
name

`rm` and `rm -r` - Delete

ctrl + c - Cancel a command.

# Git Commands

In order to use Git you must first install
[Git bash](https://gitforwindows.org/). This will install a terminal
application which you provides you a bash shell. If you prefer, once 
installed all these commands can also be run from a powershell
terminal. A GUI version of git is also available.

All git commands can be run from the terminal inside your text editor
or IDE if it has one, usually you will be able to select between using
powershell or Git Bash in the editors settings. Most good text editors
will also have built in integrations with Git which you can also use.

Below is a cheat sheet of some of the most common commands. It's
important to know and understand what these do even if you opt to use a
GUI version of git instead.

`git checkout <BRANCH>` and `git checkout -b <BRANCH>` - Used to 
switch to a different branch. The `-b` variant is used to create a
new branch and immeddiately switch to it.

`git add <PATH>` - Stage a file for commit where `<PATH>` is the
file or folder to be staged for commit. Use `.` to add all changes.

`git commit -m "COMMIT COMMENT"` - Commits staged files to the the 
local repository.

`git push` and `git push -u origin <BRANCH>` - Pushes local commits 
to the remote repository. The `-u` variant is used when the local
branch does not exist on the remote side.

`git pull` - Pulls changes that other people have made to the remote
to your local repository. This should always be run against the
master branch before a new branch is sourced to prevent merge
conflicts down the road.

`git status` - Shows the staging status of your local repository
(i.e which files have been added using `git add`) including any
untracked files.

`git help` - Get help on git commands and a basic summary of each.
Can also be used with another git command e.g. `git help push` to
open the wiki page for that command.

# Generating SSH keys for GIT

In Order to use git will first need to generate an SSH key pair which
is used to authenticate your user to git.

1. To generate a key pair use `ssh-keygen` from the terminal.

   This will take you through a brief CLI setup wizard to create your
   key. You will be prompted for a passphrase. You may leave this blank
   if you wish by simply pressing enter at each prompt.

2. Once the key has been generated use `cat ~/.ssh/id_rsa.pub` to view
the public key that has been created. Copy this to your clipboard by
simply highlighting the terminal text.

3. You can upload the public key in the SSH key section of your account
in bit bucket.

# Notes

Relative vs Absolute paths - Relative path refers to a path given
relative to your current position in the file systems e.g
`elisa/foo/bar`. An absolute path is one given from the root of the
file system e.g. `/users/elisa/foo/bar`. Absolute paths always start
with `/` while relative ones do not.

Directory = Folder