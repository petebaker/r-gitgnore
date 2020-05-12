R related .gitignore file
=============

**git** is a great version control tool.

Using *git* for version control in data analysis projects is a really
good idea. However, we really only want to put important files under
version control and not all sorts of intermediate files out even
output files which can be easily reproduced.

A *.gitignore* file specifies intentionally untracked files to
ignore. *R* and especially *latex* can produce all sorts intermediate
files and so these can be specified in the file and git will ignore
them.

Rather than getting a huge list of files when using a GUI like RStudio
or terminal command like **git status** use a *.gitignore* file like
that provided here to ignore files appropriately.

How to use .gitignore
----------

1. Download the file *DOTgitignore* to a base directory you are using
   for your data analysis project.

2. Rename the file to *.gitignore*

3. Peruse the file and comment file names or patterns you may wish to
   be tracked

4. Enjoy a rather uncluttered view of modified and staged files

Alternatively, you can 1) download *DOTgitignore* then, once
appropriately modified for your setup, store it in a commonly used
location like ~/lib, and then 2) use the *cpDOTgitignore* bash script
to copy it to the current directory.

Notes
-------

1. *.gitignore* goes in root of project and is NOT stored with git
   repo so if you clone a repository then make sure to grab your
   *.gitignore* file again

2. You may wish to add some files which are excluded here like
   *something.log* or *something.pdf*. Simply use **git add filename**
   which will track specified file. Alternatively, comment the
   pattern(s) in the file using a hash \#

3. If you need to, then it is easy to not ignore certain files like
   pdfs or docs in subdirectories. To allow a pattern in a specific
   subdirectory then create a *.gitignore* file in that directory
   using a text editor and use negate (!).  See **man gitignore**

4. You can also configure git globally so that the downloaded,
   modified file is employed unless a .gitignore is found at the root
   directory or current directory of a project. See the comments at
   the top of *DOTgitignore* for details.
