# Missing Semester MIT CS
https://missing.csail.mit.edu/

A very useful course on CS _tools_ such as shells, vim, git, etc.

## Git lecture

### Intro
Git is a particular Version Control System
It has two major features:
- track a filetree and its files
- keep a set of metadata and references to those things

Uses:
* Who wrote a particular function in a collab?
* At what point did a certain feature stop working?
* Keep seperate parts of development seperate

Git is the de facto standard VCS

See the book 'Pro Git' for a thorough treatment
### The Data Model
Learning Git 'commands-first' is why so many people struggle with it. It is better to learn bottom-up, with the data model. 

Essentially we are concerned with creating a model for everything in one top-level directory through space and time.

Trees & Blobs (Folders and Files)
Git makes a hash of every object and uses these as unique identifiers. This way, we can have a set of pointers that refer to previous versions. A traceable thread for every piece of code

One commit:
A 'commit' is a collection of objects and their hashes, and relationships to the rest of the graph.

At a high level, Git is just a system to
1. manipulate the references
2. manipulate the tree and hashes
### Commands
`git init` creates the .git folder and prepares for the first commit of a new repository

`$git help` obv
`$git status` shows which files and changes need to be staged for a commit etc
`$git log --all --graph --decorate` **crucial** for visualizing the tree
the `master` commit is the main branch 
`HEAD` is the current 'view' into the system
`$git checkout` moves the head, rolling back or updating files and folders as needed.

`$git diff` the differences between two snapshots

`$git branch` creates a new commit, the base of a branch. Several purposes to doing this: could be testing a new feature, tracking one particular bug etc.
`$git merge` brings a branch back into the mainline
`$git mergetool` helps to resolve conflicts

### Remote and Local
Usually a cloud server like GitHub and your working machine, but could even be unrelated to github: two folders in a house, or even one machine.

`$git push` moves your local changes up to the remote, syncing them
`$git clone` gets the version from the remote
`$git fetch` not sure
`$git pull` is a combo of `$git fetch` and `$git merge`

### Advanced topics
Too many to list. Stuff like finding the original author of sth, tracking changes at a granular (char by char) level. Binary search for debugging etc.