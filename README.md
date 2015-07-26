# Outline of Linux Phrasebook, 2nd Edition

Intro

1 Things to Know About Your Command Line

- Everything Is a File
- Maximum Filename Lengths
- Names Are Case-Sensitive
- Special Characters to Avoid in Names
- Wildcards and What They Mean
- Special Files That Affect Your Command Line
- If There’s Too Much, Reset `clear`

2 The Basics

- List Files and Folders `ls`
- List the Contents of Other Folders `ls`
- List Folder Contents Using Wildcards `ls *`
- View a List of Files in Subfolders `ls -R`
- View a List of Contents in a Single Column `ls -1`
- View Contents As a Comma-Separated List `ls -m`
- View Hidden Files and Folders `ls -a`
- Visually Display a File's Type `ls -F`
- Display Contents in Color `ls --color`
- List Permissions, Ownership, and More `ls -l`
- Reverse the Order Contents are Listed `ls -r`
- Sort Contents by File Extension `ls -X`
- Sort Contents by Date and Time `ls -t`
- Sort Contents by Size `ls -S`
- Express File Sizes in Terms of K, M, and G `ls -h`
- Display the Path of Your Current Directory `pwd` (also `pwd -L` & `pwd -P`)
- Change to a Different Directory `cd`
- Change to Your Home Directory `cd ~`
- Change to Your Previous Directory `cd -`
- Change a File to the Current Time `touch`
- Change a File to Any Desired Time `touch -t`
- Create a New, Empty File `touch`
- Create a New Directory `mkdir`
- Create a New Directory and Any Necessary Subdirectories `mkdir -p`
- Copy Files `cp`
- Copy Files Using Wildcards `cp *`
- Copy Files Verbosely `cp -v`
- Stop Yourself from Copying over Important Files `cp -i`
- Copy Directories `cp -R`
- Copy Files As Perfect Backups in Another Directory `cp -a`
- Move Files and Folders `mv`
- Rename Files and Folders `mv`
- Delete Files `rm`
- Remove Several Files At Once with Wildcards `rm *`
- Stop Yourself from Deleting Key Files `rm -i`
- Delete an Empty Directory `rmdir`
- Remove Files and Directories That Aren't Empty `rm -Rf`
- Delete Troublesome Files
- Become Another User `su username`
- Become Another User, with His Environment Variables `su -l`
- Become root `su`
- Become root, with Its Environment Variables `su -`
- REMOVED
	+ Find Out What mkdir Is Doing As It Acts `mkdir -v`
	+ Remove Files Verbosely `rm -v`

3 Learning About Commands

- Find Out About Commands with man	`man [command]`
- Quickly Find Out What a Command Does Based on Its Name `man -f, man --whatis`
- Search for a Command Based on What It Does `man -k, man --apropos`
- Read a Command's Specific Man Page `man [1-8]`
- Learn About Commands with info `info`
- Navigate Within info
- Locate the Paths for a Command's Executable, Source Files, and Man Pages `whereis`
- Find Out Which Version of a Command Will Run `which`
- Discover How a Command Will Be Interpreted `type`
- REMOVED
	+ Rebuild man's Database of Commands `man -u`
	+ Print man Pages `man -t`
	+ Read Descriptions of Commands `whatis`
	+ Find a Command Based on What It Does `apropos`

4 Building Blocks

- Run Several Commands Sequentially	`;`
- Run Commands Only If the Previous Ones Succeed `&&`
- Run a Command Only If the Previous One Fails `||`
- Plug the Output of a Command into Another Command `$()`
- Understand Input/Output Streams
- Use the Output of One Command As Input for Another `|`
- Redirect a Command's Output to a File `>`
- Prevent Overwriting Files When Using Redirection `set -o noclobber`
- Append a Command's Output to a File `>>`
- Use a File As Input for a Command `<`
- Combine Input and Output Redirection `< >`
- Send Output to a File and to stdout at the Same Time `tee`

5 Viewing Files

- Figure Out a File's Type `file`
- View Files on stdout `cat`
- Concatenate Files to stdout `cat file1 file2`
- Concatenate Files to Another File `cat file1 file2 > file3`
- Concatenate Files and Number the Lines `cat -n file1 file2`
- View Control Characters in a File `cat -vet`
- View Text Files a Screen at a Time `less file1`
- Search Within Your Pager
- Edit Files Viewed with a Pager
- View the First 10 Lines of a File `head`
- View the First Several Lines of a File or Files `head -n`
- View the Last 10 Lines of a File `tail`
- View the Constantly Updated Last Lines of a File or Files `tail -f`

REMOVED 6 Printing and Managing Print Jobs

6 Manipulating Text Files

- Count the Number of Words, Lines, and Characters In a File `wc`
	+ Also `wc -w`, `wc -l`, & `wc -c`
- Number Lines In a File `nl`
	+ Also `nl -t` & `nl -a`
