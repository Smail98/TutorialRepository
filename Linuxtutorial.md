# INTRO TO LINUX:  Intro to LINUX AND UNIX & Basic Linux Commands

### Origins of LINUX and UNIX

Unix was created in the year of 1969 by Kenneth Thompson and  Dennis Ritchie. In 1972, the operation system
saw its code rewritten in C so it could outlive its initial hardware.


In the late 1980s, Berkeley developed its own variant named the Berkeley Software Distribution, while AT&T continued 
developing Unix under the names “System III” and later “System V”. 

In the late 1980’s through early 1990’s the “wars” 
between these two major strains raged. After many years each variant adopted many of the key features of the other.
At the end System V won the "war" but ended up implementing several of BDS's features in its system.
In 1991 Linus Torvalds began developing an operating system kernel, which he named “Linux”. He managed to  produce a 
freely-modifiable and very useful operating system.

Ubuntu was developed as a free open-source Linux distribution based on Debian. It's hugely
popular for its cloud computing and supports OpenStack.

Link: https://www.ubuntu.com/

### Linux Commands

Linux terminal commands allow for a fast execution of multiple tasks on the Operating System
that would usually take a considerable amount of time if done manually in OS like Windows.
It's hugely popular with programmers and system admin because of its flexibility and freedom.
Let's take a look at some commands:

First we need to open a terminal or a shell in order to enter our commands

- **cd**: allows for a change of directory. Its the same as changing folders on Windows.
- **ls**: allows to view or "list" the content of the directory you're in.
- **find**: is used to search for a specific file.
- **cat**: allows you to display the content of a file or multiple files
- **vi**: is the most  popular text editor. It works across all platforms and 
distributions and is user-friendly. When entered with a filename, it pops up a new screen and has its own commands for 
editing. 

####Linux Permissions and commands
For security reasons, Linux divides user authorization into 2 levels: ownership and permission.

Files and directory are assigned 3 different types of owners:


- **user**: A user is the owner of the file. By default, the person who created a file becomes its owner. Hence, a user is
 also sometimes called an owner.
- **group**: A user- group can contain multiple users. All users belonging to a group will have the same access permissions 
to the file. 
- **everybody else**:Any other user who has access to a file. This person has neither created the file, nor he belongs to
 a usergroup who could own the file.
 
Every file/directory has 3 types of permissions:

- **read**: This permission give you the authority to open and read a file. Read permission on a directory gives you the 
ability to lists its content.

- **write**: The write permission gives you the authority to modify the contents of a file. The write permission on a 
directory gives you the authority to add, remove and rename files stored in the directory.

- **execute**: In linux, you need a permission in order to execute a program. You may be able to read it and modify it, 
but without the execute permission, you will be limited to read/write features.

You can see the permissions of a file or directory by typing "ls -l", this will show a code looking like this
: **-rw-rw-r--**.

Let's divide this code into 4 parts:
1. **-**: the dash at the beginning of each permission indicates that it's a file. **d** indicates that its a directory.
2. **rw-**: is the user or owner's permissions. As you can see, the permissions here are read and write only.
3. **rw-**: the second 3 characters are the group's permissions. Here too, its read and write only.
4. **r--**: is the other users' permissions. Its limited to read only.

**chmod**: allows you to change the permission of a file. Its written this way:

chmod permission filename

The permission is typically written as a number. It's a code that represents one of the possible combination of permissions.
You can find a list of permissions with its corresponding code online.

**chown**: allows you to change ownership and groups for a file or directory. It's written this way:

chown user filename

- To change a user and a group:

chown user:group filename

- To change a group:

chgrp group_name filename