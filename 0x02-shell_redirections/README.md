#Shell, I/O Redirection
Describing what each script is doing
##A script that prints “Hello, World”, followed by a new line to the standard output.
*#!/bin/bash
*echo "Hello, World"
###A script that displays a confused smiley "(Ôo)'
*#!/bin/bash
*print('"(Ôo)\'')
####Display the content of the /etc/passwd file.
*#!/bin/bash
*cat /etc/passwd
#####Display the content of /etc/passwd and /etc/hosts
*#!/bin/bash
*cat /etc/passwd /etc/hosts
######Display the last 10 lines of /etc/passwd
*#!/bin/bash
*tail -n 10 /etc/passwd
#######Display the first 10 lines of /etc/passwd
*#!/bin/bash
*head -n 10 /etc/passwd
########Write a script that displays the third line of the file iacta.
*#!/bin/bash
*head -3 iacta | tail -1
#########Write a shell script that creates a file named exactly \*\\'"Best School"\'\\*$\?\*\*\*\*\*:) containing the text Best School ending by a new line.
*#!/bin/bash
*echo "Best School" > \\\\\\\"'\"Best School\"\\'"\\\\\\$\\\?\\\\\\\\\\\\\\\*\:\)
##########A script that writes into the file ls_cwd_content the result of the command ls -la. If the file ls_cwd_content already exists, it should be overwritten.
*#!/bin/bash
*ls -la > ls_cwd_content
###########Write a script that duplicates the last line of the file iacta
*#!/bin/bash
*tail -n 1 < iacta >> iacta
############Write a script that deletes all the regular files (not the directories) with a .js
*#!/bin/bash
*find . -type f -name "*.js" -delete
#############Write a script that counts the number of directories and sub-directories in the current directory.
*#!/bin/bash
*find . -type d -not -name '.' | wc -l
##############A script that displays the 10 newest files in the current directory
*#!/bin/bash
*ls -t1 | head
###############Create a script that takes a list of words as input and prints only words that appear exactly once.
*#!/bin/bash
*sort | uniq -u
################Display lines containing the pattern “root” from the file /etc/passwd
*#!/bin/bash
*grep -i "root" /etc/passwd
#################Display the number of lines that contain the pattern “bin” in the file /etc/passwd
*#!/bin/bash
*grep -c "bin" /etc/passwd
##################Display lines containing the pattern “root” and 3 lines after them in the file /etc/passwd
*#!/bin/bash
*grep -A 3 "root" /etc/passwd
###################Display all the lines in the file /etc/passwd that do not contain the pattern “bin”.
*#!/bin/bash
*grep -v "bin" /etc/passwd
####################Display all lines of the file /etc/ssh/sshd_config starting with a letter.
*#!/bin/bash
*grep '^[A-Za-z]' /etc/ssh/sshd_config
#####################Replace all characters A and c from input to Z and e respectively.
*#!/bin/bash
*tr "A" "Z" | tr "c" "e"
######################Create a script that removes all letters c and C from input
*#!/bin/bash
*tr -d "Cc"
#######################Write a script that reverse its input.
*#!/bin/bash
*rev
########################Write a script that displays all users and their home directories, sorted by users.
*#!/bin/bash
*cut -d ":" -f1,6 /etc/passwd | sort
######################### A command that finds all empty files and directories in the current directory and all sub-directories
*#!/bin/bash
*find . -empty | rev | cut -d '/' -f 1 | rev
##########################A script that lists all the files with a .gif extension in the current directory and all its sub-directories.
*#!/bin/bash
*find -type f -name "*.gif" | rev | cut -d "/" -f 1 | cut -d '.' -f 2- | rev | LC_ALL=C sort -f
###########################Create a script that decodes acrostics that use the first letter of each line
*#!/bin/bash
*cut -c 1 | paste -s -d ''
############################A script that parses web servers logs in TSV format as input and displays the 11 hosts or IP addresses which did the most requests.
*#!/bin/bash
*tail -n +2 <file_name> | cut -f -1 | sort -k 1 | uniq -c | sort -rnk 1 | head -n 11 | rev | cut -d '' -f -1 | rev

