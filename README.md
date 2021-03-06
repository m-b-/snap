# Simple and Natural Archiver for the Poor
Snap take a snapshot of the current directory.
By default, it is saved in `basename $PWD`, but
this can be adjusted with the content of `$PWD/.snap`.

Snapshot for a project `$p` are taken in `$HOME/.snap/$p/`,
and are named after current timestamp. After copying,
`$HOME/.snap/$p/polish` polish may be called if it's executable.

* -l : list all the version for current directory
* -v : verbose
* -d : diff with latest snapshot

Every thing else is sent to potential polish call.

# polish.git
File `polish.git` commit and push all the changes.

With simple naming convention, one may even be able to
extend `polish.git` to do branching. For instance, by
appending `.somebranch` the name of the project, read
from `$PWD/.snap`, polish file may detect the branch
on which it should commit the change.
