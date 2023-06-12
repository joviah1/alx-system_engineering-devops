#Shell, I/O Redirection
Describing what each script is doing
##A script that prints “Hello, World”, followed by a new line to the standard output.
*#!/bin/bash
*echo "Hello, World"
###A script that displays a confused smiley "(Ôo)'
*#!/bin/bash
*echo "(Ôo)'"
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
*echo -e "Best School" > "\\\*\\\\\\\'\\\"Best School"\'\\\\*\$\\\\?\\\*\\\*\\\*\\\*\\\*:)
##########A script that writes into the file ls_cwd_content the result of the command ls -la. If the file ls_cwd_content already exists, it should be overwritten.
*#!/bin/bash
*ls -la > ls_cwd_content
###########Write a script that duplicates the last line of the file iacta
*#!/bin/bash
*tail -n 1 < iacta >> iacta
