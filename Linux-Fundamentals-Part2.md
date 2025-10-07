In this Linux Fundamentals Part 2, I learned several key concepts that help me better understand and navigate a Linux environment.
One of the main lessons was how to connect to a Linux machine remotely using SSH (Secure Shell).
This allows secure communication with remote systems through the terminal using commands like: ssh username@host_or_ip
and if the connection uses a different port: ssh -p 2222 username@host_or_ip 
Once connected, I explored various Linux commands and how to enhance their functionality with flags and switches.
I also learned how to access command documentation using man and --help options. 
For example, man ls provides a full manual page about the ls command, while ls --help shows a shorter summary of available options. 
I practiced using several essential commands to manage files and directories: ls -a shows all files, including hidden ones.
ls -l displays detailed information such as permissions and ownership. 
touch creates new files. 
mkdir makes new directories. 
cp copies files or directories (using -r for recursive copying). 
mv moves or renames files and directories. 
rm removes files or directories (with -r for recursive deletion). 
file checks the type of a file. cat displays the content of a file. 
These commands form the foundation of daily Linux usage and help in managing the filesystem efficiently. 
I also learned how to switch users and understand basic file permissions. 
Using the su command allows switching to another user or to root, while sudo executes commands with administrative privileges. 
File permissions control who can read, write, or execute files. 
Viewing them with ls -l shows permissions in a rwx format, and they can be modified using commands like chmod (change mode for file permissions) 
and chown means change owner of file or directory. 
Additionally, I explored important root directories in an Ubuntu system and their typical purposes: 
/etc — contains configuration files for the operating system and services. 
/var — stores variable data such as logs and cache files. 
/root — the home directory for the root user. 
/tmp — holds temporary files that are often cleared after reboot.
Overall, this room helped me become more comfortable with remote Linux access, command-line operations, file permissions, and the directory structure of a Linux system. 
These skills are essential for managing and understanding how Linux systems function, which is an important foundation for my cybersecurity learning journey.
