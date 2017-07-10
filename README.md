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

#### Windows

1. Create the `C:\work` folder and the `src` folder beneath it

The isntaller should have added the appropriate environment variables, but just in case:

1. Add `GOPATH` environment variable

    1. Go to the `Control Panel -> System` and Click on `Advanced system settings`
    1. In the dialog, click the `Advanced` tab
    1. Then click on the `Encironment Variables` button
    1. Under `System Variables`, click the `New` button
    1. Enter `GOPATH` for the name, and path to your `work` folder
    1. Click `OK`

### Verify Go Installation

The easiest way to verify that Go was installed properly is to perform the following command from a terminal window:

```
go env
```

Look at the ouput and ensure that the `GOPATH` environment variable is set appropriately.