# Tmux Scripts

A set of native tmux scripts to autoarrange and start terminal commands in tmux windows and panes.

## Why Does This Project Matter to Me?

Don't you get tired of opening up your terminal and typing the same dozen or so commands to get your workday started? Wouldn't issuing a single tmux script command be so much easier? And wouldn't using tmux's built in scripting ablity provide a much ligher weight solution than tmux window configuration tools like tmuxinator that require extra dependencies?

## Requirements

1. tmux
2. permissions to 'chmod +x' the tmux scripts

## To Use

1. get scripts:         `git clone http://github.com/aaronhalford/tmux-scripts`
2. go to folder:        `cd tmux-scripts`
3. personalize scripts: `vim tmuxscriptname'
3. make executable:     `chmod +x tmuxscriptname`
4. run script:          `./tmux-scripts/tmuxscriptname`

You may want to move the tmux scripts to the root of your home folder so the scripts can be called by './tmuxscriptname'

## Contributions

I'm hopeful the community can share and expand upon this small repository by adding common tmux workflow setups for general git, vim, rubyonrails, node.js, and remote server work. Just ask yourself the question, "What windows and apps do I use during my workday?" And once you have an answer follow it up with a tmux script to automate those commands.

Pull requests should include a tmuxscript file that includes a commented out header:

```
# Name:                   mytmux
# Operating System(s):    Linux distros that use apt-get
# Software Dependencies:  webserver ssh, htop, vim, ncdu
# Description:            creates 10 named windows for general workday use
```

Please make sure your pull requests also include a unique script name and well commented code.

## A word on security and privacy

* Write your tmux-scripts as vanilla templates with the lowest level of detail possible.
* Your 'tmux.conf', 'zshrc', and 'bashrc' files can modify the result of a 'tmux send-keys' command. 
* Try to write your scripts to either accomodate the aforementioned defaults or explicity state deviations.
* Keep private information (ssh/ipaddresses/startupcompanynames/etc) out of your pull requests.
* Also beforewarded that tmux-scripts are essentially bash scripts that can issue sudo commands and destructive commands like 'rm -rf /' if the syntax or wrong directory is incorrectly set. 
* Any tmux-script that calls potentially destructive functions will be rewritten before a pull request is accepted.  Use cp instead of mv or rm. Don't sudo if you don't have to. And so on.
