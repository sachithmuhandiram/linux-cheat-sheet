
## Dealing with Files

### Getting total number of lines in a file

If we have a large file and we need to get number of lines in that file :

`cat filename | wc -l`

[count number of lines in terminal output](https://stackoverflow.com/questions/12457457/count-number-of-lines-in-terminal-output)

### Getting from nth to mth row from a large file

To get specific lines from a very large file. Here this will get from line `n` to `m` and create a new file `output.txt`

`sed -n 'n,m p' filename > output.txt`

[efficient-way-to-get-n-middle-lines-from-a-very-big-file](https://stackoverflow.com/questions/20465034/efficient-way-to-get-n-middle-lines-from-a-very-big-file)
