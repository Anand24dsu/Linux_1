---
tags:
---
```
uname -a
```


```
head -n 1/etc/issue
```
```
mount
```
```
date
```
```
uptime
```
```
whoami
```
```
man bash 
```
```
env
```
```
echo $NAME
```
```
export a='anand'
```
```
echo $a
```
```
$PATH
```
```
$HOME
```
```
echo $SHELL 
```

Redirections
```
> [[read]] input  commands from the file
```
```
< # write output commands to file
```
```
>/dev/null [[discard]] output command
```
```
/dev/null [[Blackhole]] [[bit]] bucket
```
```
>> file # append output to file
```
```
command 1|commands 2# pipe output of commands 1 to commands2
```
Directory Operations
```
pwd #print working dire
```
make directory dir
```
mkdir anand
```
change dir
```
cd anand
```
go up a previous dir
```
cd..
```
list file and dir
```
ls
```
ls options
```
ls -a
```
```
ls -R
```
```
ls -r
```
```
ls -t
```
```
ls -S
```
```
ls -l
```
```
ls -1
```
```
ls -m
```
```
ls -Q
```
```
ls -lrt
```
Search files
```
grep --help
```
```
grep *.txt
```
```
grep -i 'echo' a.txt
```
```
grep -r age.txt
```
```
find /mnt/d/wsl/devops/ext4.vhdx *.txt
```
```
find /mnt/d/wsl/*/ext4.vhdx *.txt
```
```
whereis bash
```
```
locate /mnt/c/Users/Dell/Downloads/*.log
```


File Operations
```
touch 1.txt 2.log 3.py
```
```
cat 1.txt 2.log 3.py
```
```
less 1.txt 2.log 3.py
```
```
file 1.txt 2.log 3.py
```
```
cp 1.txt 2.txt
```
```
mv 1.txt 2.txt
```
```
rm 1.txt
```
```
rm -rf 1.txt
```
```
head age.txt
```
```
head -n age.txt
```
```
tail -n age.txt
```
Process Management
```
ps
```
```
top
```
```
kill pid
```
```
pkill python3
```
```
killall python3
```
```
kill -9 <pid>
```
```
killall
```

File Permissions
```
chmod 777 file
```
Link file
```
ln a.txt hardlink.txt
```


```
ln -s c.txt d.txt
```




```
touch file.txt file1.txt a.py b.py
``````

``````
touch -d "2002-01-31 15:45:30" anand.txt
``````


``````
touch -m -t 200201311530.45 a.txt
``````


```
touch {1..2}.py
``````

``````
touch {1..1000}.txt
``````

``````
touch {A..Z}.txt
``````

``````
touch {a..z}.py
``````

``````
stat anand.txt
``````


```
ln -s c.txt d.txt
```




**The _sha256sum_ command in Linux is used to compute and check SHA256 (256-bit) checksums.**



- `>`: Redirects output (overwrites the existing content).
    
- `>>`: Redirects output (appends to the existing content).
    
- `<`: Redirects input from a file.
    
- `2>`: Redirects error output (overwrites the existing content).
    
- `2>>`: Redirects error output (appends to the existing content).
    
- `&>`: Redirects both stdout and stderr (overwrites the existing content).
    
- `&>>`: Redirects both stdout and stderr (appends to the existing content).
    
- `|`: Pipes output of one command to another.
    
- `<<`: Here document for multi-line input.
    
- `<<<`: Here string for single-line input.
    
- `/dev/null`: Discards output.

It looks like you've posted the help message for the `gzip` command, which is used to compress and decompress files. Below are some examples of how you can use `gzip`:

### 1. **Compressing a File**:

- **Command**: `gzip file.txt`
- **Explanation**: This will compress `file.txt` and replace it with `file.txt.gz`. The original `file.txt` will be deleted by default.

### 2. **Compressing a File but Keeping the Original**:

- **Command**: `gzip -k file.txt`
- **Explanation**: This compresses `file.txt` to `file.txt.gz` but keeps the original `file.txt` unchanged.

### 3. **Decompressing a File**:

- **Command**: `gzip -d file.txt.gz`
- **Explanation**: This decompresses the `file.txt.gz` file and restores the original `file.txt`.

### 4. **Decompressing and Keeping the Compressed File**:

- **Command**: `gzip -dk file.txt.gz`
- **Explanation**: This decompresses the file `file.txt.gz` but keeps both the compressed and decompressed files.

### 5. **Compressing a File and Writing to Standard Output**:

- **Command**: `gzip -c file.txt > file.txt.gz`
- **Explanation**: This compresses `file.txt` and writes the compressed output to `file.txt.gz` without deleting the original file.

### 6. **Listing the Contents of a Compressed File**:

- **Command**: `gzip -l file.txt.gz`
- **Explanation**: This shows information about the contents of `file.txt.gz`, like its original size, compressed size, and compression ratio.

### 7. **Testing a Compressed File for Integrity**:

- **Command**: `gzip -t file.txt.gz`
- **Explanation**: This tests whether `file.txt.gz` is a valid gzip file without decompressing it.

### 8. **Compressing Files in a Directory Recursively**:

- **Command**: `gzip -r directory/`
- **Explanation**: This will recursively compress all files in the specified directory and its subdirectories.

### 9. **Using a Custom Suffix for Compressed Files**:

- **Command**: `gzip -S .gz2 file.txt`
- **Explanation**: This compresses `file.txt` and gives it the `.gz2` suffix instead of the default `.gz`.

### 10. **Compressing Files with the Best Compression Level**:

