## Note

This overview is written specifically for Mac OS X users. The information it contains applies in general, however the examples are in the context of a Mac user.

## Introduction

Most of the interactions you perform with the computer are done using programs that display windows with buttons, text fields, etc. This is known as a Graphical User Interface (GUI), however there is another interface which programmers frequently use, known as a Command Line Interface (CLI). The command line interface is purely text­driven: To perform actions, the user types in commands, and the computer shows the result of the command by printing out text.

The reason programmers use command line interfaces is that it allows them to perform very specific and complicated actions with only a few keystrokes, and can reduce repetitive tasks into a single command. There are even programs designed specifically for the command line, that may or may not have a graphical user interface counterpart.

On the Mac, we can use the Terminal application inside Applications ► Utilities to open a command line interface.

### Folder and Paths

A folder, also known as a directory, is a container for files and other folders. These are the same folders you see when you look for files using Finder. A “path” describes the location of a file or folder, including all the folders you need to go into to find it. The folders in a path are separated using a slash (“/”). A slash at the beginning indicates a path starting at the hard drive, usually represented in the Finder by a device called “Macintosh HD”. The path of the Terminal application, which is actually called “Terminal.app”, would be written /Applications/Utilities/Terminal.app.​A tilde (“~”) at the beginning of a path means the path is relative to your home folder, so your Music folder’s path is ~/Music.​Your desktop is actually a folder called “Desktop” inside your home folder, so it's path is ~/Desktop. 

A path that starts with a slash or tilde is known as an absolute path, because it specifies the full location of a file or folder. If a path doesn’t start with a slash or a tilde, it is known as a relative path. When you use the Terminal application, it has a notion of a “current working directory”, which is a folder it places at beginning of any relative path to turn it into an absolute path. By default, when you start the Terminal application, the current working directory is your home folder. That means when you write “Desktop”, it assumes you mean “~/Desktop”.

If any file or folder in a path has spaces in its name, you must either put a backslash (“\”) before the space or put quotation marks around the entire path, because spaces are used to separate multiple items in the command line interface.

### Basic Terminal Commands

The following are some very basic Terminal <b>commands</b> that will help you get started.

```pwd```       Prints the full (absolute) path current working directory. Use this if you’re unsure what the current working directory is.

```cd path```  Changes the current working directory to p​ath.​If the current working directory is your home folder and you type “c​dDesktop”​, then your current working directory becomes ​~/Desktop.​If you don’t specify p​ath,​ then it changes the current working directory to your home directory.

```ls path```  Lists the files in the folder specified by path. If you don’t specify p​ath,​then it lists the files in the current working directory.

```ls -l path``` The same as ​ls​except it prints more information about each file, including the date it was last modified.

```mkdir name``` Creates a folder (mkdir = “make directory) with the given name.

```rm name``` Deletes the file with the given name. This cannot be used to delete folders.
<b>Warning</b>: This does not move files to the Trash, it deletes them immediately and irreversibly.

```rm -r name``` Deletes the folder with the given name. The folder be empty or only contain other empty folders.

```rm -rf name``` Deletes the folder with the given name and any files and folders it contains.<b>Warning</b>: This command can cause serious damage. It’s safer to move folders to the Trash in Finder.

You can also interrupt a command by holding the Control key and typing C. This combination is abbreviated as Ctrl­C. When you type this combination, Terminal will display ^C​and interrupt the currently running command.

When entering a file name, if you enter the first few letters and press Tab, the Terminal will try to auto­complete the name. For auto­complete to work, there must be a single, unambiguous completion. If it doesn’t work, try adding a few more letters of the name.

