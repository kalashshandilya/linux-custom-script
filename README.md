# *Linux Custom Script*
A Linux custom script is a set of instructions written in a scripting language, typically Bash (Bourne Again SHell), but it could be another scripting language like Python or Perl. Custom scripts are created by users to automate tasks, perform specific functions, or carry out a sequence of commands. These scripts are tailored to meet the specific needs and requirements of the user or system administrator.

# Code explanation:-
## Command Line Arguments Handling:
This block checks the first argument provided when running the script ($1) and selects the appropriate case based on the value of $1. The script is designed to handle different commands like cpu, memory, user, file, --help, and --version.

## CPU Command:
If the first argument is cpu, this block checks the second argument ($2) to determine the specific subcommand. If $2 is getinfo, it executes the lscpu command to display CPU information. If $2 is anything else, it prints an error message indicating an unknown CPU command.

# Memory Command:
Similar to the CPU command, this block handles the memory command. If the subcommand is getinfo, it executes free -m to display memory information. Otherwise, it prints an error message for an unknown memory command.

# User Command:
For the user command, it checks if the subcommand is create or list. If it's create, it checks whether a username is provided ($3), creates the user using useradd, and provides feedback. If it's list, it lists all users or only those with sudo privileges based on the presence of --sudo-only. Otherwise, it prints an error for an unknown user command.

# File Command:
For the file command, if the subcommand is getinfo, it checks if a filename is provided ($3). If so, it uses stat to display file information. If not, it prints an error for a missing filename. For any other file subcommand, it prints an error for an unknown file command.

# --help Option:
If the script is called with --help, it prints a help message providing information about how to use internsctl.

# --version Option:

If the script is called with --version, it prints the current version of internsctl.

# Unknown Command Handling:
If the provided command doesn't match any of the recognized commands, it prints an error message indicating an unknown command.

This script is a simple command-line utility that allows users to query information about the CPU, memory, users, and files on a system, along with providing options for help and version information.

# Output images

![image](https://github.com/kalashshandilya/linux-custom-script/assets/81811583/2f529e2b-87de-4cdd-b468-4073d32ee757)


![image](https://github.com/kalashshandilya/linux-custom-script/assets/81811583/597bfe91-2892-417d-a053-d4c151a59eb0)


![image](https://github.com/kalashshandilya/linux-custom-script/assets/81811583/b19be03e-bfc4-48dd-af6a-3f16e6c64185)


![image](https://github.com/kalashshandilya/linux-custom-script/assets/81811583/f0e0a353-ecea-4bd4-8fe9-14a29d1e4bcb)