- **Command**: `gzip -9 file.txt`
- **Explanation**: This compresses `file.txt` with the highest compression level (slower, but more efficient).

### 11. **Compressing a File for Rsync**:

- **Command**: `gzip --rsyncable file.txt`
- **Explanation**: This compresses the file `file.txt` in a way that makes it more efficient for use with `rsync` (which can save bandwidth during file synchronization).

Tar file


You can replace `file.txt` and `directory/` with your own file and directory names

It looks like you've pasted the full help message for the `tar` command. Here are a few examples of how to use `tar` in various scenarios using the command:

1. **Creating an Archive**:
    - **Command**: `tar -cf archive.tar file1 file2 file3`
    - **Explanation**: This will create a tar archive named `archive.tar` containing `file1`, `file2`, and `file3`.
2. **Extracting an Archive**:
    - **Command**: `tar -xf archive.tar`
    - **Explanation**: This extracts the contents of the `archive.tar` into the current directory.
3. **Listing the Contents of an Archive**:
    - **Command**: `tar -tvf archive.tar`
    - **Explanation**: This lists all the files inside `archive.tar` in a verbose format.
4. **Appending Files to an Existing Archive**:
    - **Command**: `tar -rf archive.tar newfile1 newfile2`
    - **Explanation**: This adds `newfile1` and `newfile2` to the existing `archive.tar`.
5. **Extracting Files to a Specific Directory**:
    - **Command**: `tar -xf archive.tar -C /path/to/directory`
    - **Explanation**: This extracts the contents of `archive.tar` into `/path/to/directory`.
6. **Extracting Specific Files from an Archive**:
    - **Command**: `tar -xf archive.tar file1 file2`
    - **Explanation**: This extracts only `file1` and `file2` from `archive.tar`.
7. **Compressing an Archive with gzip**:
    - **Command**: `tar -czf archive.tar.gz file1 file2`
    - **Explanation**: This creates a gzipped tar archive named `archive.tar.gz` containing `file1` and `file2`.
8. **Using Wildcards**:
    - **Command**: `tar -cf archive.tar *.txt`
    - **Explanation**: This creates a tar archive named `archive.tar` containing all `.txt` files in the current directory.
9. **Excluding Files or Directories**:
    - **Command**: `tar -cf archive.tar --exclude='*.bak' .`
    - **Explanation**: This creates a tar archive but excludes all `.bak` files from being added.
10. **Extracting Files from a Compressed Archive**:
    - **Command**: `tar -xzf archive.tar.gz`
    - **Explanation**: This extracts the contents of a gzipped tar archive.

### File and Directory Management:

- `ls`: List directory contents.
- `cd`: Change directory.
- `mkdir`: Create a new directory.
- `rmdir`: Remove empty directories.
- `rm`: Remove files or directories.
- `cp`: Copy files or directories.
- `mv`: Move or rename files or directories.
- `touch`: Create an empty file or update file timestamps.
- `cat`: Concatenate and display file content.
- `head`: Display the beginning of a file.
- `tail`: Display the end of a file.

### File Permissions:

- `chmod`: Change file permissions.
- `chmod`: Change File Permissions

The `chmod` (change mode) command is used to change the file permissions on a Unix-based system. It can modify who can read, write, and execute a file.

#### Syntax:

bash

Copy code

`chmod [options] mode file_name`

- `mode`: The permissions you want to set (could be numeric or symbolic).
- `file_name`: The file or directory you want to change permissions for.

#### Numeric Mode (Octal Representation)

- `r` (read) = 4
- `w` (write) = 2
- `x` (execute) = 1

Permissions are represented by three digits:

- **Owner** (user)
- **Group**
- **Others**

Each permission is a sum of the numbers:

- `7` = read + write + execute (4+2+1)
- `6` = read + write (4+2)
- `5` = read + execute (4+1)
- `4` = read
- `3` = write + execute (2+1)
- `2` = write
- `1` = execute
- `0` = no permissions

#### Example:

1. **Set read, write, and execute for owner, and read for group and others:**
    
    bash
    
    Copy code
    
    `chmod 744 file.txt`
    
2. **Add execute permission to the owner:**
    
    bash
    
    Copy code
    
    `chmod u+x file.txt`
    
3. **Remove write permission from group:**
    
    bash
    
    Copy code
    
    `chmod g-w file.txt`
    
4. **Give read and execute permissions to everyone (owner, group, others):**
    
    bash
    
    Copy code
    
    `chmod a+rx file.txt`
    

### 2. `chown`: Change File Owner and Group

The `chown` command is used to change the owner and/or group of a file or directory.

#### Syntax:

bash

Copy code

`chown [options] owner:group file_name`

- `owner`: The new owner of the file.
- `group`: The new group associated with the file.
- `file_name`: The file or directory.

#### Examples:

1. **Change the owner of a file:**
    
    bash
    
    Copy code
    
    `chown newuser file.txt`
    
2. **Change the owner and group of a file:**
    
    bash
    
    Copy code
    
    `chown newuser:newgroup file.txt`
    
3. **Change the owner of a directory recursively:**
    
    bash
    
    Copy code
    
    `chown -R newuser directory_name`
    
4. **Change the group of a file without changing the owner:**
    
    bash
    
    Copy code
    
    `chown :newgroup file.txt`
    

### Additional `chmod` and `chown` Options:

- `-R`: Apply the command recursively (e.g., for all files in a directory).
- `-v`: Verbose mode, show what changes are being made.
- `-c`: Only report changes that actually occurred.

#### Example with `chmod` (Recursive):

bash

Copy code

`chmod -R 755 directory_name`

