# Welcome to the Go Course!

## Preparing for the Course

### Installing Go

The first step is to download and install Go [here](https://golang.org/dl/)

The most important part of installing Go is setting up the `$GOPATH` environment variable. You can set this variable to whatever folder you wish, but it must have a child `src` folder beneath it. For the purposes of this course, we will use the folder `work`.

#### Mac

1. Create the `~/work` folder and the `src` folder beneath it
1. In the `~/.bash_profile` file, add the following lines:

```
export GOPATH=$HOME/work
export PATH=$PATH:$GOPATH/bin
```

**NOTE:** If you are using a Nordstrom Mac, you will need to change your default shell from `KSH` to `Bash` via the following command:

```
chsh -s /bin/bash
```

After entering your password, close all of your terminal instances and re-start the terminal console.

#### Windows

1. Create the `C:\work` folder and the `src` folder beneath it

The installer should have added the appropriate environment variables, but just in case:

1. Add `GOPATH` environment variable

    1. Go to the `Control Panel -> System` and Click on `Advanced system settings`
    1. In the dialog, click the `Advanced` tab
    1. Then click on the `Environment Variables` button
    1. Under `System Variables`, click the `New` button
    1. Enter `GOPATH` for the name, and path to your `work` folder
    1. Click `OK`

### Workspace

The workspace is defined first by the location pointed to by `GOPATH`. Beneath the `src` folder is where projects are located.

Usually, to conform to best practices, beneath the `src` folder are the names of the organizations where the code is stored. Typically, these are SCMs, like `github.com`.

Beneath that folder is the name of the account owner for the SCM. For example: `nordstrom` or your own name.

And finally, the last folder is the Go project folder.

```
$HOME/work                          // The main source folder (GOPATH)
    |
    |-- 📂 src
        |
        |--  📂 bitbucket.org
            |--  📂 nordstrom
                |-- order-guard     // Location of order-guard repo
        |-- 📂 github.com
            |--  📂 andrewlader
                |-- go-course       // Location of go-course work
```

### Verify Go Installation

The easiest way to verify that Go was installed properly is to perform the following command from a terminal window:

```
go env
```

Look at the ouput and ensure that the `GOPATH` environment variable is set appropriately.
### Class IDE

<img src="https://github.com/AndrewLader/go-course/blob/master/images/vscode.PNG" width="241" test="VSCode" />

For this course, the IDE of choice is Visual Studio Code, which can be downloaded from [here](https://code.visualstudio.com/download/)

#### Go Extension Plugin

Once this has been installed, install the `Go Extension` plugin using the following steps. Make sure you pick the one with over 900K downloads.

<img src="https://github.com/AndrewLader/go-course/blob/master/images/go-plugin.png" width="290" test="Go Plugin" />

1. Launch VS Code Quick Open (`Command + P` on a Mac, or `Ctrl + P` on a Windows machine)
1. Type the following command and press `Enter`

```
ext install Go
```

You may be told to reload VS Code.

#### Configure Go Tools

Once the plugin has been installed, it is time to install some additional Go tools to help with editing.

1. Launch the Command Palette (`Command + Shift P` on a Mac, or `Ctrl + Shift + P` on Windows)
1. Type `Go Install`. The option `Go: Install/Update Tools` should be visible.
1. Select this option, and wait while all of the Go tools are installed
