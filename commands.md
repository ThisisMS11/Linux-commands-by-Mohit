## Terminal Illuminator  
A program that will let use the terminal in a graphical way.

## mkdir
To create a Folder
```
mkdir folder_name
```


* parentfolder is already present in the current directory.

To create a subdirectory
```
mkdir /parentfolder/newfolder
```

To create directory in middle to two directories
```
mkdir -p /parentfolder/newparent/newchildfolder
```

To print the current working directory
```
pwd
```


To know the destination where any program is installed in ubuntu
```
whereis program_name
```
> whereis git

## ls

To list down all the folders in your current directory
```
ls
```

To show all the hidden files as well
```
ls -a
```

To show all the sub directories as well
```
ls -R
```

To show more details about
```
ls -l 
```
To combine both hidden files and more details
```
ls -la
```

## cd
To change directory
```
cd ./directory_name
```

To get out of the current directory
```
cd ..
```

## cat

To show what's inside the a file(like .txt files)
```
cat file_name
```
To copy a file data into another file
```
cat file_name > second_file_name
```

### Stuff with cat
To translate the contents of a file from uppercase to lowercase and store it in another file
```
cat file_name.txt | tr a-z A-Z > newfile.txt
```


## echo
To override the existing data of any txt file
```
echo "new_contents" > file_name
```

## man
To find the manual of any command
```
man command_name (ls,cat,echo etc.)
```

## touch
To create new files in the current directory
```
touch file_name
```

To create new files inside of a sub folder
```
touch subfolder_name/newfile.txt
```

## cp
To copy a file into another
```
cp file_to_copy_name > newfile_name
```

To copy a folder along with all the subfolders within it
```
cp -R source_folder destination_folder
```

` checkout man cp to explore more. `

## mv
To move a file from one folder into another
```
mv file_name folder_name
```

To rename a file using mv command
```
mv old_file_name newfile_name
```

To move the file as well as rename it
```
mv old_file_name ./destination_folder_name/newname.txt
```

To move one subfolder into cd
```
mv parentfolder/subfolder_name .
```


## rm
To remove a file from your folder
```
rm file_name
```

To remove a folder
```
rm -R folder_name
```

To remove a folder even if it's in user
```
rm -rf folder_name
```

## sudo (super user do)
For some commands you may require some administrative permissions.

```
sudo command_name 
```

## df
For getting information about disk space usage
```
 df
```

`for getting info in MBs df -m`

## du
For finding disk usage information about the files of the cd
```
du 
du -h  (human readable)
du -l
```

## head
To show the starting lines of your file
```
head file_name
```
To show only the first n lines 
```
head -n no. file_name
```

## tail
To show the lines from the end of the file. 
```
tail file_name
```

## diff
To show the difference of contents between two files
```
dif first_file_name second_file_name
```

## find
To find files with some specific extensions.
```
find all the files with the specified extensions
```
> find . -type f -name "*.txt"

To find out all the files in the previous directory
```
find ..
```

To find in any particular directory
```
find ./directory_name/
```

To find all the folders in the current directory
```
find . -type d
```

To find all the files that were modified x minutes ago
```
find . -type f -mmin -x
```

To find all the files that were modified before x minutes age
```
find . -type f -mmin +15
```                  
You can combine the above two together like

to return the files modified more than x minutes ago and less than y minutes ago
```
find . -type f -mmin +x -mmin -y
``` 

To search files only in the current directory
```
find . -type f -maxdepth 1
```

To find all the files that are empty in the current directory
```
find . -empty 
```

* you can explore on your own.

To find and delete files in the current directory with specified extension
```
find . -type f -name "*.txt" -exec rm -rf {} + 
```

## grep (to find the content inside of files)

To find some content in some file
```
grep "content_to_find" file_name
```

To disable case-sensitive search
```
grep -i "content_to_find" filename
```

To find out the line no
```
grep -n "content_to_find" filename
```

To find some content in all the files in the current directory

```
grep "mohit" ./*.txt
```

To find content inside subfolder files as well
```
grep -r "content" 
```
* checkout other flag man grep

## command history
To find the history of all commands
```
history 
```