#### Example with `chown` (Recursive):

bash

Copy code

`chown -R newuser:newgroup directory_name`

Let me know if you need further clarification!
- `chown`: Change file owner and group.

### System Information:

- `pwd`: Print the current working directory.
- `whoami`: Display the current user.
- `uname`: Display system information.
- `df`: Display disk space usage.
- `du`: Display disk usage.
- `top`: Display tasks and system information.
- `ps`: Display current processes.
- `kill`: Terminate a process.
- `uptime`: Display how long the system has been running.

### Network:

- `ping`: Send ICMP ECHO_REQUEST to network hosts.
- `ssh`: Open SSH connection to a remote host.
- `scp`: Securely copy files between hosts.
- `wget`: Download files from the web.
- `curl`: Transfer data from or to a server.
- `netstat`: Print network connections, routing tables, interface statistics.
- `ifconfig`: Configure a network interface.
- `ip`: Show/manipulate routing, devices, policy routing, and tunnels.
- `traceroute`: Print the route packets take to the network host.

### Disk and Filesystem:

- `mount`: Mount a filesystem.
- `umount`: Unmount a filesystem.
- `mkfs`: Create a filesystem.
- `fsck`: Check and repair a filesystem.

### Text Processing:

- `grep`: Search text using patterns.
### Assertions

- **`\A`**: Start of the string.
- **`$`**: End of the string (or end of line in multi-line patterns).
- **`\Z`**: End of the string.
- **`\b`**: Word boundary.
- **`\B`**: Not a word boundary.
- **`\<`**: Start of a word.
- **`\>`**: End of a word.

### Character Classes

- **`\c`**: Control character.
- **`\s`**: White space.
- **`\S`**: Not white space.
- **`\d`**: Digit.
- **`\D`**: Not a digit.
- **`\w`**: Word character (letters, digits, and underscores).
- **`\W`**: Not a word character.
- **`\x`**: Hexadecimal digit.
- **`\O`**: Octal digit.

### POSIX Character Classes

These represent common categories of characters:

- **`[:upper:]`**: Uppercase letters.
- **`[:lower:]`**: Lowercase letters.
- **`[:alpha:]`**: Alphabetic letters.
- **`[:alnum:]`**: Alphanumeric (letters and digits).
- **`[:digit:]`**: Digits.
- **`[:xdigit:]`**: Hexadecimal digits.
- **`[:punct:]`**: Punctuation characters.
- **`[:blank:]`**: Space and tab.
- **`[:space:]`**: All whitespace characters (spaces, tabs, line breaks).
- **`[:cntrl:]`**: Control characters.
- **`[:graph:]`**: Visible characters (excluding spaces).
- **`[:print:]`**: Printable characters, including spaces.
- **`[:word:]`**: Word characters (alphanumeric and underscore).

### Lookahead and Lookbehind

- **`?=`**: Positive lookahead assertion.
- **`?!`**: Negative lookahead assertion.
- **`?<=`**: Positive lookbehind assertion.
- **`?<!`**: Negative lookbehind assertion.

### Quantifiers

These control how many times an expression can match:

- **`*`**: 0 or more occurrences.
- **`+`**: 1 or more occurrences.
- **`?`**: 0 or 1 occurrence.
- Adding a `?` makes a quantifier _ungreedy_ (match the smallest possible portion).

### Escape Sequences

