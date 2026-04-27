WSL2 + Ubuntu Setup Guide (Windows to Linux Bash)
From Beginner to Developer Setup

This guide explains how to run a full Linux (Bash) environment inside Windows using WSL2. No dual boot or heavy virtual machines are required.

1. What is WSL?

WSL (Windows Subsystem for Linux) is a feature that allows you to run a Linux environment directly inside Windows.

Simple idea:
Run Ubuntu inside Windows using a terminal.

Why WSL2 instead of WSL1?
Uses a real Linux kernel
Better performance and speed
Supports Docker and modern development tools
Provides an environment similar to production systems
2. Install WSL (One Command)
Step 1

Open PowerShell as Administrator

Step 2

Run the following command:

wsl --install
What this command does:
Enables WSL
Installs Ubuntu
Sets WSL2 as default

After this, your system will restart.

If You Get an Error (Virtualization Issue)

If you see an error like:

WSL2 is not supported on this machine

Follow the steps below.

3. Enable Virtualization (BIOS)
Steps:
Shut down your laptop
Turn it on and immediately press ESC
Press F10 to enter BIOS
Navigate to:
System Configuration → Virtualization Technology
Set it to Enabled
Save and Exit using F10
4. Install WSL Core Components (Manual Fix)

Open PowerShell as Administrator and run:

wsl --install --no-distribution

Restart your system after this step.

5. Install Ubuntu

After restart, run:

wsl --install -d Ubuntu

Ubuntu will be downloaded and installed automatically.

6. First-Time Setup

When Ubuntu launches:

Create a username
Create a password (input will be hidden)

You are now inside a Linux environment.

7. Verify Installation

Run the following command:

bash --version

If a version is displayed, the installation is successful.

8. Access Windows Files from Linux

Windows drives are mounted under /mnt.

cd /mnt/c

Example:

cd /mnt/c/Users/YourUsername/Desktop

This allows file sharing between Windows and Linux.

9. Basic Bash Commands
List files and directories
ls
ls -l
ls -a
Show current directory
pwd
Change directory
cd folder_name
cd ..
cd ~
10. Practice Task

Try the following commands:

mkdir practice_folder
cd practice_folder
touch file.txt
echo "WSL is awesome" > file.txt
cat file.txt
pwd
ls

If these commands work correctly, you understand the basics.

Pro Tips
Use Visual Studio Code with WSL for best workflow
Remember the /mnt/c path for Windows files
Practice Linux commands regularly
Use this environment for Python, Node.js, and development tools

Summary
WSL2 allows Linux to run inside Windows
Installation is simple and quick
Ubuntu is the default distribution
Ideal for development environments
Bash basics are essential
Bonus

If this guide helped you, consider starring the repository and sharing it with others.
