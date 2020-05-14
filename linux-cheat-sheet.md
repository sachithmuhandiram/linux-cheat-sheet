
## Dealing with Files

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
