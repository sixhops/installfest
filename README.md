# WDI Install Fest

We'll be installing the following tools.

* Slack
* Homebrew
* Oh my ZSH
* VS Code
* Git
* Node
* PostgreSQL
* Python
* Django

## Slack

We will be using slack to communicate throughout the course. You will receive an invite to the relevant channels via e-mail. You can login via the web browser, but downloading / installing the app is highly recommended.

[Download Slack](https://slack.com/downloads)

Remember to drag the Slack app into the Applications folder when you open the downloaded archive.

## Homebrew

Homebrew is a package manager that we will use to install various command line tools in our class.

Open up terminal, and paste the following command to install Homebrew. You might be prompted to install XCode Command Line Tools during the install process.

```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

If you are prompted to install the XCode CLI, say yes and your homebrew installation will continue.

After the installation process, run the command `brew doctor`. If any warnings or errors are displayed, we will need to resolve them before proceeding with the rest of the install fest.

Lastly, make sure to run `brew update` to make sure you have the latest lists of available software.

## Xcode

We do not use Xcode in class but some other applications that we do use require some Xcode libraries. Normally, all you need is the Xcode CLI which should have already been installed when you installed Homebrew. If it didn't get installed, you can use this command:

```
xcode-select --install
```

If you need to, you can install Xcode through the App Store. (You probably don't need to.) [Link here](https://itunes.apple.com/us/app/xcode/id497799835?mt=12)

## Install Oh My ZSH

[Oh-My-ZSH](https://github.com/robbyrussell/oh-my-zsh) is an advanced, customized shell that boosts productivity when working at the command prompt.

To install, use this command at the terminal prompt:

```
curl -L http://install.ohmyz.sh | sh
```

Restart Terminal, and you should see a brand new and colorful command prompt.

## Visual Studio Code
We'll be running Visual Studio Code as our text editor of choice. 

Download and install VSCode from [https://code.visualstudio.com/](https://code.visualstudio.com/)

Launch a terminal, and you should be able to open a folder to edit by typing `code .`

Check [this link](https://code.visualstudio.com/docs/setup/mac) for troubleshooting if you run into issues.

## Git

Git is the version control software we will be using.

To install Git:
```
brew install git
```

#### Setting up SSH Key

Please make sure you have signed up for an account on [Github](http://www.github.com).

You might find your self having to re-authenticate GIT every time you work on your command line. Setup SSH Keys to let Github remember your machine in the future.

* [Github Generating SSH Keys](https://help.github.com/articles/generating-ssh-keys/)

## Node

Node is a JavaScript engine for the backend. We use it to power our web servers and connect to our databases.

```
brew install node
```

Verify the installation afterwards by running:

```
node -v
npm -v
```

The above commands should display versions without any errors. To verify that all the required permissions are set correctly, try to install a global module:

```
npm install -g nodemon
```

This should install the `nodemon` module globally with no errors. If any errors occur, run this command to change the permissions associated with where npm installs modules:

```
sudo chown -R $USER /usr/local/lib
```

## PostgreSQL

Install the **PostgreSQL** database mangement system (DBMS) using Homebrew with this command:

```
brew install postgresql
```

After Postgres is installed run this command:

```
brew services start postgresql
```
 
Followed by this command:
 
```
createdb
```


## Installing MongoDB

Use homebrew to install the MongoDB server

```
brew install mongodb
```
Make the data directory with the following command:

```
sudo mkdir -p /data/db
```

Use this command to see the username that you used to log in:

```
whoami
```

Set data directory permissions (replacing USERNAME with the result from whoami above):

```
sudo chown -R USERNAME:wheel /data
```

### Testing the MongoDB server

You start the Mongo daemon (server) with the following command:
```
mongod
```

Press `control-c` to stop the server.

## Installing Python 3

Brew is also used to install Python 3. (Python 2 is already installed on your Mac.) To install Python 3 without errors, we first need to create a couple directories and change them to be owned by us:

```
mkdir /usr/local/lib
mkdir /usr/local/Frameworks
whoami
```
Make a note of the username returned from `whoami`. Enter that username in place of USERNAME below:
```
sudo chown -R USERNAME:wheel /usr/local/lib
sudo chown -R USERNAME:wheel /usr/local/Frameworks
```

If you received no errors from those commands, then use this command to install version 3:

```
brew install python3
```

You can test the installation by running `python3 --version`.

This should also install `pip3`, a package installer for Python 3. You can verify that it is installed and working by updating it with the following command:

```
pip3 install --upgrade pip setuptools wheel
```

This should return some normal messages - no errors. Now that `pip3` is working, we can use it to install a useful Python shell:

```
pip3 install ipython
```

iPython makes it easy to write python code in your terminal. We may not use it a huge amount but it is handy to have around.

## Installing Django

We will also use `pip3` to install Django, a robust back-end server for Python. We will be installing the 2.0.x version:

```
pip3 install Django
```

## Verify your installation

Make sure to restart your terminal and then run each of these commands. Finally call someone over to validate your installation.

```
python3 --version
pip3 --version

node -v
npm -v

git --version
psql --version
subl -v (or atom -v)

```

## Installing Spectacle

Install [Spectacle](https://www.spectacleapp.com/) for resizing windows.

## Installing Imgur

Create an account on [imgur.com](https://imgur.com/) and install [mac2imgur](https://github.com/mileswd/mac2imgur) to ease uploading screenshots and other images from your computer to your imgur account.
