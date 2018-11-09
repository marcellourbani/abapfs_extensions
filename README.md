# ABAPFS extensions
Allow updates on systems older than 7.51 with [visual studio code ABAP remote filesystem extension](https://github.com/marcellourbani/vscode_abap_remote_fs)

## Installation

Import in your dev system with [ABAPGIT](https://github.com/larshp/abapGit)

## Technical details
The ABAP developement tools require ABAP objects to be locked before they can be updated. This requires stateful sessions
Eclipse works over RFC, which is stateful by default

Visual studio code works over HTTP, and needs to manage the stateful session flag.
This is handled fine in my 7.51 developer edition, but not in older systems. This enhancement implements the same mechanism in older systems

There is no need to install this in systems which handle the sessions already, but it won't cause issue if imported. It will simply (re)set the flag twice
