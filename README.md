git-shell-commands
==================

My git-shell-commands -- thanks to a PlanZero post
http://planzero.org/blog/2012/10/24/hosting_an_admin-friendly_git_server_with_git-shell

Comamnds from the Aritcle
-------------------------
* addkey -- Addes a pasted OpenSSH key.  Script prompts user to paste the key.
* create -- Creates a new git repository.  Adds the ".git" extension if it is omitted.

Additions
---------
* help -- Prints the help file at login and whenever the user executes the help command.
* delete -- Deletes the specified git project.  Adds the ".git" extention is necessary.

Git Account Create
------------------
From the article, substitute "/srv/data/git" for whatever path holds git repos:
* useradd --create-home --skel /dev/null --home-dir /srv/data/git --shell /usr/bin/git-shell git
* chmod 750 /srv/data/git
* mkdir /srv/data/git/git-shell-commands
* Clone the repo to /srv/data/git/git-shell-commands

Requirements
------------
The verison of git that comes with CentOS/RedHat 6.5+ is insufficient.  You'll have to compile a newer
version of git (recommend making the RPMs), or find newere pre-compiled git RPMs.


