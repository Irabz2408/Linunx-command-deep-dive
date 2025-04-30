> # Linunx-command-deep-dive
* Linux Commands Deep Dive 
Now that you have a client terminal and have accessed your remote serve what next? 
For the next couple of projects, you will learn a lot about Linux commands, therefore, its time ti get your hands dirty. 


* What is a Linux Command? 
A Linux command refers to a program or utility that runs in the command-line interface (CLI). The CLI is a text-based environment where you interact with the system by typing commands 
Linux commands are executed by entering text in the Terminal and pressing Enter. These commands enable you to perform a wide range of tasks, including installing packages, managing users, manipulating files and directories, configuring system settings, and more. 
The general syntax of a Linux command is as follows: (Try the commands used as example as you read along) 

> # Command 
* A command may consist of options and parameters, but they are not always required. Here the key components of a command: 
CommandName: This represents the action or task you want to perform using the commanc For example if you wish to list files in a folder, you basically use the ' ls' command. 
![](./Images/ls%20command.png)



* Option or Flag: An option modifies the behavior of a command. It is typically preceded by c hyphen (-) or double hyphen (--) and can be used to customize the command's functionalit For example, if I want to show extra information for each listed file, i will run the command 'ls -l" 
![](./Images/ls%20-l%20command%20.png)


* Parameter or Argument A parameter provides specific information or data required by the command to execute the desired action. For example, if I want to create a new directory (or folder), I will use the 'mkdir' command. The parameter will be the name of the directory in which I will pass to it. 'mkdir photos' will create a photos directory. 
![](./Images/mkdir%20photo.png)


* It's important to note that Linux commands are case-sensitive, so you need to enter them exactly as they are spelled and formatted. 


> # Manipulating files and directories on Linux 


Most of your time on Linux will be working with files and directories. Hence, it is very important t know how to work with them. In the next section, we will focus on different commands that covers different use cases of manipulating files and directories on linux. 
The 'sudo' command 
In Linux, some actions need special permission to be carried out, like creating files in certain areas or changing important system settings. This is where the sudo command comes into pla) "sudo" stands for "superuser do," and it allows you to run commands with the security privileges of another user, typically the superuser or "root." 
Why Use sudo? 
Security: It helps in keeping the system secure by limiting access to powerful commands. Tracking: It logs who executed which command, adding a layer of accountability. 
How sudo Works: 
When you precede a command with sudo, Linux asks for your password. Once you enter it correctly, you can run commands as if you were the system's superuser for a short period (usual 15 minutes). This means you won't need to enter your password for each sudo command within 

Here's how you can do it: 
1. Open your terminal, and connect to your linux server using SSH. 
2. Try creating a folder in a restricted location. For example, let's try to create a folder namec "example" in the ' /root' directory, which is reserved for the root user: 
3. observe the error the failure . you are likely to encounter a permission denied error like this: 
![](./Images/mkdir%20root%20example.png)

this error because regular user do not have necessary permision to create directories in /root
 4. the we use sudo ton sucessfully create the folder
![](./Images/sudo%20root.png)

Note: Using sudo gives you significant power over your system, including the ability to change delete crucial system files. So, its wise to use it carefully and only when necessary 
pwd command 
Use the ' pwd' command to find the path of your current working directory. Simply entering pwd‘ will return the full current path - a path of all the directories that starts with a forward slash (/). For example, ' /home/username%. 
The ' pwd' command uses the following syntax: 

![](./Images/pwd%20command.png)


* To confirm you are there use the "pwd" command to check where you are 

To list out the files and directories on in root filesystem simply type "sudo ls -l" below we have the output
![](./Images/sudoo%20ls.png)


Side Hustle Task 1: 
Create a directory called ' photos' inside the ' /usr' directory navigate into the ' photos' directory Create 3 more random directories inside the ' photos' directory Show the newly created directories on the terminal Navigate into one of them Show the full path where you currently are on the screen 
Is command 
The 'I.s' command lists files and directories. Running it without a flag or parameter will show the current working directory's content. 
To see other directories' content, type 'ls' followed by the desired path. For example, to view files in the Documents folder, enter: 
Is /home/ubuntu/Documents 
Here are some options you can use with the Is command: 

* first i create a file named "photos"
![](./Images/mkdir%20photo.png)


* The "photo" files and i will also create more folders inside "photo" with names of "travel" "business" "family"
![](./Images/creating%20sub%20folder.png)

* And i will access one of the files "travels" 
![](./Images/cd%20travels.png)


* All these are ways of creating folder in an exsitng folder


> # CAT COMMAND 
cat command 
'Concatenate', or ' cat', is one of the most frequently used Linux commands. It lists, combines and writes file content to the standard output (i.e to the terminal console). To run the ' cat' command, type cat followed by the file name and its extension. For example: 

![](./Images/cat%20command.png)
