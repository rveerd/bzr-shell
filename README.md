README
======

A limited shell for remote access to Bazaar repositories.

Based on [this](http://stackoverflow.com/a/12993743) post.

When this script is called from a Bazaar client through an URL such as "bzr+ssh://bzr-user@bzr-server/path/to/branch", it receives two command line options:

* $1 is set to "-c";
* $2 is set to "bzr server --inet --directory=/path/to/branch --allow-writes" (for Bazaar 2.6).

The script currently runs the default shell with these options but you can use another shell, run another command or manipulate the options, such as setting another base directory.

A possible alternative is using the ForceCommand option in sshd_config, possibly together with ChrootDirectory to limit access to the file system.