- Format a file so it's more readable `fmt`
- Select an Entire Column of Data in a Delimited File `cut`
- Join Files Into Sequential Columns `paste`
	+ Also `paste -d`
- Sort the Contents of a File `sort`
	+ Also `sort -n`, `sort -r`, & `sort -k`
- Sort the Contents of a File Numerically `sort -n` & `sort -g`
- Remove Duplicate Lines In a File `uniq`
	+ Also `uniq -i`
- Compare Two or More Files To See What’s Changed `diff -u`
- Substitute Selected Characters with Others `tr`
- Delete matching characters `tr -d`
- Replace repeated characters with a single instance `tr -s`
- Find & Replace Text In a File `sed -i`
- Print Specific Fields In a File `awk`

7 Ownership & Permissions

- Change the Group Owning Files and Directories `chgrp`
- Recursively Change the Group Owning a Directory `chgrp -R`
- Change the Owner of Files and Directories `chown`
- Change the Owner of Files and Directories Based on the Current Owner `chown --from`
- Change the Owner and Group of Files and Directories `chown owner:group`
- Understand the Basics of Permissions
- Change Permissions on Files and Directories Using Alphabetic Notation `chmod`
- Change Permissions on Files and Directories Using Numeric Permissions `chmod`
- Change Permissions Recursively `chmod -R`
- REMOVED
	+ Keep Track of Changes Made to a File's Group with chgrp `chgrp -v, chgrp -c`

8 Archiving and Compression

- Archive and Compress Files Using zip `zip`
- Get the Best Compression Possible with zip `zip -[0-9]`
- Archive and Compress Files of a Specified Type in Directories and Subdirectories `zip -r test.zip . -i \*.htm`
- Password-Protect Compressed Zip Archives `zip -P -e`
- Unzip Files `unzip`
- Test Files That Will Be Unzipped `unzip -t`
- Archive and Compress Files Using gzip `gzip`
- Archive and Compress Files Recursively Using gzip `gzip -r`
- Uncompress Files Compressed with gzip `gunzip`
- Test Files That Will Be Unzipped with gunzip `gzip -t`
- Archive and Compress Files Using bzip2 `bzip2`
- Uncompress Files Compressed with bzip2 `bunzip2`
- Test Files That Will Be Unzipped with bunzip `bunzip2 -t`
- Archive Files with tar `tar -cf`
- Archive and Compress Files with tar and gzip `tar -zcvf`
- Test Files That Will Be Untarred and Uncompressed `tar -zvft`
- Untar and Uncompress Files `tar -zxvf`
- REMOVED
	+ List Files That Will Be Unzipped `unzip -l`
	+ Get the Best Compression Possible with gzip `gzip -[0-9]`
	+ Get the Best Compression Possible with bzip2 `bzip -[0-9]`

9 Finding Files, Directories, Words, & Phrases

- Search a Database of Filenames `locate`
- Search a Database of Filenames Without Worrying About Case `locate -i`
- Update the Database Used by locate `updatedb`
- Searching Inside Text Files for Patterns `grep`
- The Basics of Searching Inside Text Files for Patterns
- Search Recursively for Text in Files `grep -R`
- Search for Words and Highlight the Results `grep --color=auto`
- Search for Text in Files, Ignoring Case `grep -i`
- Search for Whole Words Only in Files `grep -w`
- Show Line Numbers Where Words Appear in Files `grep -n`
- Search the Output of Other Commands for Specific Words
- See Context for Words Appearing in Files `grep -A, -B, -C`
- Show Lines Where Words Do Not Appear in Files `grep -v`
- List Files Containing Searched-for Words `grep -l`
- List the Number of Occurrences of Words in Files `grep -c`
- Search for Words Inside Search Results `grep | grep`
- REMOVED
	+ Manage Results Received When Searching a Database of Filenames `locate -n`

10 The find Command

- Find Files by Name `find -name`
- Find Files by Ownership `find -user` & `find -group`
- Find Files by File Size `find -size`
- Find Files by File Type `find -type`
- Find Files by Modification Time `find -mtime`
- Show Results If the Expressions Are True (AND) `find -a`
- Show Results If Either Expression Is True (OR) `find -o`
- Show Results If the Expression Is Not True (NOT) `find -n`
- Execute a Command on Every Found File	`find -exec`
- Execute a Command on Found Files More Efficiently `find +` & `find | xargs`
- Execute a Command on Found Files Containing Spaces `find -print0`
- REMOVED
	+ Find Files by Group Ownership	`find -group`
	+ Print Find Results into a File `find -fprint`

11 Your Shell

- View Your Command-Line History `history`
- Run the Last Command Again `!!`
- Run a Previous Command Using Numbers `![##]`
- Run a Previous Command Using a String `![string]`
- Search for a Previous Command and Run It `^-r`
- Display All Command Aliases `alias`
- View a Specific Command Alias `alias [alias name]`
- Create a New Temporary Alias `alias [alias]='[command]'`
- Create a New Permanent Alias `alias [alias name]='[command]'`
- Remove an Alias `unalias`
- Create a New Temporary Function `[function name] ()` or `function [function name]`
- Create a New Permanent Function `[function name] ()` or `function [function name]`
- Display All Functions 
- Remove a Function `unset -f [function name]`
- When to Use an Alias and When to Use a Function

