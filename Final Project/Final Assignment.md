# Study Guide

# Question 1

## awk
Awk is a scripting language used for processing and displaying text. Awk can work with a text file or from standard output
awk + options + {awk command} + file + file to save is optional
awk '{print $1}' ~/Documents/Csv/cars.csv
awk -F: '{print NR,$1,$3}' /etc/passwd
awk 'NR > 3 { print }' /etc/passwd
## cat
The cat command is used for displaying the content of a file.
cat + option +files to display
cat todo.lst, cat ~/Documents/todo.lst cat -s ~/Documents/todo.md
## cp
cp copies files/directories from a source to a destination
cp + files to copy + destination
cp Downloads/wallpapers.zip Pictures/
cp -r ~/Downloads/wallpapers ~/Pictures/
cp Downloads/wallpapers/* ~/Pictures/
## cut
The cut command is used to extract a specific section of each line of a file and display it to the screen
cut + option + files
cut -d ':' -f1 /etc/passwd
cut -d ':' -f1,7 /etc/passwd
cut -b 1-5 usernames.txt
## grep
Grep is used to search text in given file. grep works line by line basis
grep + option + search criteria + files
grep 'dracula' ~/Documents/dracula.txt
grep -i 'dracula' ~/Documents/Books/dracula.txt
grep -v 'war' ~/Documents/books/war-amd-peace.txt
## head
The head command displays the top N number of lines of a given file
head + option + files
head ~/Documents/Book/dracula.txt head -5 ~/Documents/Book/dracula.txt head 5 ~/Documents/Book/dracula.txt
## ls
ls is used for listing the content of a given directory or the file itself
ls + option + directory to list
ls -a
ls -a ~/Pictures
ls -lR ~/Pictures
## man
man (manual) view the manual of a command
man + command
man ls
man 5 passwd
man -k file
## mkdir
mkdir is used for creating a single directory or multiple directories
mkdir + the name of the directory
mkdir wallpapers
mkdir wallpapers/ocean
mkdir ~/wallpapers/forest
## mv
mv moves and renames directories
mv + source + destination
mv Downloads/homework.pdf Documents/
sudo mv ~/Downloads/theme /usr/share/themes
mv homework.docx cis106homework.docx
## tac
The tac command is used for displaying the content of a file in reverse order
tac + option + files to display
tac todo.md tac ~/Documents/todo.md tac lab7.md
## tail
The tail command displays the last N number of lines of a given file
tail + option + file
tail ~/Documents/Book/dracula.txt
tail -5 ~/Documents/Book/dracula.txt
tail 5 ~/Documents/Book/dracula.txt
## touch
Touch is used for creating files
touch + option
touch list
touch ~/Downloads/games.txt
touch "list of foods.txt"
## tr
The tr command is used for translating or deleting characters from standard output.
Standard output | tr + option + set + set
cat file.txt | tr '. ','
cat program.py | tr "[:space:]" '/t'
cat file.py | tr -s "[:space:]" ' '
## tree
The tree command shows a list of files in a select folder
tree + folder/installation
tree -d ~
tree -a Directory/
tree -f Directory/

# Question 2

## How to work with multiple terminals open
You can work with multiple terminals by having them in different tabs or in separate panes in the same tab
You can switch between them using the arrow keys in conjunction with the tab and control/shift keys
## How to work with manual pages
Use the command man + command + name
## How to search for specific words in the manual page
man -s or  man -k
## How to redirect output > and |
The | command is called a pipe. It is used to pipe, or transfer, the standard output from the command on its left into the standard input of the command on its right. "Hello Worlds" | wc -w
The > symbol is used to redirect output by taking the output from the command on the left and passing as input to the file on the right. "Hello" > hello.txt
## How to append the output of a command to a file
The >> shell command is used to redirect the standard output of the command on the left and append (add) it to the end of the file on the right.
"Hello World!" >> greetings.txt
## How to use wildcards
[q2](wildcards.png)
## How to use brace expansion
Brace expansions use commands to make folders shortcuts. To use them
rm -r wallpapers/
mkdir -p wallpapers/cars/{1080p,2k,4k}
tree wallpapers/