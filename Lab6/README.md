# Administration Lab

This is a set of optional exercises, to practice some of the commands needed for system administration.  Try using the man pages for the commands suggested, and figure how to use them.  We will go over some of them in class, and you can ask questions about any of the others, in class or in the discussion forum.

These are optional, but they can be used instead of some of the other exercises or labs (especially lab 11), if you are more concerned with system administration than with being able to write shell scripts.  Being able to read scripts, and at least write simple ones, is just as important for administration, though, and most of these require scripts for the answer.
 
Please put the answers in your own "bin" directory (your ~/bin).  If the answer is a script, make sure it is readable and executable by everyone.  If just a file with the answer commands, still put it in your own bin directory, but not executable.  If it comes from the web, make sure you understand it, and that it will work on OUR server. 


1. (10 points)  Make a script to find all old, unused files, larger than 1 megabyte, starting at a directory supplied by the user (default: /tmp).  Make “old” be more than a month by default, but allow the user to change it.  Similarly make the  size be one megabyte by default, but allow the user to change it.  (Use find command.)

2. (5 points)  Find the file system layout (with the df command.)  Note where each partition or separate disk is mounted, how big it is, and how much space is left on it.  If you want more practice scripting, write a script that will show the mountpoints, and how much space is left on them.

3. (10 points) Copy a directory (and all it’s sub-directories) with tar AND with cpio.  To avoid problems with recursion (copying the same files you are creating), I suggest for testing (and default) making a directory in /tmp (with your name), and copying your home directory and it’s subdirectories into it.  Make a script for this, and allow the user to choose the source and destination directory. 
    Try to preserve the owner, permission, and creation date attributes.  Note that this is two different  scripts.

4. (5 points)  Log in remotely to newton.csmcis.net.  Can you tell which daemon is handling your login?  (Think ps and PPID.) . Write a script to show the commands to do this.  The daemon you are after is the last process owned by "root" that starts your login session going. The process it starts has the same name, but is owned by you, and finishes setting up your current session.  Note that just showing ALL running processes, or even all your own, is not sufficient.

5. (10 points)  Try to find the largest regular files in some of the partitions, either on newton.csmcis.net or (even better) on your own machine (if it’s some flavor of UNIX.)  Try using the du and sort commands.  Unless you can run as root (superuser), you won’t be able to see the sizes of all the files; try to find out what you can.  Either write a script, or describe the commands you would use to do this.  You could try to find the largest files (and maybe directories) on the whole machine, or in a particular partition (which is best), or just in your own account.  Think of this as trying to to remove some files to get more space from a full disk partition, so you might want to see the directories that contain the large files, and decide if they are very important (not to be deleted), or old, no-longer-useful files.  So just finding the largest file is not sufficient, you need to be able to find the next largest, etc, with enough information (who owns it, how old is it, when was it last used) to decide if you want to keep or delete it.  Or perhaps just compress it.
