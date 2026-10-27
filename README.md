# rangerized_yazi_config

config and plugins to make che (or dual-yazi) behaves like ranger

## Motivation

Ranger is slow when loading files on NAS. Tried che (fork of dual-yazi, which is dual pane fork of yazi), it is fast. 

This repo contains my config and plugins to make operation of che more close to Ranger. It is compatible with dual-yazi and most compatible with yazi (just dual-pane operation may not work).

## Intro

Not aim to achivie all core behaviors of Ranger. In stead, three main goals are targeted.  
1. Ranger like keymap with minor tweaks to accomandate Yazi's functions.
2. Script to implement open function in Ranger. Let user input script name, pass selected files or cursor hovered file to the script as arguments, run the script and return back to Yazi. Yazi can start a shell but it cannot autocomplete cmd. There is no need to reinvent wheels given there are so many powerful tools in Bash and Python. Starting a Bash session and prefilling it with arguments is the simplest and best solution.  
3. Open shell in Yazi, let user run cmd and return to Yazi.
4. Universal confirm plug to let Yazi ask user to confirm for any cmd they feel risky. In my case, I let Che to ask confirmation for quit, copy_to, and move_to.

## Prerequisite:

Yazi, I personally prefer dual pane FM, so che or dual-yazi are my choice.  
Kitty terminal. Kitty has convienent function to prefill bash with text. Implementing this in standard Bash is not easy and not very elegant.  

## Install

Copy content under che to Yazi or equivalent's config folder. 

In kitty's config file, add following:
allow_remote_control yes

## Usage

Press "r", "r" to open a kitty window on top of che with prefilled selected files. 

Press "r", "b" to open a kitty window for user to run cmd.

Press "q", "F5", "F6", che will ask user to confirm first.

Done
