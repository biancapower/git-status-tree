[![Build Status](https://travis-ci.org/knugie/git-status-tree.png?branch=master)](https://travis-ci.org/knugie/git-status-tree)

git-status-tree
=============================================

The tree command (http://mama.indstate.edu/users/ice/tree)
recursively lists directories and files like that:

    $ tree --dirsfirst
    .
    ├── bin
    │   ├── git-status-tree
    │   ├── install
    │   └── uninstall
    ├── lib
    │   ├── bash_color.rb
    │   ├── node.rb
    │   └── nodes_collection.rb
    ├── src
    │   ├── git_status_tree.rb
    │   └── git-status-tree.rb
    ├── test
    │   ├── node
    │   │   ├── test_node_attributes.rb
    │   │   ├── test_node_children_error.rb
    │   │   ├── test_node_class.rb
    │   │   ├── test_node_create_from_string.rb
    │   │   ├── test_node_instance.rb
    │   │   └── test_node_name_error.rb
    │   ├── nodes_collection
    │   │   ├── test_nodes_collection_class.rb
    │   │   └── test_nodes_collection_instance.rb
    │   └── test_git-status-tree
    ├── DELETEME.txt
    ├── GPL-LICENSE
    ├── LICENSE
    ├── MIT-LICENSE
    ├── README.md
    └── VERSION

The git tree command (https://github.com/knugie/git-status-tree)
also prints this kind of a tree, containing only the the files listed
by git-status. The output is colored. In order to use git-status-tree
you need to install Ruby (http://www.ruby-lang.org) and of course
Git is needed as well.

Install
------
    $ git clone https://github.com/knugie/git-status-tree.git
    $ cd git-status-tree
    $ ./bin/install

Config
------
Set the indentation as you like, default is 4.

    $ git config --global status-tree.indent <indent>


Uninstall
------
    $ cd git-status-tree
    $ ./bin/uninstall

Try it!
------
    $ echo "I need to install Ruby."
    $ git clone https://github.com/knugie/git-status-tree.git
    $ cd git-status-tree
    $ ./bin/install
    $ echo "modified" >> README.md
    $ echo "added" > test/TODO.txt
    $ rm DELETEME.txt
    $ git tree
    .
    ├── test
    │   └── TODO.txt (?)
    ├── DELETEME.txt (D)
    └── README.md (M)
