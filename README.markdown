## Tmux remote pairing scripts

Just a set of scripts to help setup, attach to and shutdown a tmux
session for remote rails pairing over ssh using VIM.

## Requirements

* Tmux
* Rails
* VIM
* Rspec
* Spork/Guard

You will also need a /var/tmux folder with group permissions.
Recommended route is to create a tmux group and add all users that will
be sharing the session to it and then give group permissions to the
folder.

## Installation

Copy the script files to /usr/local/bin or any other location you prefer
thats on the path.

## Usage

The host user starts the session from the rails project folder using tmux-start. This will create tmux
server session called 'pairing' with four windows:-

1. VIM - The coding window
1. Server - The rails server running on port 3000
1. Bash - A general usage bash shell
1. Spork - A spork session to autorun the specs

The remote user can then ssh into the host machine and run tmux-attach.

Once the pairing session has finished run tmux-stop to kill the session
and the server.
