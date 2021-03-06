# SSH-Starter-Interface

[![Build Status](https://travis-ci.org/NullDev/SSH-Starter.svg?branch=master)](https://travis-ci.org/NullDev/SSH-Starter)

This is a newer version of my SSH Starter script.

A small Expect script which will start SSH sessions with automatically entered password.<br>
You can specify <b>hostname</b>, <b>password</b>, <b>port</b> and <b>username</b> inside the script for **4** different servers. 

<sup>"ssh.sh" - When 97% of your keyboard is broken...</sup>

> Tested on Ubuntu 16.04 and 14.04

This script also features CLI arguments so you can connect to your server instantly without getting prompted to choose a server.

Usage: <br>
$ `./ssh.sh 1`<br>
$ `./ssh.sh 2`<br>
$ `./ssh.sh 3`<br>
$ `./ssh.sh 4`

**Extra feature**: You can pass a command as argument, which will be executed after login!

Example Usage: <br>
$ `./ssh.sh 1 echo hello` <br><br>
This will execute `echo hello` once the login was sucessful. 

### Small code info:
`expect "assword:"` on <a href="https://github.com/NullDev/SSH-Starter/blob/master/ssh.sh#L67">Line 67</a> is not a typo. 
It matches "Password" as well as "password".

## HOW TO INSTALL

1. Install expect script <br>
&nbsp;&nbsp;&nbsp;$ `sudo apt-get update` <br>
&nbsp;&nbsp;&nbsp;$ `sudo apt-get install expect` <br>

2. Clone and navigate to this repository <br>
&nbsp;&nbsp;&nbsp;$ `git clone https://github.com/NullDev/SSH-Starter.git && cd SSH-Starter` <br>

3. Move the script wherever you want <br>
&nbsp;&nbsp;&nbsp;$ `mv ssh.sh ..`<br>

4. Edit the script as you need it <br>
&nbsp;&nbsp;&nbsp;$ `cd .. && nano ssh.sh` <br>

5. Make the script executable <br>
&nbsp;&nbsp;&nbsp;$ `chmod +x ssh.sh` <br>

6. Thats it! You can either start in from the terminal with <br>
&nbsp;&nbsp;&nbsp;$ `./ssh.sh` <br>
Or by doubleclicking it!

## Optional:

If you do not want to store your password in the script directly, you could create a passwor file. Lets say you create a file called "p" in your home directory and store the password there. Then you can use 

`set SERVER_1_PKEY [exec cat ~/p]`

instead of 

`set SERVER_1_PKEY "password1"`

on <a href="https://github.com/NullDev/SSH-Starter/blob/master/ssh.sh#L9-L12">Line 9 to 12</a>.

However, this does not provide additional security (It isn't even security through obscurity). This is just for storing the password somewhere else instead of directly inside the script.

<p align="center">
<br>
<strike>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</strike> Screenshot <strike>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</strike><br><br>
</p>
<center>
<img src="https://raw.githubusercontent.com/NullDev/SSH-Starter/master/.src/scr1.png" />
</center>