- **`\`**: Escape the following character to treat it literally.
- **`\Q` and `\E`**: Begin and end literal sequence (escaping everything in between).

### Common Metacharacters

- **`\n`**: New line.
- **`\r`**: Carriage return.
- **`\t`**: Tab.
- **`\v`**: Vertical tab.
- **`\f`**: Form feed.
- **`\xxx`**: Octal character.
- **`\xhh`**: Hexadecimal character.

### Groups and Ranges

- **`(a|b)`**: Match `a` or `b`.
- **`(...)`**: Group matching.
- **`(?:...)`**: Non-capturing group.
- **`[abc]`**: Character class, matches any of `a`, `b`, or `c`.
- **`[^abc]`**: Matches any character except `a`, `b`, or `c`.
- **`[a-q]`**: Matches any lowercase letter from `a` to `q`.
- **`[0-7]`**: Matches any digit from 0 to 7.

### Pattern Modifiers

- **`g`**: Global match (find all matches).
- **`i`**: Case-insensitive matching.
- **`m`**: Multi-line matching.
- **`s`**: Treats the string as a single line.
- **`x`**: Allows comments and whitespace in patterns.
- **`e`**: Evaluate replacement.
- **`U`**: Ungreedy pattern.

### String Replacement

- **`$n`**: Refers to the nth captured group in replacement strings.
- **`$&`**: Entire matched string.
- **`$1`, `$2`, etc.**: First, second, etc., captured group.
- **`$'`**: After the matched string.
- **`$``**: Before the matched string.
- `awk`: Pattern scanning and processing language.
- `sed`: Stream editor for filtering and transforming text.
- `sort`: Sort lines of text files.
- `uniq`: Report or omit repeated lines.
- `wc`: Print newline, word, and byte counts for each file.
- `cut`: Remove sections from each line of files.
- `paste`: Merge lines of files.
- `diff`: Compare files line by line.
- `comm`: Compare two sorted files line by line.

### Compression:

- `tar`: Store and extract files from an archive file.
- `gzip`: Compress files.
- `gunzip`: Decompress files.
- `zip`: Package and compress files.
- `unzip`: Extract compressed files.

### Package Management:

- `apt-get`: Package handling utility in Debian/Ubuntu.
- `yum`: Package manager for RPM-based distributions.
- `dnf`: Package manager for RPM-based distributions (successor to `yum`).

### User Management:

- `useradd`: Create a new user.
- `usermod`: Modify a user account.
- `userdel`: Delete a user account.
- `passwd`: Update a user’s authentication tokens.
- `groupadd`: Create a new group.
- `groupdel`: Delete a group.
- `groups`: Show group memberships.

### Miscellaneous:

- `echo`: Display a line of text.
- `date`: Display or set the system date and time.
- `history`: Display the command history.
- `alias`: Create an alias for a command.
- `unalias`: Remove an alias.
- `crontab`: Schedule periodic background jobs.
- `at`: Schedule a command to run once at a particular time.
- `man`: Display the user manual for a command.
- `info`: Display command documentation.

### Common Unix/Linux Commands:

### File and Directory Management:

- `ls`: List directory contents.
    - `ls -l` (long format)
    - `ls -a` (include hidden files)
    - `ls -h` (human-readable file sizes)
    - `ls -r` (reverse order)
    - `ls -t` (sort by modification time)
- `cd`: Change directory.
    - `cd /path/to/directory` (change to specified directory)
    - `cd ..` (move up one directory)
    - `cd ~` (change to home directory)
- `mkdir`: Create a new directory.
    - `mkdir new_dir` (create `new_dir`)
    - `mkdir -p path/to/new_dir` (create nested directories)
- `rmdir`: Remove empty directories.
    - `rmdir dir` (remove `dir`)
    - `rmdir -p path/to/dir` (remove directories and their parents if empty)
- `rm`: Remove files or directories.
    - `rm file` (remove `file`)
    - `rm -r dir` (recursively remove `dir` and its contents)
    - `rm -f file` (force remove `file`)

### File Operations:

- `cp`: Copy files or directories.
    - `cp source destination` (copy `source` to `destination`)
    - `cp -r source_dir destination_dir` (recursively copy directories)
- `mv`: Move or rename files or directories.
    - `mv old_name new_name` (rename `old_name` to `new_name`)
    - `mv file1 file2 dir` (move `file1` and `file2` to `dir`)
- `touch`: Create an empty file or update file timestamps.
    - `touch file` (create `file`)
- `cat`: Concatenate and display file content.
    - `cat file` (display content of `file`)
- `head`: Display the beginning of a file.
    - `head file` (show the first 10 lines of `file`)
    - `head -n 20 file` (show the first 20 lines of `file`)
- `tail`: Display the end of a file.
    - `tail file` (show the last 10 lines of `file`)
    - `tail -n 20 file` (show the last 20 lines of `file`)

### 1. **File and Directory Management**

1. `ls`
2. `ls -l`
3. `ls -a`
4. `ls -lh`
5. `ls -R`
6. `pwd`
7. `cd /path/to/directory`
8. `cd ~`
9. `cd ..`
10. `cd -`
11. `mkdir directory_name`
12. `rmdir directory_name`
13. `rm filename`
14. `rm -r directory_name`
15. `rm -rf directory_name`
16. `cp source destination`
17. `cp -r source destination`
18. `mv source destination`
19. `mv old_name new_name`
20. `touch filename`
21. `stat filename`
22. `find /path -name "filename"`
23. `find /path -type f`
24. `find . -name "*.txt"`
25. `tree`
26. `ln filename link_name`
27. `ln -s filename symlink_name`
28. `which command`
29. `whereis command`
30. `updatedb`
31. `locate filename`
32. `file filename`
33. `chmod permissions filename`
34. `chmod +x filename`
35. `chmod 755 filename`
36. `chown user:group filename`
37. `chown -R user:group directory`
38. `chgrp group filename`
39. `umask`
40. `umask 022`
41. `readlink filename`
42. `realpath filename`
43. `basename filename`
44. `dirname filename`
45. `dir`
46. `dir -l`
47. `dircolors`
48. `lsblk`
49. `blkid`
50. `mount`
51. `umount`
52. `fstab`
53. `systemctl restart service`
54. `systemctl stop service`
55. `systemctl start service`
56. `systemctl enable service`
57. `systemctl disable service`
58. `xargs`
59. `install`
60. `mkfifo filename`
61. `read`
62. `wc`
63. `split`
64. `cmp`
65. `comm`
66. `cut`
67. `paste`
68. `tee`
69. `sponge`
70. `dir -p`
71. `find . -type f`
72. `find . -type d`
73. `find . -size +10M`
74. `find . -name "*.log"`
75. `find . -exec ls -lh {} \;`
76. `stat`
77. `tree -L 2`
78. `tree -d`
79. `tree -a`

### 2. **Text Viewing and Editing Commands**

80. `cat filename`
81. `more filename`
82. `less filename`
83. `head filename`
84. `head -n 10 filename`
85. `tail filename`
86. `tail -f filename`
87. `vim filename`
88. `vi filename`
89. `nano filename`
90. `gedit filename`
91. `emacs filename`
92. `nano -w filename`
93. `tee filename`
94. `cut -d ":" -f 1 filename`
95. `cut -f1,2 filename`
96. `sort filename`
97. `sort -r filename`
98. `uniq filename`
99. `wc filename`
100. `wc -l filename`
101. `wc -w filename`
102. `grep "pattern" filename`
103. `grep -i "pattern" filename`
104. `grep -r "pattern" /path`
105. `grep -v "pattern" filename`
106. `grep -E "regex" filename`
107. `sed 's/pattern/replacement/' filename`
108. `sed 's/pattern/replacement/g' filename`
109. `awk '{print $1}' filename`
110. `awk '{print $2, $3}' filename`
111. `tr 'a-z' 'A-Z' < input.txt`
112. `tr -d 'a' < input.txt`
113. `join file1 file2`
114. `diff file1 file2`
115. `cmp file1 file2`
116. `split filename`
117. `split -l 10 filename`
118. `emacs filename`
119. `vimdiff file1 file2`
120. `colordiff file1 file2`
121. `fold -w 80`
122. `shuf filename`
123. `uniq -c filename`
124. `fmt filename`
125. `column -t filename`

### 3. **System Information Commands**

126. `uname`
127. `uname -a`
128. `top`
129. `htop`
130. `ps`
131. `ps aux`
132. `ps -ef`
133. `df`
134. `df -h`
135. `du`
136. `du -sh *`
137. `free`
138. `free -h`
139. `uptime`
140. `who`
141. `whoami`
142. `w`
143. `id`
144. `last`
145. `last -n 10`
146. `dmesg`
147. `lscpu`
148. `lshw`
149. `lsblk`
150. `lsusb`
151. `lspci`
152. `ifconfig`
153. `ip addr show`
154. `ip a`
155. `ip link`
156. `hostname`
157. `hostnamectl`
158. `timedatectl`
159. `journalctl`
160. `systemctl status`
161. `systemctl list-units`
162. `sysctl -a`
163. `vmstat`
164. `iostat`
165. `mpstat`
166. `sar`
167. `watch command`
168. `uptime`
169. `arch`
170. `file /path/to/file`
171. `mount`
172. `umount`
173. `blkid`
174. `lvm`
175. `dmidecode`
176. `lsmod`
177. `modinfo`
178. `lsmod`
179. `lsusb`
180. `lsblk`
181. `ps -A`
182. `findmnt`
183. `ip route`

### 4. **Package Management Commands (Debian-based Systems)**

184. `sudo apt update`
185. `sudo apt upgrade`
186. `sudo apt install package_name`
187. `sudo apt remove package_name`
188. `sudo apt autoremove`
189. `sudo apt purge package_name`
190. `sudo apt-get install package_name`
191. `sudo apt-get remove package_name`
192. `sudo apt-get update`
193. `sudo apt-get upgrade`
194. `dpkg -l`
195. `dpkg -i package_name.deb`
196. `apt-cache search package_name`
197. `apt-cache show package_name`
198. `apt show package_name`
199. `apt list --installed`
200. `apt list package_name`
201. `sudo apt-get autoremove`
202. `sudo apt-get clean`
203. `sudo apt-get autoclean`
204. `sudo dpkg --configure -a`
205. `sudo apt-get dist-upgrade`
206. `apt list --upgradable`

### 5. **Package Management Commands (Red Hat-based Systems)** 

207. `sudo yum update`
208. `sudo yum install package_name`
209. `sudo yum remove package_name`
210. `sudo yum list installed`
211. `sudo yum search package_name`
212. `sudo yum info package_name`
213. `sudo yum clean all`
214. `sudo dnf install package_name`
215. `sudo dnf remove package_name`
216. `sudo dnf update`
217. `sudo dnf list installed`
218. `yum history`

### 6. **Disk Usage and Partitioning**

219. `fdisk -l`
220. `fdisk /dev/sda`
221. `parted /dev/sda`
222. `mkfs.ext4 /dev/sda1`
223. `tune2fs -l /dev/sda1`
224. `resize2fs /dev/sda1`
225. `mount /dev/sda1 /mnt`
226. `umount /mnt`
227. `lsblk`
228. `partprobe`
229. `gparted`
230. `df -h`
231. `du -sh *`
232. `smartctl -a /dev/sda`
233. `hdparm -I /dev/sda`
234. `mount -t ext4 /dev/sda1 /mnt`
235. `mount -t ntfs /dev/sda1 /mnt`
236. `swapoff -a`
237. `swapon -a`
238. `tune2fs -l /dev/sda1`
239. `fsck /dev/sda1`

### 7. **Networking Commands**

240. `ping 8.8.8.8`
241. `ping` [www.google.com](https://www.google.com "https://www.google.com/")
242. `traceroute google.com`
243. `nslookup google.com`
244. `dig google.com`
245. `ifconfig`
246. `ip addr`
247. `ip link`
248. `netstat`
249. `netstat -tuln`
250. `ss -tuln`
251. `route`
252. `route -n`
253. `wget` [http://example.com/file](http://example.com/file "http://example.com/file")
254. `curl` [http://example.com](http://example.com "http://example.com/")
255. `scp user@host:/path/to/file /local/path`
256. `rsync -avz source destination`
257. `ftp`
258. `sftp`
259. `telnet host port`
260. `ssh user@host`
261. `ssh -p port user@host`
262. `iptables -L`
263. `iptables -A INPUT -p tcp --dport 22 -j ACCEPT`
264. `ufw enable`
265. `ufw allow 22/tcp`
266. `ufw deny 23`
267. `ufw status`
268. `ufw reset`

### 8. **File Permissions and Ownership**

269. `chmod 755 filename`
270. `chmod +x filename`
271. `chmod -R 755 directory`
272. `chown user:group filename`
273. `chown -R user:group directory`
274. `chgrp group filename`
275. `umask 022`
276. `umask`
277. `setfacl`
278. `getfacl`
279. `ls -l`
280. `ls -Z`
281. `chcon`

### 9. **Process Management**

282. `ps aux`
283. `ps -ef`
284. `top`
285. `htop`
286. `kill <pid>`
287. `kill -9 <pid>`
288. `pkill process_name`
289. `killall process_name`
290. `bg`
291. `fg`
292. `jobs`
293. `nice`
294. `renice`
295. `at`
296. `cron`
297. `crontab -e`
298. `crontab -l`
299. `crontab -r`
300. `systemctl restart service`
301. `systemctl stop service`
302. `systemctl start service`
303. `systemctl status service`
304. `systemctl enable service`
305. `systemctl disable service`
306. `nice`
307. `renice`

### 10. **User and Group Management**

308. `useradd username`
309. `usermod -aG group username`
310. `userdel username`
311. `groupadd groupname`
312. `groupdel groupname`
313. `passwd username`
314. `chage -l username`
315. `chage -E 2024-12-31 username`
316. `id username`
317. `whoami`
318. `who`
319. `last`
320. `lastlog`
321. `adduser username`
322. `deluser username`
323. `groups username`
324. `sudo`
325. `sudo su`
326. `sudo usermod`
327. `sudo visudo`

### 11. **Searching and Finding**

328. `find /path -name "*.txt"`
329. `find /path -type f`
330. `find /path -mtime +5`
331. `locate filename`
332. `updatedb`
333. `grep -r "pattern" /path`
334. `grep "pattern" filename`
335. `grep -l "pattern" *`
336. `grep -i "pattern" filename`
337. `grep -v "pattern" filename`
338. `grep -E "regex" filename`

### 12. **Compression and Archiving**

339. `tar -cvf archive.tar directory`
340. `tar -xvf archive.tar`
341. `tar -czvf archive.tar.gz directory`
342. `tar -xzvf archive.tar.gz`
343. `tar -czf archive.tar.gz directory`
344. `tar -xzf archive.tar.gz`
345. `gzip filename`
346. `gunzip filename.gz`
347. `bzip2 filename`
348. `bunzip2 filename.bz2`
349. `xz filename`
350. `unxz filename.xz`
351. `zip archive.zip file1 file2`
352. `unzip archive.zip`
353. `rar a archive.rar file1 file2`
354. `unrar x archive.rar`

### 13. **Miscellaneous**

355. `history`
356. `history | grep command`
357. `clear`
358. `exit`
359. `echo "text"`
360. `echo $variable`
361. `date`
362. `cal`
363. `uptime`
364. `alias name='command'`
365. `unalias name`
366. `date +%Y-%m-%d`
367. `sleep 5`
368. `watch command`
369. `time command`
370. `man command`
371. `whatis command`
372. `info command`
373. `sudo command`
374. `sudo -i`
375. `sudo su`
376. `sudo visudo`
377. `sudo !!`
378. `sudo tee`
379. `sudo systemctl restart service`
380. `sudo shutdown now`
381. `sudo reboot`
382. `reboot`
383. `shutdown -h now`
384. `shutdown -r now`

### 14. **File System Management**

385. `mkfs.ext4 /dev/sda1`
386. `fsck /dev/sda1`
387. `mount /dev/sda1 /mnt`
388. `umount /mnt`
389. `tune2fs -l /dev/sda1`
390. `resize2fs /dev/sda1`
391. `e2fsck /dev/sda1`
392. `mount -o loop /path/to/file.iso /mnt`
393. `mount -t ntfs /dev/sda1 /mnt`
394. `mount -t ext4 /dev/sda1 /mnt`
395. `swapoff -a`
396. `swapon -a`

### 15. **Backup and Restore**

397. `rsync -avz source/ destination/`
398. `tar -cvf backup.tar directory/`
399. `tar -xvf backup.tar`
400. `cp -r source/ destination/`
401. `dd if=/dev/sda of=/path/to/backup.img`
402. `scp user@remote:/path/to/file /local/path`
403. `rsync -avz /local/backup/ remote:/path/`
404. `rsync -avz --delete /source/ /destination/`

### Linux Topics

### Basic File and Directory Commands

- `pwd` – Print the current working directory (shows where you are in the file system).
    - Example: `pwd`
- `cd` – Change the current directory.
    - Example: `cd /home/user/Documents`
- `ls` – List files and directories in the current directory.
    - Example: `ls`
- `mkdir` – Create a new directory.
    - Example: `mkdir new_folder`
- `rmdir` – Remove an empty directory.
    - Example: `rmdir old_folder`
- `rm` – Remove a file or directory.
    - Example: `rm file.txt`
    - To remove a directory with files: `rm -r folder_name`
- `cp` – Copy files or directories.
    - Example: `cp file1.txt file2.txt`
    - To copy a directory: `cp -r dir1/ dir2/`
- `mv` – Move or rename files and directories.
    - Example: `mv file1.txt newfile.txt` (rename)
    - To move a file: `mv file1.txt /home/user/Documents/`

### Text File Viewing and Editing

- `cat` – Display the content of a file.
    - Example: `cat file.txt`
- `more` – View the content of a file, one screen at a time.
    - Example: `more file.txt`
- `less` – Similar to `more`, but allows backward navigation.
    - Example: `less file.txt`
- `nano` – A simple text editor in the terminal.
    - Example: `nano file.txt`
    - Press `Ctrl + X` to exit.
- `echo` – Display a line of text or variable value.
    - Example: `echo "Hello, World!"`
- `head` – Show the first few lines of a file.
    - Example: `head file.txt`
- `tail` – Show the last few lines of a file.
    - Example: `tail file.txt`
- `wc` – Count words, lines, and characters in a file.
    - Example: `wc file.txt`

### System Information and Management

- `date` – Display the current system date and time.
    - Example: `date`
- `cal` – Display the current month's calendar.
    - Example: `cal`
- `whoami` – Show the current logged-in username.
    - Example: `whoami`
- `uptime` – Show how long the system has been running.
    - Example: `uptime`
- `hostname` – Display or set the system’s hostname.
    - Example: `hostname`
- `df` – Display disk space usage.
    - Example: `df -h`
- `free` – Display memory usage.
    - Example: `free -h`
- `top` – Display running processes and system resource usage.
    - Example: `top`

### User and Group Management

- `who` – Show who is logged into the system.
    - Example: `who`
- `whoami` – Show the current logged-in user.
    - Example: `whoami`
- `useradd` – Add a new user.
    - Example: `sudo useradd username`
- `passwd` – Change a user's password.
    - Example: `sudo passwd username`
- `groups` – Show the groups a user belongs to.
    - Example: `groups username`
- `id` – Display user ID (UID) and group ID (GID).
    - Example: `id username`

### File Permissions

- `chmod` – Change file permissions (read, write, execute).
    - Example: `chmod 755 file.txt` (Owner can read, write, and execute; group and others can read and execute)
- `chown` – Change file owner and group.
    - Example: `sudo chown user:group file.txt`
- `ls -l` – List files with detailed information (including permissions).
    - Example: `ls -l`

### Searching Files

- `find` – Search for files in a directory hierarchy.
    - Example: `find /home/user -name "*.txt"`
- `locate` – Find files by name quickly using a database (requires the `locate` database to be updated).
    - Example: `locate file.txt`
- `grep` – Search text in files for specific patterns.
    - Example: `grep "word" file.txt`

### Networking and Internet

- `ping` – Check the connectivity to a host or IP address.
    - Example: `ping google.com`
- `ifconfig` (or `ip a` on newer systems) – Display network interface information.
    - Example: `ifconfig`
- `curl` – Transfer data from or to a server using various protocols.
    - Example: `curl` [https://example.com](https://example.com "https://example.com/")
- `wget` – Download files from the web.
    - Example: `wget` [http://example.com/file.zip](http://example.com/file.zip "http://example.com/file.zip")

### Process Management

- `ps` – Display currently running processes.
    - Example: `ps aux`
- `kill` – Terminate a process by its PID (Process ID).
    - Example: `kill 1234` (where `1234` is the PID)
- `top` – Display system resource usage, running processes, and their statuses.
    - Example: `top`

### Disk and Filesystem Utilities

- `fdisk` – A tool for partitioning hard disks.
    - Example: `sudo fdisk -l` (list disk partitions)
- `mount` – Mount a filesystem.
    - Example: `sudo mount /dev/sda1 /mnt`
- `umount` – Unmount a mounted filesystem.
    - Example: `sudo umount /mnt`
- `lsblk` – List block devices and their mount points.
    - Example: `lsblk`
- `df` – Display disk space usage.
    - Example: `df -h`

### Package Management (Debian/Ubuntu-based systems)

- `apt-get update` – Update the package index.
    - Example: `sudo apt-get update`
- `apt-get upgrade` – Upgrade all installed packages to the latest versions.
    - Example: `sudo apt-get upgrade`
- `apt-get install` – Install a package.
    - Example: `sudo apt-get install firefox`
- `apt-get remove` – Remove a package.
    - Example: `sudo apt-get remove firefox`

### Archiving and Compression

- `tar` – Archive and compress files into a `.tar` file.
    - Example: `tar -cvf archive.tar file1 file2`
    - To extract: `tar -xvf archive.tar`
- `gzip` – Compress files with the `.gz` format.
    - Example: `gzip file.txt`
- `gunzip` – Decompress `.gz` files.
    - Example: `gunzip file.txt.gz`
- `zip` – Compress files into a `.zip` archive.
    - Example: `zip archive.zip file1 file2`
- `unzip` – Extract files from a `.zip` archive.
    - Example: `unzip archive.zip`

### Disk Usage and Management

- `du` – Display disk usage of files and directories.
    - Example: `du -sh folder_name`
- `lsblk` – List information about all block devices.
    - Example: `lsblk`
- `fsck` – Check and repair a filesystem.
    - Example: `sudo fsck /dev/sda1`

### System Shutdown and Reboot

- `shutdown` – Shut down the system.
    - Example: `sudo shutdown now`
- `reboot` – Reboot the system.
    - Example: `sudo reboot`
- `poweroff` – Turn off the system.
    - Example: `sudo poweroff`
### File and Directory Management

- `find` - Search for files in a directory hierarchy.
    - Example: `find /home/user -name "*.txt"`
- `locate` - Find files by name quickly using a database.
    - Example: `locate file.txt`
- `which` - Show the full path of shell commands.
    - Example: `which python`
- `basename` - Strips directory and suffix from filenames.
    - Example: `basename /path/to/file.txt`
- `dirname` - Get the directory name of a path.
    - Example: `dirname /path/to/file.txt`
- `ln` - Create hard and symbolic links.
    - Example: `ln -s /path/to/file /path/to/symlink`

### Text File Processing

- `grep` - Search for patterns in files.
    - Example: `grep "hello" file.txt`
- `awk` - A powerful text processing tool for pattern scanning and processing.
    - Example: `awk '{print $1}' file.txt`
- `sed` - Stream editor for transforming text.
    - Example: `sed 's/old/new/' file.txt`
- `tr` - Translate or delete characters.
    - Example: `echo "hello" | tr 'a-z' 'A-Z'`
- `tee` - Read from standard input and write to standard output and files.
    - Example: `echo "Hello World" | tee file.txt`

### System Monitoring and Performance

- `df -h` - Display disk space in a human-readable format.
- `du -sh` - Display directory space usage in a human-readable format.
- `free -m` - Display memory usage in megabytes.
- `iostat` - Report CPU and I/O statistics.
- `uptime` - Show how long the system has been running.
- `lscpu` - Display CPU architecture information.
- `dmesg` - Print kernel ring buffer messages.
- `lsof` - List open files and the processes using them.
- `tload` - Display terminal loading graph (in real-time).

### Networking

- `curl` - Transfer data from or to a server (supports many protocols).
    - Example: `curl` [http://example.com](http://example.com "http://example.com/")
- `wget` - Non-interactive network downloader.
    - Example: `wget` [http://example.com/file.zip](http://example.com/file.zip "http://example.com/file.zip")
- `ssh` - Secure Shell to login to a remote system.
    - Example: `ssh user@hostname`
- `scp` - Securely copy files between hosts over SSH.
    - Example: `scp file.txt user@hostname:/path/to/destination`
- `netstat` - Display network connections, routing tables, and interface statistics.
- `ss` - A utility to investigate sockets (faster than `netstat`).
- `traceroute` - Trace the route packets take to a network host.
    - Example: `traceroute google.com`
- `ifconfig` (or `ip a` on modern systems) - Display or configure network interfaces.
- `nslookup` - Query DNS records.
    - Example: `nslookup example.com`

### File Permissions and Ownership

- `chmod` - Change file permissions.
    - Example: `chmod 755 file.txt`
- `chown` - Change file owner and group.
    - Example: `chown user:group file.txt`
- `chgrp` - Change group ownership of a file.
    - Example: `chgrp group file.txt`
- `umask` - Set default file creation permissions.
    - Example: `umask 022`
- `getfacl` - Get file access control lists.
- `setfacl` - Set file access control lists.

### User Management

- `adduser` / `useradd` - Add a new user.
    - Example: `sudo useradd newuser`
- `passwd` - Change a user's password.
    - Example: `sudo passwd newuser`
- `usermod` - Modify a user account.
    - Example: `sudo usermod -aG group newuser`
- `deluser` / `userdel` - Delete a user account.
    - Example: `sudo userdel newuser`
- `groups` - Show user groups.
    - Example: `groups newuser`
- `who` - Display who is logged into the system.
- `w` - Show who is logged in and what they are doing.
- `last` - Show last login information.
- `sudo` - Run a command as a superuser or another user.

### Disk and Storage Management

- `fdisk` - Partition table manipulator for Linux.
    - Example: `sudo fdisk /dev/sda`
- `mkfs` - Create a filesystem on a device.
    - Example: `sudo mkfs.ext4 /dev/sda1`
- `mount` - Mount a filesystem.
    - Example: `sudo mount /dev/sda1 /mnt`
- `umount` - Unmount a filesystem.
    - Example: `sudo umount /mnt`
- `lsblk` - List information about block devices.
- `parted` - A tool for managing partitions.
- `blkid` - Find block device attributes.

### Process Management

- `ps` - List current running processes.
    - Example: `ps aux`
- `top` - Display tasks and their resource usage interactively.
- `htop` - An interactive process viewer, more user-friendly than `top`.
- `kill` - Terminate a process by PID.
    - Example: `kill 1234`
- `killall` - Kill processes by name.
    - Example: `killall processname`
- `bg` - Resume a suspended job in the background.
- `fg` - Bring a background job to the foreground.
- `jobs` - List background jobs.

### Archiving and Compression

- `tar` - Archive files.
    - Example: `tar -czvf archive.tar.gz file1 file2`
- `zip` - Compress files into a ZIP archive.
    - Example: `zip archive.zip file1 file2`
- `unzip` - Extract files from a ZIP archive.
    - Example: `unzip archive.zip`
- `gzip` - Compress files.
    - Example: `gzip file.txt`
- `gunzip` - Decompress files.
    - Example: `gunzip file.txt.gz`
- `bzip2` - Compress files (better compression than `gzip`).
    - Example: `bzip2 file.txt`
- `tar -xjvf` - Extract a `.tar.bz2` archive.

### System Administration and Maintenance

- `cron` - Daemon to execute scheduled commands.
- `crontab` - Edit cron jobs.
    - Example: `crontab -e`
- `systemctl` - Control the systemd system and service manager.
    - Example: `sudo systemctl restart nginx`
- `service` - Manage services on older systems (not using systemd).
    - Example: `sudo service apache2 restart`
- `journalctl` - Query and display logs from systemd.
    - Example: `journalctl -u nginx`
- `lsmod` - Show currently loaded kernel modules.
- `modprobe` - Add or remove modules from the Linux kernel.
- `lspci` - Display information about PCI buses and devices.
- `lsusb` - Display information about USB devices.
- `uname -r` - Show the kernel version.
- `hostname` - Show or set the system hostname.

### Disk and Filesystem Utilities

- `fsck` - Check and repair filesystem inconsistencies.
- `mount` - Mount a filesystem.
    - Example: `sudo mount /dev/sda1 /mnt`
- `df -h` - Display disk space usage in human-readable form.
- `du -sh` - Show the disk usage of files and directories.
- `xfs_check` - Check an XFS filesystem.
- `tune2fs` - Adjust tunable filesystem parameters for ext filesystems.

### Backup and Restore

- `rsync` - Sync files and directories between two locations.
    - Example: `rsync -av source/ destination/`
- `tar` - Archive files for backup.
    - Example: `tar -czvf backup.tar.gz /path/to/files`
