# More Shell Scripting

1.  In Labs 8, 9 and 10 you made a command that would list the phone.txt file sorted and human-readable.  Lets use the knowledge and techniques to make two new, general scripts.  The first will add a name to the phone.txt file, the second will look up names in it.  Either one should allow you to list the whole file.  You can name the scripts (let’s call  them commands, because I want them to act like normal commands) anything you like, but it should be a clear name or abbreviation that represents their function.  (NOTE that if you want to, you can make a single script/command to do both of these functions, as long as you give good messages and instructions for using it.)

    a. The command should be well commented inside, and also give good feedback to the users when anything goes wrong.  Give a usage message if the user asks for it (a -? flag??)
    b. The default phones.txt file will be
~isaacs/class/unix.part2/phone.txt, but the user should have the option of giving his own file for  either lookup or adding.  (For the addphone command, you might even allow the user to add to more than one file at the same time.)  Consider the possibility of giving the user a list of phone directories (phone number files), and allowing the user to choose one (or more?) of them, or type in a new one.
   c. Don’t forget to check that the phone directory is readable by the user (on look-up), and writable when adding a new number.  It shouldn't need to be writable if only reading it.
   d.  The user might also want to delete a name, or change someones number, email, or  the spelling or their name.
   e. Please be careful not to erase the original phone lists – mine or yours or the users.  You might consider backups.
   f.  Make copious use of comments, and any of the shell programming constructs you can make use of.  Make up any flags you need to.

2. Change your script  from the last lab that printed out the largest of 3 numbers - make it so that  you can give it any number of numbers.  Don't forget that the numbers should be parameters, entered on the command line.

3.  Write a script that will look at the files in a directory and report on how many there are of each type: regular files, directory files, and other.  For each file, give the permissions that “other” has for that file, preferably in human-readable form (not just r, w, x).  Allow the user to choose the directory as a parameter to this script, and make sure you have permissions to read that directory.  If the user doesn't give a directory name, you could run the report on the current directory. Again, you need good comments, and good feedback to the user.  Also the users output should be well formatted.
