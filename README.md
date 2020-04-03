# Alexa-Skill
Alexa Voice Menus and JSON requests

Based mostly on amazon's flask-ask [tutorial](https://developer.amazon.com/blogs/post/Tx14R0IYYGH3SKT/Flask-Ask:-A-New-Python-Framework-for-Rapid-Alexa-Skills-Kit-Development)


# To Set Up
## Install Pip
To check if already installed try running:

`pip --version` and `pip3 --version`

either works but note that if pip3 worked but not pip then every pip below should be replaced with pip3

If these commands did not work then you can install pip with the following instructions

download [here](https://bootstrap.pypa.io/get-pip.py)

navigate to the download directory and run

`python3 get-pip.py`

## Install Flask-Ask:
`pip install flask-ask`

this threw an error when I first tried it.  I did a ton of googling, accidentally closed the window uninstalled and reinstalled things I didn't need to and then tried it again and it magically worked.  If you get a "import error no module named..." try closing the terminal window and running the install command again.

## Install Ngrok
Create an ngrok account [here](https://dashboard.ngrok.com/signup)
Login to your account
Follow steps 1-3  in ngrok's [setup tutorial](https://dashboard.ngrok.com/signup)

## Downgrade Cryptography (semi-optional)
This solved a "internal server error 500" that ngrok would throw when alexa launched the app.  You can try skipping this step, you might not get this error. who knows?

In the terminal run

`install cryptography==2.2.4me.py`

# To Run:
## Start the Application
In a terminal window, navigate to the directory that has the code and run

`python3 ./app.py`
## Open an ngrok channel
Open a new terminal window using `ctrl` `alt` `t`
then run

`./ngrok http 5000`

Leave this window open

## Point the skill to the channel
open alexa skill
update the default endpoint with the https://###.ngrok.io url displayed in the terminal next to "Forwarding" when you ran the `./ngrok http 5000` command.  Save these changes.

## Upload skill to Echo
I don't know yet.  For now use the 'test' tab in the Amazon skill console