12 Monitoring System Resources

- Discover How Long Since Your Computer Was Restarted `uptime`
- View All Currently Running Processes `ps aux`
	+ Also `ps -w aux`
- View a Process Tree `ps axjf`
- View Processes Owned by a Particular User `ps U [username]`
- End a Running Process `kill`
- End Every Instance of a Running Process `killall`
- View a Dynamically Updated List of Running Processes `top`
- List Open Files `lsof`
- List a User's Open Files `lsof -u`
- List Users for a Particular File `lsof [file]`
- List Processes for a Particular Program `lsof -c [program]`
- Display Information About System RAM `free`
- Show File System Disk Usage `df`
- Report File Space Used by a Directory `du`
- Report Just the Total Space Used for a Directory `du -s`
- Report File Space Used by a Directory and Its Files `du -a`
- Create a Sorted Report of File Space Used by a Directory `du -k`

13 Installing Software

- Install Software Packages for RPM-Based Distributions `rpm -ihv, rpm -Uhv`
- Remove Software Packages for RPM-Based Distributions `rpm -e`
- Install Software Packages and Dependencies for RPM-Based Distributions `yum install`
- Remove Software Packages and Dependencies for RPM-Based Distributions `yum remove`
- Upgrade Software Packages and Dependencies for RPM-Based Distributions `yum update`
- FIX: Find Packages Available for Download for RPM-Based Distributions `yum search, yum list`
- Install Software Packages for Debian-Based Distributions `dpkg -i`
- Remove Software Packages for Debian-Based Distributions `dpkg -r`
- Install Software Packages and Dependencies for Debian-Based Distributions `apt-get install`
- Remove Software Packages and Dependencies for Debian-Based Distributions `apt-get remove`
- Upgrade Software Packages and Dependencies for Debian-Based Distributions `apt-get upgrade`
- Find Packages Available for Download for Debian-Based Distributions `apt-cache search`
- Clean Up Unneeded Installation Packages for Debian-Based Distributions `apt-get clean`
- Troubleshoot Problems with apt

14 Connectivity

- View the Status of Your Network Interfaces `ifconfig`
- Show All Open Network Connections `lsof -i`
- Verify That a Computer Is Running and Accepting Requests `ping, ping -c`
	+ Also `ping -n`
- Trace the Route Packets Take Between Two Hosts `traceroute`
	+ Also `traceroute -n`
- Perform Simple DNS Lookups `host`
- Perform Complex DNS Lookups `dig`
- Configure a Network Interface `ifconfig`
- View the Status of Your Wireless Network Interfaces `iwconfig`
- Configure a Wireless Network Interface `iwconfig`
- Grab a New Address Using DHCP `dhclient`
- Make a Network Connection Active `ifup`
- Bring a Network Connection Down `ifdown`
- Display Your IP Routing Table `route`
	+ Also `route -n`
- Change Your IP Routing Table `route`
- Troubleshooting Network Problems

15 Working on the Network

- Securely Log In to Another Computer `ssh`
- Securely Log In to Another Machine Without a Password `ssh`
- Securely and Conveniently Log In to Another Computer With a Password `ssh-agent`
- Emulate Several Terminals Within One, Even Disconnected `screen` (or `tmux`?)
- Securely Transfer Files Between Machines `sftp`
- Securely Copy Files Between Hosts `scp`
- Securely Transfer and Back Up Files `rsync -avz`
- Download Files Non-interactively `wget`
- Download Websites Non-interactively `wget -r`
- Download Sequential Files and Internet Resources `curl`
- Cruise the Web With a Text-Based Web Browser	`w3m`, `lynx`, & `elinks`

16 Windows Networking

- Discover the Workgroup's Master Browsers `nmblookup -M, -S, -A`
- Query and Map NetBIOS Names and IP Addresses `nmblookup -T`
- List a Machine's Samba Shares `smbclient`
- Access Samba Resources with an FTP-Like Client `smbclient`
- Mount a Samba Filesystem `mount -t cifs` & `umount -t cifs`
	+ Also `smbmount` & `smbumount`

17 Basic Shell Scripting

- Send Text to STDOUT `echo`
	+ Also `echo -e`
- Print a Sequence of Numbers `seq`
- Comment Your Script `#`
- Run Commands If Conditions Are Met (Or Not) `if then else`
- Execute a Command For Every New Value In a List `for`
- Run Commands While Something Is True `while`
	+ Also `until`
- Working With Variables `date="date +%Y-%m-%d"`
- Working With Functions
- Read User Input `read`
- Test If a Condition Is True Or False `test` & `[`
- Redirect Text Or Code To an Interactive Command (Here Document) `<<`
