## Updating OS

### For debian based OS

`sudo apt update`

`sudo apt upgrade`

`sudo apt dist-upgrade`

`sudo apt autoremove`   This will remove outdated packages after upgrade.


### For redhat based OS

`yum update`


## Dealing with Files

### Checking differences between files

To check difference between two files. Following command will show just basic details.

`diff file1 file2`

To get detailed description

`diff -u file1 file2`

#### Getting changes to a file

If we have two files and want to get them their difference to a file.

`diff file1 file2 > differences.diff`

Applying changes to `file1`

`patch file1 < differences.diff`

First we **MUST** create `.diff` file as mention above and then `patch` command.

### Getting total number of lines in a file

If we have a large file and we need to get number of lines in that file :

`cat filename | wc -l`

[count number of lines in terminal output](https://stackoverflow.com/questions/12457457/count-number-of-lines-in-terminal-output)

### Getting from nth to mth row from a large file

To get specific lines from a very large file. Here this will get from line `n` to `m` and create a new file `output.txt`

`sed -n 'n,m p' filename > output.txt`

[efficient-way-to-get-n-middle-lines-from-a-very-big-file](https://stackoverflow.com/questions/20465034/efficient-way-to-get-n-middle-lines-from-a-very-big-file)

### Append date-time to a filename

`echo dateTimeFileName-"`date +"%d-%m-%Y"` `

This will make `dateTimeFileName-14-05-2020`

**Get Month as string**

`dateTimeFileName"`date +"%d%b"`".txt` Output will be `dateTimeFileName_14:May.txt`
You can add `%y` to get year.

[append-date-to-filename-in-linux](https://stackoverflow.com/questions/1795678/append-date-to-filename-in-linux)

### Changing file permission to executable

When you create a shell-script, to execute it, we need to change file permission. To do it.

`chmod +x filename.sh`
