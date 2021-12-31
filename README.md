![Gitstart](https://user-images.githubusercontent.com/82140149/147836931-c76261fc-6f77-41a8-8b2e-7a5679857c9a.png)

# **Gitstart**

[More details about Gitstart](https://towardsdatascience.com/automate-creating-a-new-github-repository-with-gitstart-1ae961b99866).

## Overview
> Gitstart creates, adds, and pushes with one line.<br><br>

This script automates creating a git repo. The script will:

•	Create .gitignore if you provide a language.<br>
•	Create a license.txt depends on your choice.<br>
•	Create a new repo at GitHub.com.<br>
•	Create a README.md file with the repo name.<br>
•	Add README.md and commit with a message.<br>
•	Add the remote and push the file.<br>

The script reads your GitHub username from ~/.config/gh/hosts.yml and uses the directory name as a GitHub repo name.


## Requirements

•	UNIX-lie (Tested on Ubuntu and MacOS.)

•	[GitHub CLI](https://cli.github.com/manual/), >v2.3.0.

•	[jq](https://stedolan.github.io/jq/).


Linux users can download gh cli from the [Releases page](https://github.com/cli/cli/releases), then run:


``` 
sudo apt install ./gh_x.x.x_xxxxxxx.deb
```

## Installation

### Linux/macOS using Awesome

After installing [Awesome package Manager](https://github.com/shinokada/awesome):

``` 
awesome install sachetutekar/gitstart
```


### MacOS using Homebrew

If you have Homebrew on your macOS, your can run:

``` 
brew tap sachetutekar/gitstart && brew install gitstart
```

### Debian/Ubuntu

Download the latest version from [releases page](https://github.com/shinokada/gitstart/releases) and run:

sudo apt install ./gitstart_version_all.deb

### Uninstallation

If you install Gitstart either Awesome package manager/Homebrew/Debian package, then the following will uninstall Gistart.

``` curl -s https://raw.githubusercontent.com/shinokada/gitstart/main/uninstall.sh > tmp1 && bash tmp1 && rm tmp1 ```

### Usage

•	Login github using gh auth login.
•	Starting gitstart

``` 
# define a dir path
gitstart -d repo-name
# in a current dir
cd new_repo
gitstart .
```

Adding language preference

``` 
gitstart -d repo-name -l python 

```

This will add python .gitignore as well.

•	The script asks you about your license preference.

``` 
Is it correct your GitHub username is sachetutekar? y/yes/n/no
y
>>> Your github username is sachetutekar.
>>> Your new repo name is test1.
Select a license:
1) MIT: I want it simple and permissive.
2) Apache License 2.0: I need to work in a community.
3) GNU GPLv3: I care about sharing improvements.
4) None
5) Quit
Your lisence: 2
Apache
Creating a public remote repo /Users/sachetutekar/Downloads/test1>>> Running git init.
Initialized empty Git repository in /Users/sachetutekar/Downloads/test1/.git/
? Repository name test1
? Repository description test1 repo
✓ Created repository sachetutekar/test1 on GitHub
✓ Added remote git@github.com: sachetutekar/test1.git
>>> LICENSE is created.
>>> Creating .gitignore for ...
```

•	Select a visibility.

```
>>> You are logged in. Creating your newtest in remote.
? Visibility  [Use arrows to move, type to filter]
> Public
  Private
  Internal
```

## About Licensing

Read more about [Licensing](https://docs.github.com/en/free-pro-team@latest/rest/reference/licenses).

## Author

Sachet Utekar

•	[Medium](https://medium.com/@sachet.utekar)<br>
•	[LinkedIn](https://www.linkedin.com/in/sachetutekar/)

## License

Copyright (c) 2021 Shinichi Okada (@sachetutekar) This software is released under the MIT License.
