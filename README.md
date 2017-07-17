```
               @@@   @@@
              @@@    @@@@
             @@@     @@ @@
            @@@      @@  @@
           @@@       @@   @@
          @@@        @@    @@
         @@@         @@     @@
        @@@          @@      @@
  @    @@@           @@       @@  @ |
  |   @@@@@@@@@@@@   @@        @@ | |-
  |   @@@@@@@@@@@@   @@        @@ | \_/
\_/    @@@           @@       @@
        @@@          @@      @@
         @@@         @@     @@
          @@@        @@    @@
           @@@       @@   @@
            @@@      @@  @@
             @@@     @@ @@
              @@@    @@@@
               @@@   @@@

```

# jedit

Pronounced as it's spelled (**not** as jay-edit, etc.)

## Getting Started (development)

Want to develop or test jedit? Follow these instructions to do so!

### Prerequisites

 - Preferrably UNIX like OS (e.g. Linux, MacOS, **However, Windows users can use this too, with extra steps**)
 - ncurses
 - g++

#### Debian (or Debian based distros e.g. ubuntu)

```
sudo apt-get update
sudo apt-get install ncurses
```
And if you don't already have g++
```
sudo apt-get install g++
```

#### Other linux systems, or MacOS

Use whichever package manager you have on your operating system (e.g. pacman, homebrew)
to install the neccessary packages. They are probably named identically regardless.

#### Windows

The best way to get started on Windows is by installing the Windows subsystem for Linux. Basically this is 
a way of opening up an ubuntu shell in Windows! You can find out more about that 
[here](https://msdn.microsoft.com/en-gb/commandline/wsl/install_guide), but

> Your PC must be running a 64-bit version of Windows 10 Anniversary Update or later (build 1607+).

Once you've got the bash shell up and running, you can follow the steps for debian

### Installing for development

Now you're ready to get the development environment set up!

First, clone the repository to somewhere on your hard drive.

```
git clone https://github.com/j4cobgarby/jedit
```

Move into the root directory of the repository

```
cd path/to/repository/root
```

Clean the current build

```
make clean
```

And build for your operating system

```
make
```

Now you can simply run it

```
./jedit
```

## Built With

* g++ - The c++ compiler
* [ncurses](http://invisible-island.net/ncurses/man/ncurses.3x.html) - To do graphical stuff in a terminal

## Contributing

 1. Fork it
 2. Create a new branch for your new feature
 3. Develop this branch - comment (briefly or in detail) how it all works
 4. Push your fork
 
## How to use

Similar to vim, jedit has different modes for editing files. jedit has two modes:

 - `NORMAL`
 - `INSERT`

### NORMAL mode

When you open up jedit, you'll be in `NORMAL`. This is the mode in which you can make use of jedit's
different commands. To switch from `NORMAL` to `INSERT`, simply press `i`.

### INSERT mode

Once you're in `INSERT`, you can start writing text in the file. You may enter text just as in any
other editor. When you want to go back into `NORMAL`, press `escape`.

### NORMAL mode commands

|Key|Action|Notes|
|---|---|---|
|`x`|Quits jedit|Doesn't prompt to save. Make sure you've already saved if you want to keep what you've done.|
|`s`|Saves the current file|If you're not editing a file and instead writing a new file from scratch, jedit will open a dialog box asking for you to name your new file.|
|`i`|Enters insert mode.||

### Opening files

To open a file in jedit, you must do so when you run the program. The file name is specified as a command line argument.

```
jedit path/to/file
```

*Note at the moment, file paths can't include spaces. This is a known issue.*

### Creating new files

You can create a new file the same way you'd open one which already exists. Suppose you want to create a file called `new_file.txt`, you could do this

```
jedit new_file.txt
```

And then, once it's loaded, press `s` to create it.

Alternatively you could rely on your operating system's commands

```
touch new_file.txt
jedit new_file.txt
```

or something like that. If that doesn't work, you could always do

```
echo> new_file.txt
jedit new_file.txt
```

## Authors

* **Jacob Garby** - *Initial development* - [j4cobgarby](https://github.com/j4cobgarby)

See also the list of [contributors](https://github.com/j4cobgarby/jedit/contributors) who participated in this project.