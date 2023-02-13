# BASH TIPS, TRICKS and FUN HINTS

Small Change

This is a compilation of useful tools, codeblocks and best practices for BASH scripting and Linux administration and some small git maneuvers. If using VS Code, press `ctrl + shift + V` to view the Markdown File in all its glory.

### Most linux systems have a maximum number of 32768 PIDs (Process ID numbers). One way to check your max-pid is with the command.
- `cat /proc/sys/kernel/pid-max`
### Should you ever encounter an error like "Cannot Allocate Memory", max-pid is one thing you can check. Some other useful commands for troubleshooting PIDs and memory usage are:
- `ps -eLF`
- `free`
- `du`
- `top`

### Synchronous - one at a time
#### Semi-colon lets the bash know that echo a and echo b are two separate commands and need to be run separately one after the other.
- echo a;
- echo b;

### Return value of last command
- `echo $?`

### Return public IP address
- `curl ifconfig.me`

### configuring network interfaces
- `ip`

### Text User Interface for controlling NetworkManager
- `nmtui`

### terminate processes by PID
- `kill`
### enter messages into the system log
- `logger`
### socket stats
- `ss`
### process snapshot
- `ps`
### Print network connections, routing tables, interface statistics
- `netstat`
###  firewalld (suite) [documentation](https://firewalld.org/documentation/utilities/)
- `firewall-cmd`...
### bring most recently stopped process to fg (or input PID for specificity)
- `fg`
### interactive view of text stream
- `less`
### disk free
- `df`
### DNS lookup utility (domain info groper)
- `dig`

### switch to the root user
- `sudo su`

### On the difference between [], [[]], and (())
- [] is equal to the test command, returns a true or false value
- [[]] is the newer more versatile test command which supports the < > operators. [] will interpret < > operators as redirections as in adding text to a file
- Does not work with all kinds of shells other than BASH
- (()) has applications that allow bash to perform math similar to C syntax.
- If `a=1` then `echo \$((a++))` returns 1 and then increments "a" to 2
On the other hand, if `echo \$((++a))`, "a" gets incremented before the echo is called so "2" is returned.

### `shift [n]`
- moves arguments over [n] spaces. \$1 after shift 3 will become \$4. \$2 after shift n will become \$(2+n)

### Verify shasum
- `shasum -a 256 /path/to/file`

### VIM
- in command mode in vim: dd deletes the line selected

### git
- `git log` shows all edits, timestamp and author in chronological order
- `git branch -a` - displays all branches in repo
- `git rev-list --all --count` show number of commits in the repo
- `git init --initial-branch main` we're not naming our branches "master" anymore
- `git remote rename <current> <new>` rename remote to "origin"
- `git remote -v` verify remote location and name
- `git push -u origin main` push to remote upstream: necessary on first push to remote

### ssh key for git



### Ansible
- Made by Red Hat, a suite of open-source software tools that enables infrastructure as code. Includes software provisioning, configuration management, and application deployment functionality.
- Study terraform/kubernetes/Jenkins over ansible