To find commands commands with some specific command
```
history | grep "ls"
```


## File permissions
There are three types of permissions:-
1. Read
2. Write
3. Execute
Three types of people that deal with files
* User
* Group
* Another group like guests

To find the permissions given to these three folks respectively for any particular file
```
ls -l file_name
```

Rewriting permissions
```
chmod u=rwx, g=rx, o=r file_name
```
* u=user, g=group, o=other || r=read, w=write, x=execute

Rewriting permissions using octal numbers
Divided into three categories:
4 = read,  2 = write, 1 = execute

so if i want to give all three permissions to all three users then i can do like this:
```
chmod 777 filename
```
! 7=(4+2+1)  
you got it i know.


## chown (changing owner)
To find the current user
```
whoami
```

> In Unix-like computer OSes (such as Linux), root is the conventional name of the user who has all rights or permissions (to all files and programs) in all modes (single- or multi-user).

To change user to root or any other
```
sudo chown root file/folder_name
```
To find all the files with permissions
```
find . -perm 777
```

## regex (search on google)



## alias (shortcut forms of terminal commands)
to see all of your aliases

`bashrc is in our root directory`
```
cat ~/.bashrc
```

To add your own alias (here vim is my text editor)
```
vim ~/.bashrc
```

## keyboards shortcuts inside terminal
To move to start of command
```
ctrl + a
```
To move to end of command
```
ctrl + e
```
To remove everything after the cursor
```
ctrl + k
```

run previous command using history
```
!command_no
```

to run the last command of a specific type
```
!command_name
ex:- !find
```

to run multiple commands simultaneously
```
command_1 ; command_2; command_3;
```

## sort 
To sort the contents of a file
```
sort file_name
```
> use -r flag to reverse sort.

## ping
To check connectivity status with online servers
```
ping google.com
```

## wget 
To download files from network
```
wget download_url
``` 

To download files and rename them at the same time
```
wget -o file_name.ext download_url 
```

## top
To get info about cpu processes
```
top
```

to kill a program
```
kill program_id
```

## zip
To zip files
```
zip file_name1 file_name2 file_name3
```

To unzip
```
unzip zip_file_name.zip
```

## hostname
To know the hostname
```
hostname
```
To know the ip address of the host
```
hostname -i
```

## useradd
* if below commands require permissions use sudo command

To add new user for your system
```
useradd user_name
```
To set a password for the new user
```
passwd new_user_name
```

To  delete a user
```
userdel user_name
```

## uname
To display system information, use the uname command. Displays the operating system name as well as the system node name, operating system release, operating system version, hardware name, and processor type.
```
uname -a
```

> To find info about the operating system
```
cat /etc/os-release 
```

> To get the cpu details
```
lscpu
```


## free/vmstat
To know about the free memory
```
free
```
To know virtual memory
```
vmstat
```

## id
print real and effective user and group IDs
```
id
```
## getent
To know whether a user exists or not
```
getent group user_name
```

## lsof
To find out the names of all the open files
```
lsof
```

## nslookup
To checkout id address of particular domain name
```
nslookup domain_name
```


`netstat :- to find all the ports that are listening`

## htop
You can checkout allthe resources which are begin consumed
```
htop
```


# Explore Own Your Own
1. cut


# working with operators

## & (and)
To run in the background so that other commands that can be executed
```
ping google.com & ping amazon.com
```
the first one google.com is running in the background

## && (and and)
To run a command only when the previous command is executed
```
echo "first" && echo "second"
```

## || (or)
To run a command only when the previous command fail to execute
```
fdjkajdkfal || echo "alternative_commmand"
```

## !(not)
To handle any exceptions like
To delete all the files/folder except one
```
rm -r !(file/folder_name)
```
## >> (append)
To add some content to existing files
```
echo "new_content" >> file_name.ext
```

## mutiple commands + operators
```
echo "first" && {echo "second"; echo "third";}
```


# What are environment Variables?
These are some preadjusted paths a user can set to help the OS identify and search programs via the terminal.

# What are bash files?
These are some files that get executed whenever we open any terminal window.


| WARNING: Never execute any command without knowing what it does to avoid loses .Enjoy 😄  
| --- |





