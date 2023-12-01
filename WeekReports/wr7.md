---
name: Tambi Samkough
semester: Fall 2023
course: cis-106
---

# Week Report 7

## Week Report Questions

### The cat command
(A) The cat command is used for displaying the content of a file, Cat is short for concatenate which is its command intended use. 
(B) cat + option +files(s) to display. 
(C) Display the contents of a file located in the pwd - cat todo.lst. Display yhe content of a file using absolute path - cat ~/Documents/todo.lst.
### The tac command
(A) The tac command is used for displaying the content of a file in reverse order. tac concatenates files and displays the output of the concatenation.
(B) tac + option + file(s) to display
(C) Display the content of a file located in the pwd - tac todo.md. Display the content of a file using absolute path - tac ~/Documents/todo.md.
### The head command
(A) The head command displays the top N number of lines of a given file. By default, it prints the first 10 lines. If more than one file name is provided then date from each file is preceded by its file name.
(B) head + option + file(s)
(C) Display the first 10 lines of a file. - head ~/Documents/Book/dracula.txt. Display the first 5 lines of a file. head -5 ~/Documents/Book/dracula.txt
### The tail command
(A) The tail command displays the last N number of lines of a given file. By default, it prints the last 10 lines. If more than one file name is provided then data from each file is preceded by its file name.
(B) tail + option + file
(C) Display the last 10 lines of a file. - tail ~/Documents/Book/dracula.txt. Display the last 5 lines of a file. tail -5 ~/Documents/Book/dracula.txt.
### The cut command
(A) The cut command is used to extract a specific section of each line of a file and display it to the screen.
(B) cut + option + file(s)
(C) Display a list of all the users in your system - cut -d ':' -f1 /etc/passwd. Display a list of all the users in your system with their login shell - cut -d ':' -f1,7 /etc/passwd
### The paste command
(A) The paste command is used for joining files horizontally in columns
(B) paste + option + files
(C) Merge two files - paste users.lst ip_address.lst. Merge two files using a different delimiter - paste -d ":" users1.lst ip_addresses.lst
### The sort command
(A) The sort command is used for sorting files. The sort command supports sorting: alphabetically, in reverse order, by number, and by month
(B) sort + option + file
(C) Sort a file - sort users.lst. Sort a file in reverse order - sort -r users.txt
### The wc command
(A) The wc command is used or printing the number of lines, characters and bytes in a file
(B) wc + option + file(s)
(C) Display the number of characters in a file - wc--m users.txt. Display the number of lines in a file - wc -l users.txt
### The tr command
(A) The tr command is used for translating or deleting characters from standard output.
(B) Standard output | tr + option + set + set
(C) Translate one character to another - cat file.txt | tr '.' ','. Translate white space into tabs - cat program.y | tr "[:space:]" '/t'
### The diff command
(A) The diff command compares files and displays the differences between them
(B) diff + option + file1 + file2
(C) Display the difference between two files - diff cars.csv cars-backup.csv. Display the difference between two files in a column format - diff -y cars.csv cars-backup.csv
### The grep command
(A) Grep is used to search text in a given file. Grep works line by line basis it matches the search criteria in a line by line basis
(B) grep + option + search criteria + file(s)
(C) Search any line that contains the word dracula in the given file - grep 'dracula' ~/Documents/dracula.txt. Search any line that contains the word dracula regardless of case with number line - grep -in 'dracula' ~/Documents/Books/dracula.txt
### The awk command
(A) Awk is a scripting language used for processing and displaying text. Awk can work with a text file or from a standard output. Awk was created in Bell Labs during the 70s. There are several implementations of Awk: nawk, mawk, gawk, and busybox. Awk performs operations line by line
(B) awk + options + awk command + file + file to save
(C) Print the first column of every line of a file - awk '{print $1}' ~/Documents/Csv/cars.csv. Print first field of /etc/passwd file - awk _F: '{print $1}' /etc/passwd
### The sed command
(A) SED is a stream editor that perform operations on files and standard output. For instance it can search, find and replace, insert, and deletion. By using SED you can edit files without opening them
(B) sed options + sed script + file
(C) Replacing a string in a given file - sed 's/pizza/rice/' shopping-list.lst. Replacing the number of occurrences of a pattern in a file - sed 's/pizza/rice/4' shopping-list.lst
### More Examples of the awk command
1. Print the last field of the /etc/passwd - awk -F: '{print $NF}' /etc/passwd
2. Print the first and last field of the /etc/passwd - awk -F: '{print $1," = ",$NF}' /etc/passwd
3. Print the first and 3 field with line numbers - awk -f: '{print NR,$1,$3}' /etc/passwd
4. Print the first and 4th field with a different field separator - awk -F: '{OFS="="}{print $1,$4}' /etc/passwd
5. Start printing a file from a given line besides the first two lines - awk 'NR > 3 { print }' /etc/passwd
### More Examples of the sed command
1. Replacing all the occurrence of the pattern in a file - sed 's/pizza/rice/g' shopping-list.lst
2. Replacing from the given number occurrence to the rest occurrences in a file. Start at the second time the word appears and continue to till the end of a file - sed 's/pizza/rice/3g' shopping-list.lst
3. Replacing string on a specific line number - sed '3 s/pizza/rice/' shopping-list.lst
4. Replacing string on a range of lines - sed'1,3 s/pizza/rice/' shopping-list.lst
5. To delete a particular line, Line 5 - sed '5d' shopping-list.lst