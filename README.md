# GIT_Tutorial

How to generate ssh key and configure ssh key in GIT.

## **Pre-requisites**

* Install Git in your system follow this **[link]**(https://git-scm.com/).
* Open *Git Bash* which looks like 
	![Git Bash](https://github.com/abhishekkdubey/GIT_Tutorial/blob/master/git_bash.PNG)

* Run the below command according to instructions


## **SSH keys**

An SSH key allows you to establish a secure connection between your computer and GIT. Before generating an SSH key in your shell, check if your system already has one by running the following command:

```
cat ~/.ssh/id_rsa.pub
```


If you see a long string starting with ssh-rsa or ssh-dsa, you can skip the ssh-keygen step.

Note: It is a best practice to use a password for an SSH key, but it is not required and you can skip creating a password by pressing enter. Note that the password you choose here can't be altered or retrieved.

To generate a new SSH key, use the following command:

```
ssh-keygen -t rsa -C "<username/Email Id/>"
```

This command will prompt you for a location and filename to store the key pair and for a password. When prompted for the location and filename, you can press enter to use the default.

Use the command below to show your public key:

```
cat ~/.ssh/id_rsa.pub
```

Copy-paste the key to the 'SSH and GPG Keys/SSH Keys' under the User settings or into user profile. Please copy the complete key starting with ssh- and ending with your username and host.

To copy your public key to the clipboard, use code below. Depending on your OS you'll need to use a different command:

## **Windows:**

```
clip < ~/.ssh/id_rsa.pub
```

## **Mac:**

```
pbcopy < ~/.ssh/id_rsa.pub
```

## **GNU/Linux (requires xclip):**

```
xclip -sel clip < ~/.ssh/id_rsa.pub
```

