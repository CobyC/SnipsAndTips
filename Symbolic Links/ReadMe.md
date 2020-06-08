**Create Symbolic Links Using Command Prompt**

Taken from [this
URL](https://www.maketecheasier.com/create-symbolic-links-windows10/#:~:text=Creating%20symlinks%20in%20Windows%20is,a%20symlink%20for%20a%20file.)

Run cmd.exe with admin privileges.

The mklink command takes arguments as:

_`mklink Link Target`_

The first path after the command is called the “Link.”
The second path is the physical file on disk and is called “Target.”

Eg: to create a symlink in the _```C:```_ drive for a text file located on the _```E:```_ drive, the command looks like this.

`mklink "C:\\Path\\Symlink_File.txt" "E:\\Real_File.txt"`

**symlinks can be made for directories too.**

To do that add the switch _`/D`_ as a parameter in the command. (make sure the folder does not already exist in the “target” drive)

`mklink /D "C:\\Path\\Symlink_Folder" "E:\\Real_Books"`

Delete a symlink by selecting the link like you would a normal file or directory and hit delete. (only the link will be removed)

Note however if you navigate to the target and hit delete the physical file will be deleted along with the symlink.
