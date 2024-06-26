# UnZip files using tar
> tar -xzvf archive.tar.gz
# Zip files using tar
> tar -czvf archive.tar.gz stuff
# Search and replace using sed
> sed 's/string-to-replace/replace-with/g' filename.txt
# Convert tsv to csv
> tr '\ t' ',' < file.tsv > file.csv
# Find and exec
> find . -type f -exec ls -lh {} +
This finds all files (-f) in the current directory and then
executes (-exec) the `ls -lh` command on those files. Terminate
with `+`
# Redirecting stdout and stderr 
For redirecting stdout and stderr both
> ./test.sh &> /dev/null
For just stdout `1>` and for stderr `2>`
# Finding unique lines in file
> uniq file.txt
`-u` prints unique lines and `-d` prints all duplicated lines
`uniq` does not detect repeated lines unless they are adjacent.
Sort the input first using `sort`
# Printing ascii characters from non-ascii (binary) file
> strings data.txt
# Manipulating variable names
Edit variable names as ${var/replace-this/with-this}
> ${i/.fastq/output}
Delete shortest pattern match from start
> ${VAR#pattern}
Delete longest pattern match from start
> ${VAR##pattern} 
Delete shortest pattern match from end
> ${VAR%pattern}  
Delete longest pattern match from end
> ${VAR%%pattern} 
# Letter rotation ciphers in linux
For example, to decode or encode rot13
> tr 'A-Za-z' 'N-ZA-Mn-za-m' < data.txt
# Sending message to a server
> echo "message" | nc localhost 2000
# Remove non-printable characters from a variable in bash
> tr -dc '[[:print:]]' <<< "$var"
# Making a QR Code
> qrencode -o output.svg -t SVG -d 160 input-data
# Sorting file contents
> sort -k1 -n -t, filename.csv
`-k1` sorts by column 1, `-n` sorts numerically instead of lexicographically,
-t, sets the delimiter
