# Command Line Interface Basics

## Terminal (on Mac)

Terminal is used to execute text-based commands that interact directly with the operating system. There are many things that we do as developers that can only be done through the command line, and learning how to use it is an essential part of being a developer.

Using the command line may seem daunting, but it's pretty straightforward once you understand the basics.

## Finding Your Terminal

You can access your terminal by navigating to your **Applications** folder and clicking on **Utilities**.

## Basic Commands

#### Help

    git help

This command lists some of the basic commands used in Git. Simply type it into the terminal and hit enter, then read the documentation that pops up.

#### Find Active User

    whoami

This command tells you the name of the active user on the device.

#### List Contents

    ls

This command will list all the folders and files within the directory you're currently in in the terminal. Terminal will begin in the root file of your device, usually named after the user. Using the `ls` command here will provide a list of whatever is in your root file. For me, it's folders like:

- Documents
- Pictures
- Applications
- Desktop

This command is incredibly useful because if you forget the available options when navigating within the terminal, it displays the list of possible options.

#### Directory Navigation

    cd

This command is used to navigate through directories within your system. Using `cd` on its own will return you always to the root folders of your system.

If you want to move **up one directory**:

    cd <directory-name>

If you don't remember the name of the directory, feel free to use `ls` first! If I wanted to navigate into my Documents folder from my root directory, I would enter `cd Documents` and hit enter. _Note that everything is case sensitive, so if your folder has a capital letter you must type a capital letter._

If you want to move **down one directory**:

    cd ..

Need to move back to the previous folder? Just back up with the above command.

**Tip**: When working in the terminal, you can hit tab to autocomplete what you're typing. For example, if I wanted to use `cd Documents`, I would type `cd Doc` and then hit tab, which will auto-fill in the remainder for the word Document.

#### Make A Folder

    mkdir <directory-name>

This lets you make a folder within your current directory. For example, if I wanted to make a folder called `Dogs` within my Pictures folder, I would `cd` into Pictures, then use `mkdir Dogs`. You can confirm it worked by using the `ls` command to see the content of the Pictures folder.

**Note**: When creating a directory, if the name of the directory is more than one word you must use quotes. If you were to do `mkdir Dog Pictures`, that would create two directories, one for Dog, and one for Pictures. If you wanted a single folder called Dog Pictures, you  need to have it in quotes, like `mkdir "Dog Pictures"`.

#### Make A File

    touch <file-name.file-type>

If you want to make a file instead, you can use the `touch` command. It's important to note that when making a file name, you must append the filename with the file type. For example, `touch hello.doc` will be a `.doc` file. If you do not provide the file type, it will default to a `.txt` file.

**Note**: the same single-word rules apply to making files as they did to creating directories. This is consistent across the terminal. This is why many developers have folders like `dog-pictures`; it's easier to navigate to from within the terminal.

#### Open

    open <path/to/file>

If you want to open a folder or file, you can use the `open` command followed by the path to the file. Alternatively, if you're already in the directory where the file is located, you can do `open <file-name>`. Otherwise, it would look something like `open Documents/Writing/hello`. This would open a file called **hello** within the **Writing** directory.

#### The Current Path

    pwd

If you've navigated pretty far into a series of nested directories, it can be helpful to see the previous path. Typing `pwd` will show you the entire path leading to where you currently are. For example, in my Documents folder, `pwd` returns `/Users/amy/Documents`.

#### Clear The Terminal

    clear
    Command + K

The terminal can start to have a lot of information on it as you go about your day and can be quite overwhelming to look at. Once you start waiting for error messages, being able to clear your terminal is very important. Do this this, simply type `clear` and hit enter, or use `Command + K`.

#### Command History

    history

Did you type a command earlier and you want to know what it was again? You can use `history` to get a list of your recent commands, going back about 15 commands. Alternatively, you can use the `arrow up` and `arrow down` keys to reshow the previous command, going back one command at a time per arrow click.

#### Get Your Computer To Speak To You

    say <whatever you want it to say>

This one is not only fun but can be very helpful for people who need more accessibility! Simply type `say <whatever you want to say>` and hit enter, then listen to your computer speak to you! Just make sure your volume is up.

#### Add Path into Terminal Prompt

##### For zsh Shells

In the root directory inside of the terminal type:

    open ~/.zshrc

##### For bash Shells

In the root directory inside of the terminal type:

    open ~/.bash_profile

In the file, I added this line:

    PROMPT='%F{cyan}%n%f %F{blue}%~%f %% '

The `%F{cyan}%n%f` added my name in cyan. The `%F{blue}%~%` added the path in blue. There are a lot of different customization options available and you can find some of them here:

(https://zsh.sourceforge.io/Doc/Release/Prompt-Expansion.html)
