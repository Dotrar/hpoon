# hpoon
Harpoon like functionality in the terminal

## Usage:
    hpoon [dir] [opt-name]  | store a mark, optionally with a name
    hpoon                   | retrieve the last marked file or dir
    hpoon @[name]           | retrieve marked file with name

Can only mark files and directories that exist, but can retrieve
marks that no longer exist on the filesystem

## Examples:

    cd /path/to/dir     # cd to a dir
    hpoon .             # harpoon it

    # in a different shell (ie: tmux)
    cd /new/abs/dir     # totally different dir
    cp * `hpoon`      # copy files over to the last harpooned dir

    # works on deleted files
    hpoon filename myfile           #harpoon a file with "myfile"
    rm filename
    cd /somewhere/else/entirely
    mv some_file `hpoon @myfile` # result: mv that_file /original/path/filename
`
