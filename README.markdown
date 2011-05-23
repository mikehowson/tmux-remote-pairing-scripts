## Tmux remote pairing scripts

Just a set of scripts to help setup, attach to and shutdown a tmux
session for remote rails pairing over ssh using VIM.

## Requirements

* Tmux
* Rails
* VIM
* Rspec
* Spork/Guard

## Installation

Copy the script files to /usr/local/bin or any other location you prefer
thats on the path.

## Usage

The host user starts the session from the rails project folder using tmux-start. This will create tmux
server session with four windows:-

1. VIM - The coding window
1. Server - The rails server running on port 3000
1. Bash - A general usage bash shell
1. Spork - A spork session to autorun the specs
