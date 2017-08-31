# Learn command line

Please follow and complete the free online [Command Line Crash Course
tutorial](https://web.archive.org/web/20160708171659/http://cli.learncodethehardway.org/book/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. Each "chapter" focuses on a command. Type the commands you see in the _Do This_ section, and read the _You Learned This_ section. Move on to the next chapter. You should be able to go through these in a couple of hours.

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

> > **show current working directory:** pwd
> > **create a directory:** mkdir[dir]
> > **delete a directory:** rmdir[dir] (if empty) or rm -R [dir] (if directory not empty)
> > **create a file using touch:** touch [file]
> > **deleting a file:** rm [file] or rm -i[file] with confirmation
> > **renaming a file:** mv [file] [new filename]
> > **listing hidden files:** ls -a
> > **copying a file from one directory to another:** cp [file] [dir]
> > **pushing output to a file to a file:** > [file]
> > **changing directory:** cd[dir]
> > **last command written:** up arrow
> > **auto-fill:** tab

---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`  
`ls -a`  
`ls -l`  
`ls -lh`  
`ls -lah`  
`ls -t`  
`ls -Glp`  

> > **ls:** lists the files and directory in current directory
> > **ls -a:** lists all files including hidden ones
> > **ls -l:** displays files in long format
> > **ls -lh:** displays in long format and uses unit suffixes for size of file 
> > **ls -lah:** displays all of the files, including hidden, using unit suffixes in long format
> > **ls -t:** displays time modified files first before sorting by alphabetical order
> > **ls -Glp:** Enables color output, in long format, with a /after the directories

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > **ls -d:** displays only directories
> > **ls -R:** displays subdirectories
> > **ls -t:** displays newest files first
> > **ls -c:** displays files by timestamp
> > **ls -r:** displays files in reverse order

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > Xargs is a command line tool that reads data from a standard input (stdin) and executes the command supplied to it. It is often used in combination with a find command for files with a certain string pattern and then pipe those results as input to a xarg command which then does something else with them. You can also use a xarg command to find directly. I'll need to play around with this tool to wrap my head around how it works.

> > **Finding a files then piping into a xarg command which lists the results:** find ./[dir] -name "*[string pattern]" -print0 | xargs -0 ls

$ xargs find -name "*.txt" - which will find all of the files with .txt as an extension in that directory

 

