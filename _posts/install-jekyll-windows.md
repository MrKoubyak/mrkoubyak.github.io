# Create Jekyll env. on Windows

## Linux on Windows (WSL)
The Windows Subsystem for Linux (WSL) lets developers install a Linux distribution (such as Ubuntu, OpenSUSE, Kali, Debian, Arch Linux, etc) and use Linux applications, utilities, and Bash command-line tools directly on Windows, unmodified, without the overhead of a traditional virtual machine or dualboot setup.

### Prerequisites
You must be running Windows 10 version 2004 and higher (Build 19041 and higher) or Windows 11 to use the commands below. 

### Install
Open PowerShell or Windows Command Prompt in administrator mode by right-clicking and selecting "Run as administrator", enter the wsl --install command, then restart your machine.
This command will enable the features necessary to run WSL and install the Ubuntu distribution of Linux. 

```bash
wsl --install
```

## Install Ruby on Ubuntu
Using the built-in apt package manager offers the fastest and easiest way to install Ruby on Ubuntu

1. Update & Upgrade the system repositories
```bash
sudo apt update && sudo apt upgrade -y
```
Then update components for WSL2
```bash
sudo apt install build-essential
```

2. Use the following command to install Ruby:
```bash
sudo apt install ruby ruby-dev
```

3. When prompted, type Y and press Enter to confirm the installation.

4. Once the installation is complete, verify it by checking the current version of Ruby:
```bash
ruby --version
```
5. Update your Ruby gems
```bash
sudo gem update
```

## Install Jekyll on Unbuntu
1. Install Jekyll
```bash
sudo gem install jekyll bundler
```

2. Check your Jekyll version:
```bash
jekyll -v
```

## Connect Visual Studio Code with Ubuntu
Visual Studio Code, along with the WSL extension, enables you to use WSL as your full-time development environment directly from VS Code. 
You can:
- develop in a Linux-based environment
- use Linux-specific toolchains and utilities
- run and debug your Linux-based applications from the comfort of Windows while maintaining access to productivity tools like Outlook and Office
- use the VS Code built-in terminal to run your Linux distribution of choice

1. Install Visual Studio Code
2. Install the Remote Development extension pack (https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack). This extension pack includes the WSL extension, in addition to the Remote - SSH, and Dev Containers extensions, enabling you to open any folder in a container, on a remote machine, or in WSL.

To open a project from your WSL distribution, open the distribution's command line and enter: `code .`

## Install GIT
Git comes already installed with most of the Windows Subsystem for Linux distributions, however, you may want to update to the latest version. You also will need to set up your git config file.

for the latest stable Git version in Ubuntu/Debian, enter the command:
```bash
sudo apt-get install git
```
